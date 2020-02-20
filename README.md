# ExtractLenovoBiosImages-Guide

This guide attempts to extract Bios Image from a Lenovo Device. (Tested on Lenovo Legion Y530)

Thanks to [@tyrng](https://github.com/tyrng) for contributing this guide.

# Dependencies

- [7zip](https://www.7-zip.org/)
- [innoextract v1.8](https://github.com/dscharrer/innoextract/releases)
- [msvcr120.dll](https://www.dll-files.com/msvcr120.dll.html)
- [InsydeImageExtractor Initial Release](https://github.com/LongSoft/InsydeImageExtractor/releases)
- [H2OEZE](https://www.win-raid.com/t4639f16-TOOL-H-EZE-Insyde-quot-Easy-BIOS-Editor-quot.html)
- [UEFITool v0.27.0](https://github.com/LongSoft/UEFITool/releases)

# Steps

`
$ innoextract <bios.exe>
`

Open the resulting .exe with 7zip as archive, then extract all files from the archive.

`
$ extractor <bios.fd> <out.fd>
`

Use UEFITool to search the desired file type such as jpg(JFIF)/gif(GIF89a)/bmp(BM) as text with unicode unchecked. For .pcx files use hexadecimal 0A 05 01 08.

Finally, extract Raw Section body as <filename>.jpg/gif/bmp accordingly.

