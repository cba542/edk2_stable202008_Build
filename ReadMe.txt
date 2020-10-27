edk2_stable202008
1.
target.txt 
ACTIVE_PLATFORM       = OvmfPkg/OvmfPkgX64.dsc
TARGET_ARCH           = X64

TOOL_CHAIN_TAG        = VS2015x86 
根據VS版本

2.
C:\Users\User\Downloads\brotli-master.zip\brotli-master\c 
資料放到
C:\BIOS\edk2_stable202008\MdeModulePkg\Library\BrotliCustomDecompressLib\brotli\c

3.
C:\Users\User\Downloads\openssl-1.1.1h.tar\openssl-1.1.1h\openssl-1.1.1h
把裡面的檔案放到
C:\BIOS\edk2_stable202008\CryptoPkg\Library\OpensslLib\openssl


4
build 完成之後的
C:\BIOS\edk2_stable202008\Build\OvmfIa32\DEBUG_VS2015x86\FV\OVMF.fd
放到
C:\Program Files (x86)\qemu

配合指令
qemu-system-x86_64.exe -bios "OVMF.fd" -hda fat:rw:C:\BIOS\Temp -net none -net none
另外可以放入C:\BIOS\Temp\Startup.nsh
開機之後快速切到fs0: 目錄
fs0: