# Godot in a DevContainer (Proof of Concept)

This repository is a proof of concept to get Godot running in a devcontainer environment.
I did it on a whim to see if it was possible to run Godot in a devcontainer, I'm just glad it didnt cost me that much time.

to run in devcontainer:

``` Godot_v4.4.1-stable_linux.x86_64 ```

## Key Points

- **GUI Version**: This setup is for the GUI version of Godot, not the headless version.
- **Godot with .NET**: The intention is to integrate this as a version of Godot with .NET support.
- **Hardware Compatibility**: Tested on an AMD iGPU 8600G. Compatibility with other GPUs is not claimed. It will probably work with recent Ryzen iGPUs
- **Testing**: This setup has not been extensively tested. Use at your own risk.
- **VScode integration with Godot**: not tested yet
- **Linux**: This setup is for Linux only ( am running Kubuntu 24.04 and KDENeon), I have no idea if it will run under WSL2 ( maybe someday I'll test)

## Notes

If you need to update Godot you can do so by changing the version in the Dockerfile. The current version is 4.4.1