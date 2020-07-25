# delete2system

1.删除C:\ProgramData\Microsoft\Windows\WER子文件（A little known NTFS detail is that the rename operation can be used to move files and folders anywhere on the volume. A rename operation requires the `DELETE` permission on the origin and the `FILE_ADD_FILE`/`FILE_ADD_SUBDIRECTORY` permission on the destination folder. ）

2.删除C:\ProgramData\Microsoft\Windows\WER（If the vulnerability only enables deletion of a file because `NtCreateFile` is called with `FILE_NON_DIRECTORY_FILE`, that restriction can be bypassed by making it open the path `C:\ProgramData\Microsoft\Windows\WER::$INDEX_ALLOCATION`.）

3.执行Delete.exe "whoami" malicious.dll

![Image](https://github.com/Nan3r/delete2system/raw/master/123.PNG?raw=true)



# reference

https://github.com/DimopoulosElias/Primitives (原项目)

https://secret.club/2020/04/23/directory-deletion-shell.html
