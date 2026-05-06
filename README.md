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

## Build preset: Samsung Galaxy J7 (j7elte)
Use the values below when triggering the workflow for **j7elte**:

* `MANIFEST_BRANCH`: `12.1` (recommended first), fallback `11.0`
* `DEVICE_TREE`: Your j7elte device tree repository URL
* `DEVICE_TREE_BRANCH`: The branch matching your OrangeFox base (for example `fox_12.1`)
* `DEVICE_PATH`: `device/samsung/j7elte`
* `DEVICE_NAME`: `j7elte`
* `BUILD_TARGET`: `recovery`

### Example

```text
MANIFEST_BRANCH=12.1
DEVICE_TREE=https://github.com/<your-user>/android_device_samsung_j7elte
DEVICE_TREE_BRANCH=fox_12.1
DEVICE_PATH=device/samsung/j7elte
DEVICE_NAME=j7elte
BUILD_TARGET=recovery
```

After the run finishes, download the built recovery image from the workflow artifacts.

 # Note
* This action will now only support manifest 12.1 and 11.0, since all orangefox manifest below 11.0 are considered obsolete.
* Make sure your tree uses right variable (updated vars) from OrangeFox; [fox_11.0](https://gitlab.com/OrangeFox/vendor/recovery/-/blob/fox_11.0/orangefox_build_vars.txt) and [fox_12.1](https://gitlab.com/OrangeFox/vendor/recovery/-/blob/fox_12.1/orangefox_build_vars.txt), to avoid build erros.
