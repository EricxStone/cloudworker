# @ericxstone/cloudworker

This package is a fork from [cloudworker](https://github.com/dollarshaveclub/cloudworker) created by Dollar Shave Club. I have further added the feature to support scheduled event from cloudflare worker.

NPM: https://www.npmjs.com/package/@ericxstone/cloudworker

## Installing

Install via NPM:
```sh
npm install -g @ericxstone/cloudworker
```
## Package Usage

```
const Cloudworker = require('@ericxstone/cloudworker')

const simpleScript = `addEventListener('scheduled', event => {
  event.waitUntil(() => {});
})`

const cw = new Cloudworker(simpleScript)
cw.triggerCronJob.then((res) => {
  console.log("Schedule is triggered")
})
```

For other features and description, please refer to the [original repository](https://github.com/dollarshaveclub/cloudworker).

## License
MIT
