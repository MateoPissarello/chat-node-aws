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
- [`wscat`] to install run `npm i -g wscat` 

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


## Commands
`Send Message`:
    {"action":"sendMessage","message": (message), "recipientNickname": (nickname)}
    `RecipientNickname`: _Is the nickname of the user that is going to receive the message._
    Example:
    - {"action":"sendMessage","message":"estas aqui? necesito que hagas un chat","recipientNickname":"Mateo"}
    - {"action":"sendMessage","message":"Hola Primo Felipe","recipientNickname":"Felipe"}
`Get Messages`:
    {"action":"getMessages", "targetNickname":"(nickname)","limit":50}
    `targetNickname`:_Is the nickname of the person we want to recover the messages with_
    Example:
        - {"action":"getMessages", "targetNickname":"Mateo","limit":50}
        - {"action":"getMessages", "targetNickname":"Felipe","limit":50}



## Serverless not deploying solution

`If serverless deploy not working do the following` :
1. Delete `.serverless`,`node_modules` and `.build` folders
2. run `npm install -g npm@latest`
3. run `npm i`
4. run `serverless deploy` again and it should work


online
wscat -c wss://e5sqe76r3k.execute-api.us-east-1.amazonaws.com/dev?nickname=Mateo
wscat -c wss://e5sqe76r3k.execute-api.us-east-1.amazonaws.com/dev?nickname=Felipe

Local
serverless offline
wscat -c ws://localhost:3001/dev?nickname=Mateo
wscat -c wss://e5sqe76r3k.execute-api.us-east-1.amazonaws.com/dev?nickname=Mateo

## Licence

MIT.


