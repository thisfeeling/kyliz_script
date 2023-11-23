### Kyliz Script

### Releases

*  [Stable](https://github.com/thisfeeling/kyliz_script/releases)

### Script Configuration Example

```bash
KERNEL_TREE_BRANCH="11.0"
KERNEL_TREE="https://github.com/thisfeeling/kernel_motorola_msm8953"
DEVICE_CODENAME="ali"
KERNEL_DEFCONFIG="ali_defconfig"
BUILD_STATUS="UNOFFICIAL"
BUILD_TYPE="BETA"
KERNEL_NAME="Perf"
ARCH="arm64"
DTC_EXT="dtb"
CLANG_TREE="https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+archive/f8e856556909898bd35ee8eae829437721b5a3db/clang-r353983e.tar.gz"
CLANG_VERSION="clang-r353983e"
CLANG_VERSION_STRING="Clang Version 9.0.5"
CLANG_VERSION_DIR="clang-9"
ARM_LINUX_ANDROIDEABI_TREE="https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/arm/arm-linux-androideabi-4.9/+archive/refs/heads/pie-release.tar.gz"
AARCH64_LINUX_ANDROID_TREE="https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+archive/refs/heads/pie-release.tar.gz"
AARCH64_LINUX_GNU_TREE="https://github.com/theradcolor/aarch64-linux-gnu"
AARCH64_LINUX_GNU_TREE_BRANCH="stable-gcc"
ARM_LINUX_ANDROIDEABI_VERSION="arm-linux-androideabi-"
AARCH64_LINUX_ANDROID_VERSION="aarch64-linux-android-"
AARCH64_LINUX_GNU_VERSION="aarch64-linux-gnu-"
```
### Necessary Files "verify_dtb_ziptool"

*  [AnyKernel3](https://github.com/thisfeeling/kyliz_script/tree/kyliz/AnyKernel3)
*  [Dtbtool](https://github.com/thisfeeling/kyliz_script/tree/kyliz/Dtbtool)

### Execution
```bash
$ sudo chmod +x buildkernel.sh && sudo ./buildkernel.sh 
```
### All Changelog

### K1.2.6 STABLE 20231120

**-Improvements to "download_tools".**

**-Improvements to "download_kernel".**

**-Improvements to "install_dependencies".**

**-Fixed some code bugs.**

### K1.2.5 STABLE 20231118

**-Added "" In some variables.**

**-Improvements to "abort_if_error".**

**-Improvements to "show_status".**

**-Added "validate_environment_variables".**

**-Added "check_os".**

### K1.2.4 STABLE 20231113

**-Fixed script error $DEVICE_CODENAME/buildkernel-log-$DATE_POSTFIX-$TIME_POSTFIX.txt No such file or directory.**

**-"generate_log_filename" change by "BUILD_KERNEL_LOG".**

**-Fixed some code bugs.**

### K1.2.3 STABLE 20231113

**-Added "validate_dependencies" & "install_missing_dependencies"**

**-Added "generate_log_filename"**

**-The functions were ordered.**

**-Fixed some code bugs.**

### K1.2.2 STABLE 20231111

**-Added delay.**

**-Any functions were ordered.**

**-Fixed .git error "DEVICE_CODENAME_DIR".**

**-Fixed permission denied in "DEVICE_CODENAME_DIR".**

**-Fixed some code bugs.**

**-Obsolete code was deleted.**

### K1.2.1 STABLE 20231108

**-Added "verify_output_files"**

**-Added "set -e" in "abort_if_error".**

**-The functions were ordered.**

**-Fixed some code bugs.**

### K1.2 STABLE 20231107

**-Fixed some bugs with variables "DEVICE_CODENAME" "KERNEL_DIR"**

**-Added "verify_dtb_ziptool".**

### K1.1 STABLE 20231106

**-Improved downloading of the "get_file_name" tools.**

**-Added "verify_dependencies".**

**-Fixed some code bugs.**

### K1.0 STABLE 20231105

**-Initial Script.**

### OLDER VERSIONS DONT HAVE CHANGELOGS BECAUSE WAS "BETAS"
