# cURL 7.42.1 build (using OpenSSL 1.0.2u) that runs on unmodified Windows 98

* If you're a developer who wants to create .NET programs for Windows 98, you do not need the cURL build in Releases. Instead, add all the files in the "LibCurl.NET + libraries" folder (located in this repository's source) to your output directory, and add LibCurl.NET as a reference. If you want an example on how to use LibCurl.NET, check out the SkyBridge.cs file included (it doesn't compile on its own, and is part of a different project, but the code inside it will show you how to use the library)

* If you want to link other Windows 98 programs to OpenSSL, check out this project's sister repository openssl-windows98.

**IMPORTANT! IMPORTANT! IMPORTANT:** You need to link to a cert file (get it at "https://curl.se/ca/cacert.pem") with environment variables in autoexec.bat or in session, OR by using the flag "--cacert C:\your\path\here\cacert.pem".
This is not a Windows 98 issue of outdated certificates, this applies on any platform where you install cURL (even Windows 11, if you don't have cURL installed by default). cURL does not use the Windows certificate store
for any version of cURL or Windows. Do thos before raising an issue when your connection is closed with "certificate store not found".

This build does not support zlib or SSH. May add in future, but this was only really meant for me to get a cURL build that could access the Bluesky APIs. Now that
I have that, the continued adding of features to this build is of low priority.

This version of cURL has identical syntax to the newer versions, and uses OpenSSL 1.0.2u (the latest possible for this version, while this version of cURL
is the earliest possible cURL version that supports 1.0.2). **What this means is that you have TLS 1.2 support and a modern SSL protocol that should give
you access to virtually all websites without throwing up nasty unsupported security protocol errors.**

In short, this is the only way to access all of the modern Web on unmodified Windows 98.

I looked for a prebuilt binary for this all over the internet, couldn't find one, so made my own. Should save you from having to install VC++2005 to compile it. Yes, I downloaded Visual Studio 2005 just for compiling openssl/cURL.

Note: OpenSSL 1.0.2 reached end-of-life at the end of 2019. It can be vulnerable to attacks in the future, although it is highly unlikely that you will be
targeted or any data intercepted even if somebody tried. Nevertheless, exersize caution when sending login details for websites through OpenSSL.
