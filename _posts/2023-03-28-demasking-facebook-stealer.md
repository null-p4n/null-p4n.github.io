---
layout: post
title: "Protect Your Privacy: Beware of Malware That Steals Chrome Cookies and Passwords."
date: '2023-03-28 04:23:56 +0300'
---

Protect Your Privacy: Beware of Malware That Steals Chrome Cookies and Passwords.
----------------------------------------------------------------------------------

Recently, there has been an increase in the deployment of malware that steals Chrome cookies and passwords. One such malware was discovered as an ad for "ChatGPT-4" hosted on a platform called Trello. Trello is a project management tool that allows users to organize their projects into boards.
![2023-03-24_14-54](https://user-images.githubusercontent.com/60641238/228127422-0ba55182-a513-48c4-aa34-4d00ac4d05cb.png)

The malware was identified as an advanced persistent threat (APT) that utilized a stealth virus. A stealth virus is a type of virus that can hide in legitimate files, partitions, or boot sectors of a computer without alerting antivirus software or notifying the user of its presence. Once injected into a computer, the virus enables attackers to operate and gain control over parts or the entire system.

The malware was contained within a .zip archive that was over 800MB in size, making it difficult for VirusTotal to scan. As a result, the malware was extracted using BINWALK, which allowed for the identification of various files within the archive. These included a Microsoft Installer (.msi) file and several executable files (PE32) for MS Windows, DLL files (PE32), and Google Chrome extensions.

> _1459AA20C76F434484A8E6A4A4C42E68: PE32 executable (console) Intel 80386, for MS Windows
> _696444530633E0C7F5E58F662DB245E0: XML 1.0 document, Unicode text, UTF-8 (with BOM) text, with CRLF line terminators
> _7534306A76264E47A88B44FAFA7104BE: PE32 executable (console) Intel 80386, for MS Windows
> _85A9757E47DF5E4CBF720E6FB79023F0: PE32 executable (DLL) (console) Intel 80386 Mono/.Net assembly, for MS Windows
> _97886BFEF5084241A53F3E7E27FD9AE7: Google Chrome extension, version 3
> _9ED461AA2787417691A4F0A5502B3F89: MS Windows icon resource - 1 icon, -128x-128, 32 bits/pixel
> _B98F4865EDEBFDF745615EDDD4A5DA57: PE32 executable (DLL) (console) Intel 80386 Mono/.Net assembly, for MS Windows
> _B9D798B2ED327EEED5D9B0F4CA663E21: PE32 executable (DLL) (console) Intel 80386 Mono/.Net assembly, for MS Windows
> _C2F4039A4D613C9AF994E35FA7703362: PE32 executable (DLL) (console) Intel 80386 Mono/.Net assembly, for MS Windows
> _C7C28AB0B611136A1ED66106AC4F829C: PE32 executable (DLL) (console) Intel 80386 Mono/.Net assembly, for MS Windows
> C9E00:                             directory
> C9E00.cab:                         Microsoft Cabinet archive data, 23912569 bytes, 14 files, at 0x5c "_1459AA20C76F434484A8E6A4A4C42E68", iFolder 0x1 
> "_696444530633E0C7F5E58F662DB245E0", 7 cffolders, number 1, 390 datablocks, 0x1 compression
> _CD19606A3DDEC13CA069CFDAC9580EA9: PE32 executable (DLL) (console) Intel 80386 Mono/.Net assembly, for MS Windows
> _E43ECE427A504682B136311D646C0924: PE32 executable (GUI) Intel 80386 Mono/.Net assembly, for MS Windows
> _F0114D5337D54282AF05C021CAA515EF: PE32 executable (console) Intel 80386, for MS Windows
> _F724B0C83029CDC0DCCD854CD4EC4CAE: PE32 executable (GUI) Intel 80386 Mono/.Net assembly, for MS Windows
> a371d82808938f6a119aa0dd493058ad07be59c0d0e4e2da7152a5c0d9271cb6  _1459AA20C76F434484A8E6A4A4C42E68
> 47e5a0f101af4151d7f13d2d6bfa9b847d5b5e4a98d1f4674b7c015772746cdf  _696444530633E0C7F5E58F662DB245E0
> cd36202f90480ecacddad56ac479a3e9631ff71e9b28d4c018c57408c17641ac  _7534306A76264E47A88B44FAFA7104BE
> cb1b1ac1c1a435f7ea7ee75914aa7bb1324bfafb7910d8c814db62a77b09ffa0  _85A9757E47DF5E4CBF720E6FB79023F0
> 30dac370102f05adcb1ed94e199d67e254f66cda80774fc80aaa8601735e477b  _97886BFEF5084241A53F3E7E27FD9AE7
> 142569a9d48e7384794aba2b4d5db3ff4c4370460ab133b692168c60964f39ad  _9ED461AA2787417691A4F0A5502B3F89
> e9c71ebf653159ee260640f152f677b33d30796307803fb5340f522abff17691  _B98F4865EDEBFDF745615EDDD4A5DA57
> f3d2ebb39d2edc3cce98299c724c5eff0b7a151c5d0857dd3f35ad0ff48fbe53  _B9D798B2ED327EEED5D9B0F4CA663E21
> a90bda198d65c72d7526ba0483b5b23de961a1152cdda8c9feb695cd19d8b6d1  _C2F4039A4D613C9AF994E35FA7703362
> bab8785a6656f202b4153c887f5f19fa0075afafe728c24af50bd24342e76f75  _C7C28AB0B611136A1ED66106AC4F829C
> sha256sum: C9E00: Is a directory
> 7af5a3edcaddfaad5905c8a0f574e0b66653fd1f5e6ae158f6078f1f839d5936  C9E00.cab
> 06f159db143a3eaf9d20321535428325c9b157cecb4999fa567c7019f1258a8e  _CD19606A3DDEC13CA069CFDAC9580EA9
> b73d06e9586ae2ee193f045f0b437c93cf1525a780f3599565611e16de82d775  _E43ECE427A504682B136311D646C0924
> 78ee9334b57d75f3365b6ba570e5a55369728dd0376d26b0c92bd63c6537e216  _F0114D5337D54282AF05C021CAA515EF

Further analysis of the malware revealed the presence of various matching signatures, indicating the malware's potential to steal Chrome cookies and passwords. The malware was also found to contain a Microsoft Cabinet archive (.cab) file containing 14 files and 23912569 bytes of data.

Given the serious threat posed by this type of malware, it is critical for users to be vigilant and take proactive steps to protect their privacy. This includes avoiding suspicious links and downloads, using antivirus software, and regularly updating passwords.

[virus total](https://www.virustotal.com/gui/file/b73d06e9586ae2ee193f045f0b437c93cf1525a780f3599565611e16de82d775)

[intezer.com](https://analyze.intezer.com/analyses/115627b7-293d-42f8-9aa4-0557cc7b9531)
[filescan.io](https://www.filescan.io/uploads/641da6019c109cf74b2f2b00/reports/d2899a08-75da-449b-8512-822c350b1613) 

![image](https://user-images.githubusercontent.com/60641238/228135263-9c512ae6-9fee-4dd8-8087-c9a514a787b1.png) .
 
 Here's my [sample](https://www.dropbox.com/s/zmxib4rj6wzsd6a/ChatGPT_fake_ad_camp.zip?dl=0) used.
 
