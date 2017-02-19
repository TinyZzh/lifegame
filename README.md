# lifegame(生命游戏) 
[![Build Status](https://travis-ci.org/moyunchen/lifegame.svg?branch=master)](https://travis-ci.org/moyunchen/lifegame) [![Coveage](https://img.shields.io/codecov/c/github/moyunchen/lifegame/master.svg)](https://codecov.io/gh/moyunchen/lifegame) [![npm version](https://img.shields.io/npm/v/lifegame.svg)](https://www.npmjs.com/package/lifegame) ![download](https://img.shields.io/npm/dt/lifegame.svg) ![license](https://img.shields.io/npm/l/express.svg)

每个格子的生死遵循下面的原则：

1. 如果一个细胞周围有3个细胞为生（一个细胞周围共有8个细胞），则该细胞为生（即该细胞若原先为死，则转为生，若原先为生，则保持不变） 。
    
2. 如果一个细胞周围有2个细胞为生，则该细胞的生死状态保持不变；
    
3. 在其它情况下，该细胞为死（即该细胞若原先为生，则转为死，若原先为死，则保持不变）

用法:

> npm install lifegame

``` javascript
const {nextMap} = require('lifegame')
const map = [[1,1,1],[1,1,1],[1,1,1]]
const newmap = nextMap(map)
console.log(newmap) // newmap tobe [[1,0,1],[0,0,0],[1,0,1]]
```


``` javascript
const {nextMap} = require('lifegame')
const newmap = initMap(3,4)
console.log(newmap) // newmap tobe 3*4 map
```