# Serverless - AWS Node.js Typescript

Serverless Framework template for zero-config TypeScript support.

## Features

Thanks to [`serverless-typescript`](https://github.com/prisma-labs/serverless-plugin-typescript) plugin:

- Zero-config: Works out of the box without the need to install any other compiler or plugins
- Supports ES2015 syntax + features (`export`, `import`, `async`, `await`, `Promise`, ...)
- Supports `sls package`, `sls deploy` and `sls deploy function`
- Supports `sls invoke local` + `--watch` mode
- Integrates nicely with [`serverless-offline`](https://github.com/dherault/serverless-offline)

## Prerequisites

- [`serverless-framework`](https://github.com/serverless/serverless)
- [`node.js`](https://nodejs.org)

## Usage

To create new serverless AWS TypeScript project using this template run:

```bash
serverless create \
--template-url https://github.com/ttarnowski/serverless-aws-nodejs-typescript/tree/main \
--path myServiceName
```

where `myServiceName` should be replaced with the name of your choice.

Then change directory to the newly created one:

```
cd myServiceName
```

And run:

```
npm install
```

or:

```
yarn install
```

## Licence

MIT.

Send Message:
{"action":"sendMessage","message":"estas aqui? necesito que hagas un chat","recipientNickname":"Mateo"}
{"action":"sendMessage","message":"Hola Primo Felipe","recipientNickname":"Felipe"}

Get Messages:
{"action":"getMessages", "targetNickname":"Mateo","limit":50}

serverless deploy function --function websocketHandler


install nvm
https://github.com/coreybutler/nvm-windows/releases
nvm install 14
nvm use 14
nvm list

2:37:29

npm install --global windows-build-tools

npm install --cache
npm install -g npm@latest
npm install -g serverless
npm install -g wscat
npm install -g serverless-offline


online
wscat -c wss://e5sqe76r3k.execute-api.us-east-1.amazonaws.com/dev?nickname=Mateo
wscat -c wss://e5sqe76r3k.execute-api.us-east-1.amazonaws.com/dev?nickname=Felipe

Local
serverless offline
wscat -c ws://localhost:3001/dev?nickname=Mateo
wscat -c wss://e5sqe76r3k.execute-api.us-east-1.amazonaws.com/dev?nickname=Mateo



messageId 02704c38-b6b4-4cfd-becf-6952aff60f1c

02704c38-b6b4-4cfd-becf-6952aff60f1c
1702938474458
Hola Primo mateo
Felipe#Mateo
Felipe
