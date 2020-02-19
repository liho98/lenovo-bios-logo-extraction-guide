# ExtractLenovoBiosImages-Guide

This guide attempts to extract Bios Image from a Lenovo Device. (Tested on Lenovo Legion Y530)

# Dependencies

- [7zip](https://www.7-zip.org/)
- [innoextract v1.8](https://github.com/dscharrer/innoextract/releases)
- msvcr120.dll
- [InsydeImageExtractor Initial Release](https://github.com/LongSoft/InsydeImageExtractor/releases)
- [H2OEZE](https://www.win-raid.com/t4639f16-TOOL-H-EZE-Insyde-quot-Easy-BIOS-Editor-quot.html)
- [UEFITool v0.27.0](https://github.com/LongSoft/UEFITool/releases)

# Steps

`
$ innoextract <file>
`

`
$ extractor <infile> <outfile>
`

Use UEFITool to search the desired file type such as jpg/gif/bmp as text with unicode unchecked.

Finally, extract Raw Section body as <filename>.jpg/gif/bmp accordingly.

