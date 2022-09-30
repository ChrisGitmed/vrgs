# dark-args
A Node.js library to assist in parsing opstrings. Built because I was tired of typing two lines to access args with a popular npm package. dark-args only needs one.

---
### Install
```
yarn add dark-args
```
### Usage
###### In Node.js
```
// example.js

import { argv } from 'dark-args';

const example = async (run, name, id) => {
  if (run) console.log('Run!');
  if (name === 'Chris') console.log('Hello Chris');
  if (id < 20) console.log('Less than 20');
};

(async () => {
  await example(argv.run, argv.name, argv.id);
  process.exit(0);
})();
```
###### In terminal
```
λ node example.js --run  --name=Chris  --id=10
  Run!
  Hello Chris
  Less than 20

```
