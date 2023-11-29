# SubZero Proxy

A sophisticated web proxy that allows you to browse the web privately and bypass any website blocker. This is a completely open source project so y'all can skid off it.



# Update Logs

[11/29/23] Fixed errors when trying to navigate to a new webpage.

[11/29/23] Revived Project

[11/29/23] Open sourced

More soon...

# Configuration
Configure proxy for both client-hooking & service worker in `uv.config.js`
```javascript
self.__uv$config = {
    bare: '/bare/',
    prefix: '/service/',
    encodeUrl: Ultraviolet.codec.xor.encode,
    decodeUrl: Ultraviolet.codec.xor.decode,
    handler: '/uv.handler.js',
    bundle: '/uv.bundle.js',
    config: '/uv.config.js',
};
```


# Example Usage
```javascript
importScripts('/PATHTOSCRIPTS/uv.sw.js');

const sw = new UVServiceWorker();

self.addEventListener('fetch', event =>
    event.respondWith(
        sw.fetch(event)
    )
);
```

# Support

I will be updating this repo with new features every time that I get enough stars. Below you can see a feature list corresponding with the # of stars.

[5 Stars] - New UI

[10 Stars] - Disguiser

[15 Stars] - Improved speeds

# Credits

Original source - Ultraviolet

Fixing, adding, and upgrading - [Payson](https://github.com/paysonism)