# cURL 7.42.1 build (using OpenSSL 1.0.2u) that runs on unmodified Windows 98

If you want to link other Windows 98 programs to OpenSSL, check out thhis project's sister repository openssl-windows98.

This version of cURL has identical syntax to the newer versions, and uses OpenSSL 1.0.2u (the latest possible for this version, while this version of cURL
is the earliest possible cURL version that supports 1.0.2). **What this means is that you have TLS 1.2 support and a modern SSL protocol that should give
you access to virtually all websites without throwing up nasty unsupported security protocol errors.**

In short, this is the only way to access all of the modern Web on unmodified Windows 98.

I looked for a prebuilt binary for this all over the internet, couldn't find one, so made my own. Should save you from having to install VC++2005 to compile it. Yes, I downloaded Visual Studio 2005 just for compiling openssl/cURL.

Note: OpenSSL 1.0.2 reached end-of-life at the end of 2019. It can be vulnerable to attacks in the future, although it is highly unlikely that you will be
targeted or any data intercepted even if somebody tried. Nevertheless, exersize caution when sending login details for websites through OpenSSL.
