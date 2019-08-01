# Stair Speedtest Reborn
**Proxy performance batch tester based on Shadowsocks(R) and V2Ray**  
<img alt="GitHub tag (latest SemVer)" src="https://img.shields.io/github/tag/tindy2013/stairspeedtest-reborn.svg">
<img alt="GitHub release" src="https://img.shields.io/github/release/tindy2013/stairspeedtest-reborn.svg">
<img src="https://img.shields.io/github/license/tindy2013/stairspeedtest-reborn.svg">
  
## Intro
This is a C++ remake version of the original [Stair Speedtest](https://github.com/tindy2013/stairspeedtest) script. Despite its similarity to the script verion, this remake version works much more effectively, with faster node parsing, result picture rendering and even cross-platform support.  
  
## Installation  
### Prebuilt release  
Go to [Release Page](https://github.com/tindy2013/stairspeedtest-reborn).  
### Build
In general, you need the following build dependencies:  
* curl
* openssl
* PNGwriter
* libpng16
* freetype
* zlib
* yaml-cpp
  
On non-Windows platforms, you also need to have the following clients installed:  
* shadowsocks-libev
* shadowsocksr-libev ('ss-local' installed as the name 'ssr-local')
* v2ray-core
  
You can also use the auto configure script (experimental):
```bash
# On most Linux platforms  
./config.sh  

# On MacOS:  
./config.macos.sh
```
  
After installing all these dependencies, you can use the quick build script:  
```bash
# On Windows
build.bat  
  
# On most Linux platforms  
./build.sh  

# On MacOS:  
./build.macos.sh  
```
## Usage
* Run "stairspeedtest" for CLI speedtest, run "webgui" for Web GUI speedtest. **Currently Web GUI only supports on Windows.**
* Results for subscribe link tests will be saved to a log file in "results" folder.
* The result will be exported into a PNG file with the result log. An interactive HTML file with test results will also be generated with the PNG file. In this HTML, you can sort by name, ping, packet loss or speed.
* You can customize some settings by editing "pref.ini".
## Compatibility
Tested platforms: 
  
* Windows 10 1803 x64, Windows Server 2008 R2
* Ubuntu 18.10
* MacOS 10.14.3 Mojave
  
Supported proxy types:  

 |Proxy|Client|Config Parser|
 |:-:|:-:|:-:|
 |SSR|ShadowsocksR-libev|ShadowsocksR|
 |SS|Shadowsocks-libev|Shadowsocks \| ShadowsocksD \| Clash \| Surge (experimental) |
 |V2RAY|V2Ray-Core|V2RayN \| Quantumult \| Clash
## Known Bugs
You tell me?
## TODO
* Web GUI support on all platform