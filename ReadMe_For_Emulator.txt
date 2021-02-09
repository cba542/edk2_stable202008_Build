0.
Un-zip edk2_stable202008

1.
Execute
edksetup.bat
edksetup.bat Rebuild
build -p EmulatorPkg\EmulatorPkg.dsc -a X64 -t VS2015x86

2.
build finish then execute
\Build\EmulatorX64\DEBUG_VS2015x86\X64\WinHost.exe
(Need "Run as administrator" for Visual Studio debug)
