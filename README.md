# Test Extension

Clone the repo [godot-cpp](https://github.com/godotengine/godot-cpp).

```shell
git clone https://github.com/godotengine/godot-cpp.git -b 4.3
```

## Building the C++ bindings

This step builds godot-cpp.

```shell
godot --dump-extension-api
# OR
/Applications/Godot43.app/Contents/MacOS/Godot --dump_extension-api

cp extension_api.json <root>

# Build the godot-cpp
cd godot-cpp
scons platform=macos custom_api_file=extension_api.json
cd ..
```

## Building the plugin

This step builds the plugin library to the demo project.

```shell
scons platform=macos compiledb=yes
```

## Editing in IDE

```shell
code .
# OR
clion .
```
