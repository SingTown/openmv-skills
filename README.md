# OpenMV Skills

English | [简体中文](README-CN.md)

A plugin by [SingTown](https://singtown.com) for OpenMV Camera development.

## What the agent does

When you ask for OpenMV help, the agent is instructed to work like an embedded vision assistant, not just a code generator. It will:

- Automatically search the bundled official examples for similar scripts and proven patterns
- Check the local OpenMV API documentation before using functions or modules, so it avoids guessing unsupported APIs
- Write a complete runnable MicroPython script and save it locally as the source of truth
- When you want to test on hardware, discover and connect to an OpenMV camera through the MCP tools
- Run the saved script on the camera, read stdout/stderr, and capture frames from the camera
- Inspect the captured image output, compare it with the intended behavior, and iterate on the script
- Debug errors, tune thresholds or parameters, and rerun the script until the result matches the task
- Deploy the script as `main.py` only when you explicitly want it to run on boot

## Installation

Type the following in Claude Code or Codex:

```text
install https://raw.githubusercontent.com/SingTown/openmv-skills/refs/heads/main/INSTALL.md
```

## License

[MIT](LICENSE)
