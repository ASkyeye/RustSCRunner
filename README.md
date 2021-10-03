# RustSCRunner

Shellcode Runner/Injector in Rust using NTDLL functions directly with the ntapi Library.

Surprisingly this is my first ever Rust project that I spent my entire Sunday on and it was harder than I thought because I'm not used to the Rust Syntax or the language. There appear to be a lack of resources for this project and recently I saw trickster0 post something on Twitter which inspireded me to checkout something other than my favourites languages C++/C#. I've mostly been using DInvoke and after customizing it got 0 detection rate.

## 0 Detections on Virus Total (Will change after making public)

![Detections](Detections.png)

https://www.virustotal.com/gui/file/34d2ad3a0c5d603df03ddca8cdaff47545ab427aa9c32dd60e15764b3615abab?nocache=1


![Detections](PoC.png)


## References and Credits

* https://mr.un1k0d3r.com/ (Including the people in the VIP discord Mr.Un1k0d3r, Waldo-IRC, Ditto, nixfreax)
* https://discord.com/invite/rust-lang-community
* https://github.com/trickster0/OffensiveRust (Motivated by this repository)
* https://github.com/byt3bl33d3r/OffensiveNim
* https://twitter.com/_RastaMouse and https://twitter.com/Jean_Maes_1994