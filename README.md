# CVE-2023-28205: Apple WebKit Use-After-Free Vulnerability

This vulnerability can be exploited through maliciously crafted web content, allowing attackers to execute arbitrary code.

## Description

The code triggers a use-after-free (UAF) vulnerability by delaying the addition of `Map` and `Date` objects, which allows the garbage collector (GC) to free them. This can potentially lead to accessing freed objects, causing memory corruption or enabling exploits.

## References

- [WebKit Commit c9880de4a28b9a64a5e1d0513dc245d61a2e6ddb](https://github.com/WebKit/WebKit/commit/c9880de4a28b9a64a5e1d0513dc245d61a2e6ddb)
 
CVE-2023-28205: Clément Lecigne of Google's Threat Analysis Group and Donncha Ó Cearbhaill of Amnesty International’s Security Lab

Thanks to abc for the proof of concept example.