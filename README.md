Minimal code to reproduce the bug described in [nodejs-depd #48](https://github.com/dougwilson/nodejs-depd/pull/48):

    nvm use 14.19.0
    npm run build
    nvm use 5.12.0 32
    npm start

Tested under Windows 10 using [nvm-windows](https://github.com/coreybutler/nvm-windows/)
