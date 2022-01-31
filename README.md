TypeScript Webpack5 Keep Async Await Demo
=======================================

关键点在于`tsconfig.json`中，要把`target`设为`ES2017`或以后的，否则tsc会生成`__awaiter`这样的转换代码

```
npm install
npm run demo
```

然后

```
cat ./dist/bundle.js
```

内容如下：

```
(() => {
    "use strict";
    function util1() {
        return "util1";
    }
    const utilStr = util1();
    console.log(utilStr);
})();
```

看起来`util2`的确是被去掉了。
