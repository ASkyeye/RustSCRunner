# RustSCRunner

Shellcode Runner/Injector in Rust using NTDLL functions directly with the ntapi Library.

Surprisingly this is my first ever Rust project that I spent my entire Sunday on, which I thought I had wasted and turns out to be a success. It was harder than I thought because I'm not used to Rust Syntax or the language. There appears to be a lack of resources IMHO for these shellcode runners and recently I saw trickster0 post something on Twitter that inspired me to checkout something other than my favourites languages C++/C#. I've mostly been using DInvoke and after customizing, it got a 0 detection rate.

## 0 Detections on Virus Total (Will change after making public)

![Detections](https://github.com/memN0ps/RustSCRunner/blob/main/Detections.PNG)

https://www.virustotal.com/gui/file/34d2ad3a0c5d603df03ddca8cdaff47545ab427aa9c32dd60e15764b3615abab?nocache=1


![PoC](https://github.com/memN0ps/RustSCRunner/blob/main/PoC.PNG)


## References and Credits

* https://mr.un1k0d3r.com/ (Including the people in the VIP discord Mr.Un1k0d3r, Waldo-IRC, Ditto, nixfreax)
* https://discord.com/invite/rust-lang-community
* https://github.com/trickster0/OffensiveRust (Motivated by this repository)
* https://github.com/byt3bl33d3r/OffensiveNim
* https://twitter.com/_RastaMouse and https://twitter.com/Jean_Maes_1994
* https://docs.rs/winapi/0.3.9/winapi/
* https://www.rust-lang.org/learn