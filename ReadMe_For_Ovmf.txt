0.
Un-zip edk2_stable202008

1.
Put files
brotli-master\c
into the path
C:\BIOS\edk2_stable202008\MdeModulePkg\Library\BrotliCustomDecompressLib\brotli\c

2.
put files
openssl-1.1.1h
intoe the path
C:\BIOS\edk2_stable202008\CryptoPkg\Library\OpensslLib\openssl

3.
Switch folder to C:\BIOS\edk2_stable202008
Execute
edksetup.bat
edksetup.bat Rebuild
build -p OvmfPkg\OvmfPkgX64.dsc -a X64 -t VS2015x86

4.
build finish
C:\BIOS\edk2_stable202008\Build\OvmfIa32\DEBUG_VS2015x86\FV\OVMF.fd
OVMF.fd use for qemu bios boot

5.
put QVMF.fd to the
C:\Program Files (x86)\qemu

Execute
qemu-system-x86_64.exe -bios "OVMF.fd" -hda fat:rw:C:\BIOS\Temp -net none -net none

This cmd will sync the files under C:\BIOS\Temp\ 
