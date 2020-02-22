# ExtractLenovoBiosImages-Guide

This guide attempts to extract a Bios image from a Lenovo device. (Tested successfully on Lenovo Legion Y530)

Thanks to [@tyrng](https://github.com/tyrng) for contributing this guide.

# Dependencies

- [7zip](https://www.7-zip.org/) - A tool for opening and extracting Bios.exe as archive and file.
- [innoextract v1.8](https://github.com/dscharrer/innoextract/releases) - A tool to unpack installer (eg. Bios.exe) created by Inno Setup
- [msvcr120.dll](https://www.dll-files.com/msvcr120.dll.html) - A Dynamic-link library (DLL) required for InsydeImageExtractor
- [InsydeImageExtractor Initial Release](https://github.com/LongSoft/InsydeImageExtractor/releases) - A utility for extracting UEFI image from InsydeFlash executable file
- ~[H2OEZE](https://www.win-raid.com/t4639f16-TOOL-H-EZE-Insyde-quot-Easy-BIOS-Editor-quot.html) - A tool made by Insyde or called "Easy BIOS Editor" for viewing or editing the Bios logo~
- [UEFITool v0.27.0](https://github.com/LongSoft/UEFITool/releases) - A UEFI firmware image viewer and editor

# Steps

1. Create a new folder and copy your Bios.exe, innoextract, msvcr120.dll, InsydeImageExtractor into it.
2. Open cmd and change the current directory to the folder you created. (eg. `> cd Desktop/newfolder`)
3. Run the command `> innoextract Bios.exe`
4. Open the newly generated Bios.exe with 7zip as the archive and extract the files from the archive.
5. Run the command `> extractor Bios.fd out.fd`
6. Use UEFITool to search for the required file type, such as jpg (JFIF) / gif (GIF89a) / bmp (BM) as unchecked unicode text. For .pcx files, use the hexadecimal 0A 05 01 08.
7. Finally, extract the Raw Section body as <filename> .jpg / gif / bmp.

(Note: All dependencies and Bios.exe should be extracted and placed in the same directory)

