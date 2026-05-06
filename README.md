# OrangeFox Action Builder
Compile your first custom recovery from OrangeFox Recovery using Github Action.

# How to Use
1. Fork this repository.

2. Go to `Action` tab > `All workflows` > `OrangeFox - Build` > `Run workflow`, then fill all the required information:
 * MANIFEST_BRANCH (`12.1` and `11.0`)
 * DEVICE_TREE (Your device tree repository link.)
 * DEVICE_TREE_BRANCH (Your device tree repository branch.)
 * DEVICE_PATH (`device/vendor/codename`)
 * DEVICE_NAME (Your device codename)
 * BUILD_TARGET (`boot`, `recovery`, `vendorboot`)

## Example: build for Samsung Galaxy J7 (j7elte)
Use these values when running the workflow:

* `MANIFEST_BRANCH`: `12.1`
* `DEVICE_TREE`: your j7elte OrangeFox/TWRP-compatible device tree repository URL
* `DEVICE_TREE_BRANCH`: your device-tree branch for Android 12.1 (for example, `android-12.1`)
* `DEVICE_PATH`: `device/samsung/j7elte`
* `DEVICE_NAME`: `j7elte`
* `BUILD_TARGET`: `recovery`

> Tip: if the build fails at `lunch` or during recovery image generation, verify your device tree uses the latest OrangeFox variables for your selected manifest branch.

 # Note
* This action will now only support manifest 12.1 and 11.0, since all orangefox manifest below 11.0 are considered obsolete.
* Make sure your tree uses right variable (updated vars) from OrangeFox; [fox_11.0](https://gitlab.com/OrangeFox/vendor/recovery/-/blob/fox_11.0/orangefox_build_vars.txt) and [fox_12.1](https://gitlab.com/OrangeFox/vendor/recovery/-/blob/fox_12.1/orangefox_build_vars.txt), to avoid build erros.
