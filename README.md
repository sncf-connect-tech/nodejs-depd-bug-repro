Minimal code to reproduce the bug described in [nodejs-depd #48](https://github.com/dougwilson/nodejs-depd/pull/48):

    nvm use 14.19.0
    npm run build
    nvm use 5.12.0 32
    npm start

    TypeError: callSite.getFileName is not a function
        at callSiteLocation (C:\nodejs-depd-bug-repro\dist\bundle.js:452:3231)
        at depd (C:\nodejs-depd-bug-repro\dist\bundle.js:452:1375)
        at node_modulesBodyParserIndexJs (C:\nodejs-depd-bug-repro\dist\bundle.js:508:172)
        at __require (C:\nodejs-depd-bug-repro\dist\bundle.js:1:8616)
        at Object.<anonymous> (C:\nodejs-depd-bug-repro\dist\bundle.js:509:68)

Tested under Windows 10 using [nvm-windows](https://github.com/coreybutler/nvm-windows/)
