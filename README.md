# webrtc-setup
```
git clone https://github.com/alexklho/depot_tools.git # download depot_tools
sed -i '0,/^if*/s//DEPOT_TOOLS_UPDATE=0\n&/' depot_tools/update_depot_tools
export PATH=$PATH:depot_tools/

git clone https://github.com/alexklho/webrtc.git # download webrtc source code, or through its mirror
mkdir webrtc
cd webrtc

echo 'solutions = [
  {
    "url": "https://github.com/chromium/chromium.git",
    "managed": False,
    "name": "src",
    "deps_file": "DEPS",
    "custom_deps": {},
    "custom_vars": {},
  },
]' > .gclient

gclient sync
```
