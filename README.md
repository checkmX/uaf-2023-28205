# CVE-2023-28205: Apple WebKit Use-After-Free Vulnerability

This vulnerability can be exploited through maliciously crafted web content, allowing attackers to execute arbitrary code.

## Description

The code triggers a use-after-free (UAF) vulnerability by delaying the addition of `Map` and `Date` objects, which allows the garbage collector (GC) to free them. This can potentially lead to accessing freed objects, causing memory corruption or enabling exploits.

Thanks to abc for the proof of concept example.