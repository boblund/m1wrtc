# m1wrtc
wrtc.node for m1 and install instructions

As of 2/25/2022 npm wrtc does not support the Apple M1 processor. These instructions detail how to install an M1 build of wrtc.node. The basics of this process are taken from https://github.com/node-webrtc/node-webrtc/issues/698. This repo just simplifies things a bit.

## Install x64 wrtc

In your project directory install the Intel version of wrtc:

```npm i wrtc --target_arch=x64```

## Patch in the M1 build of wrtc

Replace the Intel build of wrtc.node in your project directory with the M1 version (wrtc-v0.5.0-napi-v3-darwin-arm64.tar.gz taken from [here](https://github.com/corwin-of-amber/node-webrtc/releases))

```cp m1wrtc/wrtc.node node_modules/wrtc/build/Release/wrtc.node```
