### Kyliz Script

**A shell-based script that allows you to download/compile auto/manual env an Android kernel and also create a flashable zip via recovery.**

### Avaible languages

**-en_US es_CO pt_BR.**

### Features

**-Check updates system, Languages system.**

**-You can manually configure the script to your liking "config.sh".**

**-You can download toolchain only setting config.sh git/wget.**

**-You can create a custom flashable kernel with this script.** [AnyKernel3](https://github.com/ZyCromerZ/AnyKernel3)

**-You configure it to your liking and you can compile a kernel with just one. [command](https://github.com/thisfeeling/kyliz_script#execution-kyliz-shell-script)**

### Releases

*  [Stable](https://github.com/thisfeeling/kyliz_script/releases)

### Script Configuration Example config.sh

```bash
#!/bin/bash
# CONFIG FILE 
# Copyright @thisfeeling
# OPTIONS
LANGUAGE="en_US" # en_US or es_CO or pt_BR
CREATE_FLASHEABLE_ZIP=true
DOWNLOAD_TOOLS=false
CLONE_KERNEL=true
COMPILE_KERNEL=true
# CONFIG AUTO/MANUAL
ENVIROMENT_AUTO=false
# KERNEL CONFIG CLONE_KERNEL=true
KERNEL_TREE_BRANCH="11.0"
KERNEL_TREE="https://github.com/thisfeeling/kernel_motorola_msm8953"
KERNEL_DEVICE_CODENAME="ali"
KERNEL_DEFCONFIG="ali_defconfig"
KERNEL_STATUS="UNOFFICIAL"
KERNEL_TYPE="BETA"
KERNEL_ZIP_NAME="Perf"
ARCHITECTURE="arm64" #arm64/arm
DT_EXT="dtb" # dtb/dts
MAKE_PREFERRED_OUT=mrproper # mrproper/clean
# ENVIROMENT TOOLS In case ENVIROMENT_AUTO=true DOWNLOAD_TOOLS=true
# CLANG CONFIG
CLANG_TREE="https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+archive/f8e856556909898bd35ee8eae829437721b5a3db/clang-r353983e.tar.gz"
CLANG_TREE_BRANCH=""
CLANG_TREE_VERSION="clang-r353983e"
CLANG_TREE_VERSION_DIR="clang-9"
# ARM LINUX ANDROIDEABI CONFIG
ARM_LINUX_ANDROIDEABI_TREE="https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/arm/arm-linux-androideabi-4.9/+archive/refs/heads/pie-release.tar.gz"
ARM_LINUX_ANDROIDEABI_TREE_BRANCH=""
ARM_LINUX_ANDROIDEABI_TREE_VERSION="arm-linux-androideabi-"
# AARCH64 LINUX ANDROID CONFIG
AARCH64_LINUX_ANDROID_TREE="https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+archive/refs/heads/pie-release.tar.gz"
AARCH64_LINUX_ANDROID_TREE_BRANCH=""
AARCH64_LINUX_ANDROID_TREE_VERSION="aarch64-linux-android-"
# AARCH64 LINUX GNU CONFIG
AARCH64_LINUX_GNU_TREE="https://github.com/theradcolor/aarch64-linux-gnu"
AARCH64_LINUX_GNU_TREE_BRANCH="stable-gcc"
AARCH64_LINUX_GNU_TREE_VERSION="aarch64-linux-gnu-"
# MANUAL ENVIROMENT TOOLS ENVIROMENT_AUTO=false DOWNLOAD_TOOLS=false CLONE_KERNEL=false
MANUAL_KERNEL_DEVICE_CODENAME_DIR="/home/thisfeeling/kyliz/ali"
MANUAL_CONFIG_CROSS_COMPILE_ARM32="/home/thisfeeling/kyliz/prebuilts/arm-linux-androideabi-/bin/arm-linux-androideabi-"
MANUAL_CONFIG_CROSS_COMPILE="/home/thisfeeling/kyliz/prebuilts/aarch64-linux-android-/bin/aarch64-linux-android-"
MANUAL_CONFIG_CLANG_TRIPLE="/home/thisfeeling/kyliz/prebuilts/aarch64-linux-gnu-/bin/aarch64-linux-gnu-"
MANUAL_CONFIG_CLANG="/home/thisfeeling/kyliz/prebuilts/clang-r353983e/bin/clang-9"
```

### Configure File "anykernel.sh" Example

```bash
## AnyKernel setup
# begin properties
properties() { '
kernel.string=Moto G(6) Custom Kernel by thisfeeling
do.devicecheck=1
do.modules=0
do.cleanup=1
do.cleanuponabort=0
device.name1=ali
'; } # end properties

# shell variables
block=/dev/block/bootdevice/by-name/boot;
is_slot_device=auto;
```
### Necessary Files

**AnyKernel3 - Dtbtool**

### Execution kyliz shell script
```bash
$ sudo chmod +x setup.sh && sudo ./setup.sh 
```
### All Changelog

### K1.3.2 STABLE 20231202

**-Fixed error code in "automatic_process", "manual_process".**

**-Fixed unused "preparation_kernel".**

### K1.3.1 STABLE 20231202

**-Added "process_compile_kernel", "COMPILE_KERNEL".**

**-Fixed some code bug in "automatic_process".**

### K1.3.0 STABLE 20231201

**-Added "process_clone_kernel", "CLONE_KERNEL".**

**-Added system languages "config_languages", "LANGUAGE"(LANGUAGES: en_US es_CO pt_BR).**

**-Deleted "show_status", "show_status_color".**

**-Deleted "process_build_kernel", "COMPILE_KERNEL".**

### K1.2.9 STABLE 20231201

**-Added "config_colors".**

**-Improvements "show_status", "show_status_color".**

**-Improvements "config_enviroment", Added check updates system.**

**-Deleted "process_configuration_preset", "process_clone_kernel", and was remplazed by "selected_process", "manual_process", "automatic_process", "MANUAL_KERNEL_DEVICE_CODENAME_DIR".**

**-Deleted "process_temp_files", "clean_temp_files", "DELETE_TEMP_FILES".**

**-Deleted "validate_environment_variables".**

**-Deleted "verify_output_files", and be put in "compile_kernel".**

**-Deleted "process_show_system_info", "SYSTEM_INFO".**

**-Deleted "check_os", "check_root", and was remplazed by "check".**

**-Deleted "sudo" in some code, to avoid errors.**

**-Deleted "validate_dependencies", "install_missing_dependencies".**

**-Obsolete code was deleted.**

**-Fixed some code bugs.**

### K1.2.8 STABLE 20231127

**-Now you can manually configure the script to your liking "MANUAL_ENVIROMENT", "manual_configure_build".**

**-Added config_enviroment file "config.sh".**

**-Added "check_root".**

**-Added "process_show_system_info" and "SYSTEM_INFO".**

**-Added "process_verify_dtb_ziptool".**

**-Added "process_only_download_kernel_tools".**

**-Improvements to "download_tools", "download_with_wget", "clone_with_git", automated wget & git clone and improvements in config.sh .**

**-Deleted function "decision_create_zip", and was remplazed by "process_zip_decision" and "CREATE_FLASHEABLE_ZIP".**

**-Deleted function "decision_clean_temp_files", and was remplazed by "process_temp_files_decision" and "DELETE_TEMP_FILES".**

**-Deleted function "decision_compile_kernel", and was remplazed by "process_build_kernel" and "BUILD_KERNEL".**

**-Obsolete code was deleted.**

**-Fixed some code bugs.**

### K1.2.7 STABLE 20231123

**-Added "show_system_info".**

**-Added "decision_clean_temp_files".**

**-Deleted variable "CLANG_VERSION_STRING", and was remplazed by "CLANG_TOOLCHAIN_VERSION".**

**-Deleted function "abort_if_error", and was remplazed by "show_status".**

**-Fixed Improvements to "install_dependencies".**

**-Obsolete code was deleted.**

**-Fixed some code bugs.**

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
