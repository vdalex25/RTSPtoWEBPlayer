# RTSPtoWEBPlayer
 external video player for projects:
- [RTSPtoWeb](https://github.com/deepch/RTSPtoWeb)
- [RTSPtoWebRTC](https://github.com/deepch/RTSPtoWebRTC)
- [RTSPtoWSMP4f](https://github.com/deepch/RTSPtoWSMP4f)
- [RTSPtoImage](https://github.com/deepch/RTSPtoImage)
- [RTSPtoHLS](https://github.com/deepch/RTSPtoHLS)
- [RTSPtoHLSLL](https://github.com/deepch/RTSPtoHLSLL)

there is no GUI in this project, you can add your own GUI

[demo page](http://htmlpreview.github.io/?https://github.com/vdalex25/rtsp-to-web-player/blob/main/index.html)
## Install

```bash
git clone https://github.com/vdalex25/RTSPtoWEBPlayer.git

cd RTSPtoWEBPlayer

npm install

npm run build
```
it's created compiled file `dist/RTSPtoWEBPlayer.js`
## Usage
Add script to your page
```html
<script src="dist/RTSPtoWEBPlayer.js"></script>
```
Create new player
```js
const options={
    parentElement: document.getElementById('player')
};
const player=new RTSPtoWEBPlayer(options);
player.load('ws://localhost:8083/stream/517fe9dbf4b244aaa0330cf582de9932/channel/0/mse?uuid=517fe9dbf4b244aaa0330cf582de9932&channel=0');
```

## Options
```js
options={
        parentElement:null,
        source:null,
        controls:true,
        muted:true,
        autoplay:true,
        loop:false,
        hlsjsconfig: {

        }
    }
```

#### `parentElement`
default: null

HTMLElement
#### `source`
link to mediasource. requires explicit protocol http/https or ws/wss
#### `controls`
default: true

show/hide notive video control
#### `muted`
default: true

#### `autoplay`
default: true

#### `loop`
default: false

#### `hlsjsconfig`
default: empty;

full list of config  you can see on [API dicumentation hls.js](https://github.com/video-dev/hls.js/blob/master/docs/API.md#fine-tuning)
## Methods

