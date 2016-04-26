---
layout: default
title: Test de la coloration syntaxique
date: 2016-04-26
---
```js
    var http = sourceToParse.url.search(/^(http:\/\/){1}/);
    var https = sourceToParse.url.search(/^(https:\/\/){1}/);
    sourceToParse.url = sourceToParse.url.replace(/www.|http:\/\/|https:\/\//gi, "");
    var afterSlash = sourceToParse.url.search(/\/.*$/);
    // console.log(sourceToParse.url);
    if (afterSlash != -1) {
        var afterSlash = afterSlash - sourceToParse.url.length;
        sourceToParse.url = sourceToParse.url.slice(0, afterSlash);
        console.log(sourceToParse.url);
    }

    sourceToParse.url = "www." + sourceToParse.url;

    if (http != -1) {
        sourceToParse.url = "http://" + sourceToParse.url;
    }else if (https != -1) {
        sourceToParse.url = "https://" + sourceToParse.url;
    }else {
        sourceToParse.url = "http://" + sourceToParse.url;
    }

    sourceToParse.parsedSource += "[" + sourceToParse.url + "]";
```
