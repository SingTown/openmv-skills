# Agent Installation Runbook

Audience: AI coding agents installing the OpenMV plugin for Codex or Claude
Code.

Goal: install `openmv-mcp` first, verify `openmv_mcp_server` is available on
the host `PATH`, then install the `openmv` plugin from the `singtown`
marketplace with the host tool's native plugin system.

## Step 1: Install openmv-mcp

Detect the host operating system and run exactly one matching branch.

### Windows Host

Requirement: install on the Windows host with `winget`. Do not install
`openmv-mcp` inside WSL.

If the active shell is WSL, stop and report that `openmv-mcp` must be installed
from Windows PowerShell on the host.

Run in Windows PowerShell:

```powershell
winget install SingTown.openmv-mcp
```

Verify in Windows PowerShell:

```powershell
openmv_mcp_server --help
```

Continue only after the verify command succeeds.

### macOS

Requirement: only Apple Silicon macOS is supported.

Install with Homebrew:

```bash
brew install SingTown/openmv/openmv-mcp
```

Verify:

```bash
openmv_mcp_server --help
```

Continue only after the verify command succeeds.

### Linux

Install with the default installer:

```bash
curl -fsSL https://raw.githubusercontent.com/SingTown/openmv-mcp/main/install.sh | sh
```

Verify:

```bash
openmv_mcp_server --help
```

Continue only after the verify command succeeds.

If a connected OpenMV camera cannot be opened because of serial permissions on
Debian or Ubuntu, run:

```bash
sudo usermod -aG dialout "$USER"
```

Then report that the user must log out and log back in before camera access can
work.

## Step 2: Install the OpenMV Plugin

Use the native plugin system for the active AI coding tool.

### Codex

Add the marketplace. If `singtown` is already registered, skip this command.

```bash
codex plugin marketplace add https://github.com/SingTown/openmv-skills
```

Install the plugin:

```bash
codex plugin add openmv@singtown
```

If the plugin is already installed, treat that as success and continue.

### Claude Code

Run these as Claude Code slash commands, not as shell commands.

Add the marketplace. If `singtown` is already registered, skip this command.

```text
/plugin marketplace add https://github.com/SingTown/openmv-skills
```

Install the plugin:

```text
/plugin install openmv@singtown
```

If the plugin is already installed, treat that as success and continue.

## Step 3: Reload the Agent Context

After installing the plugin, start a new Codex thread or a new Claude Code
session. Do not verify in the old session unless the host explicitly says plugin
reloads are available without a restart.

## Step 4: Verify

In the new session, verify plugin activation with one of these requests:

```text
Use OpenMV to list connected cameras.
```

If no camera is connected, verify skill activation with:

```text
Use OpenMV to write a color tracking script.
```

Expected result: the OpenMV skill activates, and MCP camera tools are available
when a camera operation is requested.

## Failure Handling

### `openmv_mcp_server` Not Found

Do not install the plugin until `openmv_mcp_server --help` succeeds.

- Windows: confirm installation happened on the Windows host, not inside WSL.
- macOS: confirm the machine is Apple Silicon and Homebrew installed
  `SingTown/openmv/openmv-mcp`.
- Linux: rerun the default installer:

```bash
curl -fsSL https://raw.githubusercontent.com/SingTown/openmv-mcp/main/install.sh | sh
```

### Plugin Does Not Activate

Start a new Codex thread or Claude Code session. Plugin skills and MCP tools are
loaded at session startup.

### Camera Is Not Detected

Check these conditions before changing code:

- The OpenMV camera is connected over USB.
- OpenMV IDE or another serial tool is not already using the camera.
- `openmv_mcp_server --help` succeeds on the host.
- On Linux, the user has permission to access serial devices.
