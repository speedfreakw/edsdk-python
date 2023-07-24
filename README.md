# edsdk-python
*This is a fork of the [edsdk-python](https://github.com/Jiloc/edsdk-python) Python wrapper by [Jiloc](https://github.com/Jiloc). This fork fixes some issues of the original wrapper with newer Versions of the EDSDK (used Version: 13.17.0).*

Python wrapper for Canon EOS Digital Software Development Kit, aka EDSDK.

Currently, it supports Windows only. But it shouldn't be difficult to adapt it for macOS.

# How to build

## Obtain the EDSDK from Canon

Before you can use this library you need to obtain the EDSDK library from Canon. You can do so via their developers program:

- [Canon Europe](https://www.canon-europe.com/business/imaging-solutions/sdk/)
- [Canon Americas](https://developercommunity.usa.canon.com)
- [Canon Asia](https://asia.canon/en/campaign/developerresources)
- [Canon Oceania](https://www.canon.com.au/support/support-news/support-news/digital-slr-camera-software-developers-kit)
- [Canon China](https://www.canon.com.cn/supports/sdk/index.html)
- [Canon Korea](https://www.canon-ci.co.kr/support/sdk/sdkMain)
- [Canon Japan](https://cweb.canon.jp/eos/info/api-package/)

Once you were granted access - this may take a few days - download the latest version of their library.

## Copy the EDSDK Headers and Libraries

You should now have access to a zip file containing the file you need to build this library.

Unzip the file and copy the following folders inside the `dependencies` folder of this project:
1. `EDSDK` - Containing headers and 32-bit libraries (we only use the headers!)
2. `EDSDK_64` - Containing 64-bit version of the .lib and .dlls (which we do use!)

Your dependencies folder structure should now look like this:

```
dependencies/EDSDK/Header/EDSDK.h
dependencies/EDSDK/Header/EDSDKErrors.h
dependencies/EDSDK/Header/EDSDKTypes.h

dependencies/EDSDK_64/Dll/EDSDK.dll
dependencies/EDSDK_64/Dll/EdsImage.dll

dependencies/EDSDK_64/Library/EDSDK.lib
```

Any additional files aren't needed, but won't hurt either in case you copied the entire folders.

## Build the library

Run:

```bash
pip install .
```
