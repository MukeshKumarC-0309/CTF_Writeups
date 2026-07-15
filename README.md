# CTF Writeups

Personal collection of Capture The Flag challenge writeups spanning web exploitation, binary exploitation, cryptography, forensics, reverse engineering, hardware, and Linux fundamentals — sourced from picoCTF, Root-Me, and CryptoHack.

**Maintained by:** [Cyber Vortex](https://github.com/MukeshKumarC-0309)
**TryHackMe:** [tryhackme.com/p/mukeshkumarc0309](https://tryhackme.com/p/mukeshkumarc0309) — Top 15% globally

---

## 📊 Overview

| Category | Writeups | Challenges Covered |
|---|---|---|
| [Web Exploitation](./Web_Exploitation) | 15 files | SQLi, SSTI, cookie tampering, client-side bypass, directory traversal, GraphQL introspection, broken access control |
| [Forensics](./Forensics) | 15 files | Steganography, PCAP/Wireshark analysis, disk forensics, file carving, polyglot files |
| [Cryptography](./Cryptography) | 28 files | ROT13/Caesar/Vigenère, RSA attacks, hash cracking, XOR ciphers, encoding fundamentals (hex/Base64/ASCII), one-time pads |
| [Linux Basics](./Linux_Basics) | 12 files | Shell fundamentals, Python scripting, encoding, file inspection |
| [Binary Exploitation](./Binary_Exploitation) | 3 files | Buffer overflow, format string vulnerabilities, clutter overflow |
| [Reverse Engineering](./Reverse) | 3 files | GDB debugging, ARM assembly, binary analysis |
| [Hardware](./Hardware) | 2 files | Logic analysis, IQ test-style hardware puzzles |
| **Total** | **78 writeups** | |

---

## 🚩 Challenge Index

### 🌐 Web Exploitation
| Challenge | Writeup |
|---|---|
| Web Gauntlet | [Web_Gauntlet.md](./Web_Exploitation/Web_Gauntlet.md) |
| SSTI1 | [SSTI1.md](./Web_Exploitation/SSTI1.md) |
| Cookies (detailed, curl-based) | [Cookies_2.md](./Web_Exploitation/Cookies_2.md) |
| Cookies | [Cookies.md](./Web_Exploitation/Cookies.md) |
| Don't Use Client-Side | [Dont_use_Client_Side.md](./Web_Exploitation/Dont_use_Client_Side.md) |
| Includes | [Includes.md](./Web_Exploitation/Includes.md) |
| Inspect HTML | [Inspect_HTML.md](./Web_Exploitation/Inspect_HTML.md) |
| Logon | [Logon.md](./Web_Exploitation/Logon.md) |
| SQLite (SQLiLite) | [SQLite.md](./Web_Exploitation/SQLite.md) |
| Search Source | [Search_Source.md](./Web_Exploitation/Search_Source.md) |
| API - Broken Access | [api_brokenaccess.md](./Web_Exploitation/api_brokenaccess.md) |
| Root-Me — Directory Traversal | [directorytraversal.md](./Web_Exploitation/directorytraversal.md) |
| GraphQL Introspection | [graphql_introspection.md](./Web_Exploitation/graphql_introspection.md) |
| Root-Me — HTTP IP Restriction Bypass | [htmlbypass.md](./Web_Exploitation/htmlbypass.md) |
| HTML Source Code | [htmlsourcecode.md](./Web_Exploitation/htmlsourcecode.md) |

### 🕵️ Forensics
| Challenge | Writeup |
|---|---|
| Trivial Flag Transfer Protocol (detailed) | [Trivial_Flag_Transfer_Protocol_2.md](./Forensics/Trivial_Flag_Transfer_Protocol_2.md) |
| Trivial Flag Transfer Protocol | [Trivial_Flag_Transfer_Protocol.md](./Forensics/Trivial_Flag_Transfer_Protocol.md) |
| Tunn3l_V1s10n | [Tunn3l_V1s10n.md](./Forensics/Tunn3l_V1s10n.md) |
| m00nwalk | [m00nwalk.md](./Forensics/m00nwalk.md) |
| Hide and Seek | [Hide_And_Seek.md](./Forensics/Hide_And_Seek.md) |
| Information | [Information.md](./Forensics/Information.md) |
| Tunnel Vision (tunn3l v1s10n) | [Tunnel_Vision.md](./Forensics/Tunnel_Vision.md) |
| Wireshark do dooo | [Wireshark_do_do.md](./Forensics/Wireshark_do_do.md) |
| Corrupted File | [corruptedfile.md](./Forensics/corruptedfile.md) |
| Disk Disk Sleuth | [disk_disk_sleuth.md](./Forensics/disk_disk_sleuth.md) |
| Hidden in Plainsight | [hidden_in_plainsight.md](./Forensics/hidden_in_plainsight.md) |
| Phantom Intruder | [phantom_intruder.md](./Forensics/phantom_intruder.md) |
| Red | [red.md](./Forensics/red.md) |
| Secret of the Polyglot | [secret_of_the_polygot.md](./Forensics/secret_of_the_polygot.md) |
| Very Very Very Hidden | [very_very_very_hidden.md](./Forensics/very_very_very_hidden.md) |

### 🔐 Cryptography
| Challenge | Writeup |
|---|---|
| RSA Oracle | [RSA_Oracle.md](./Cryptography/RSA_Oracle.md) |
| Custom Encryption | [Custom_Encryption.md](./Cryptography/Custom_Encryption.md) |
| miniRSA | [miniRSA.md](./Cryptography/miniRSA.md) |
| 13 (ROT13) | [13.md](./Cryptography/13.md) |
| Caesar | [Caesar.md](./Cryptography/Caesar.md) |
| Even RSA Can Be Broken | [Even_RSA_Can_Be_Broken.md](./Cryptography/Even_RSA_Can_Be_Broken.md) |
| Hashcrack | [Hashcrack.md](./Cryptography/Hashcrack.md) |
| Hide to See | [Hide_to_See.md](./Cryptography/Hide_to_See.md) |
| Mind Your P's and Q's | [Mind_your_Ps_and_Qs.md](./Cryptography/Mind_your_Ps_and_Qs.md) |
| 2Warm | [2Warm.md](./Cryptography/2Warm.md) |
| Glory of the Garden | [Glory_of_the_Garden.md](./Cryptography/Glory_of_the_Garden.md) |
| The Numbers | [The_Numbers.md](./Cryptography/The_Numbers.md) |
| Vigenere | [Vigenere.md](./Cryptography/Vigenere.md) |
| Easy1 | [Easy1.md](./Cryptography/Easy1.md) |
| Finding Flags | [Finding_Flags.md](./Cryptography/Finding_Flags.md) |
| Great Snakes | [Great_Snakes.md](./Cryptography/Great_Snakes.md) |
| ASCII | [ASCII.md](./Cryptography/ASCII.md) |
| Hex | [Hex.md](./Cryptography/Hex.md) |
| Base64 | [Base64.md](./Cryptography/Base64.md) |
| Bytes and Big Integers | [Bytes_and_Big_Integers.md](./Cryptography/Bytes_and_Big_Integers.md) |
| XOR Starter | [XOR_Starter.md](./Cryptography/XOR_Starter.md) |
| XOR Properties | [XOR_Properties.md](./Cryptography/XOR_Properties.md) |
| Favourite byte | [Favourite_byte.md](./Cryptography/Favourite_byte.md) |
| You either know, XOR you don't | [You_either_know_XOR_you_dont.md](./Cryptography/You_either_know_XOR_you_dont.md) |
| New Caesar | [New_Caesar.md](./Cryptography/New_Caesar.md) |
| Factoring | [Factoring.md](./Cryptography/Factoring.md) |
| No Padding, No Problem | [No_Padding_No_Problem.md](./Cryptography/No_Padding_No_Problem.md) |
| rsa-pop-quiz | [rsa-pop-quiz.md](./Cryptography/rsa-pop-quiz.md) |

### 🐧 Linux Basics
| Challenge | Writeup |
|---|---|
| Mod 26 | [Mod_26.md](./Linux_Basics/Mod_26.md) |
| 13 | [13.md](./Linux_Basics/13.md) |
| Interendec | [Interendec.md](./Linux_Basics/Interendec.md) |
| Unminify | [Unminify.md](./Linux_Basics/Unminify.md) |
| Format String 0 | [Format_String_0.md](./Linux_Basics/Format_String_0.md) |
| Fantasy CTF | [Fantasy_CTF.md](./Linux_Basics/Fantasy_CTF.md) |
| Binary Search | [Binary_Search.md](./Linux_Basics/Binary_Search.md) |
| Inspect Me | [Inspect_Me.md](./Linux_Basics/Inspect_Me.md) |
| Python Wrangling | [Python_Wrangling.md](./Linux_Basics/Python_Wrangling.md) |
| String It | [String_It.md](./Linux_Basics/String_It.md) |
| Tab, Tab, Attack | [Tab_Tab_Attack.md](./Linux_Basics/Tab_Tab_Attack.md) |
| Warmed Up | [Warmed_Up.md](./Linux_Basics/Warmed_Up.md) |

### 💥 Binary Exploitation
| Challenge | Writeup |
|---|---|
| Buffer Overflow 0 | [Buffer_Overflow_0.md](./Binary_Exploitation/Buffer_Overflow_0.md) |
| Format String 0 | [Format_String_0.md](./Binary_Exploitation/Format_String_0.md) |
| Clutter Overflow | [Clutter_Overflow.md](./Binary_Exploitation/Clutter_Overflow.md) |

### ⚙️ Reverse Engineering
| Challenge | Writeup |
|---|---|
| GDB Baby Step 1 | [GDB_Baby_Step_1.md](./Reverse/GDB_Baby_Step_1.md) |
| ARMssembly 1 | [ARMssembly_1.md](./Reverse/ARMssembly_1.md) |
| Vault Door 3 | [Vault_Door_3.md](./Reverse/Vault_Door_3.md) |

### 🔧 Hardware
| Challenge | Writeup |
|---|---|
| IQ Test | [IQ_Test.md](./Hardware/IQ_Test.md) |
| I Like Logic | [I_like_logic.md](./Hardware/I_like_logic.md) |

---

## 🛠️ Format

Most writeups follow a step-by-step solution format:
1. **Challenge context** — what's given
2. **Step-by-step solution** — tools and commands used, in order
3. **Flag**

---

## 🔗 Links

- GitHub: [MukeshKumarC-0309](https://github.com/MukeshKumarC-0309)
- TryHackMe: [Profile](https://tryhackme.com/p/mukeshkumarc0309)

---

*Actively updated as new challenges are solved.*
