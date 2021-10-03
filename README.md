# RustSCRunner

Shellcode Runner/Injector in Rust using NTDLL functions directly with the ntapi Library.

Surprisingly this is my first ever Rust project that I spent my entire Sunday on, which I thought I had wasted but it turned out to be a success. Coding this in Rust was harder than I thought because I'm not used to Rust Syntax or the language and IMHO there appears to be a lack of resources for these shellcode runners. Recently I saw @trickster012 post https://github.com/trickster0/OffensiveRust on Twitter that inspired me to work on this other than my favourites languages C/C++/C#. I usually use a private customised version of DInvoke made by @Jean_Maes_1994, which uses SYSCALLs which also has a 0 detection rate.

I hope that this project inspires more people to make some cool things in Rust or even GO to explore the red team evasion techniques.


## XOR Encoded Shellcode

Please note that the shellcode used is a msfvenom payload that is XOR encoded using the following loop in C#:

```csharp
for (int i = 0; i < buf.Length; i++)
{
    encoded[i] = (byte)((uint)buf[i] ^ 0xBE); //change this byte this for different XOR encoding.
}
```

The shellcode is then decoded in the Rust shellcode runner/injector using the following:
```rust
let mut shellcode : Vec<u8> = Vec::with_capacity(buf.len());
for x in &buf {
    shellcode.push(*x ^ 0xBE); //change this byte for different XOR encoding.
}
```

Make sure to comment out the appropriate line if you don't want to use any encoding and if you do then make sure you encode your shellcode with the appropriate byte.

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