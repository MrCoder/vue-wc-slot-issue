# vue-wc-slot-issue

A sample project to demo the $slots access issue in web component target.

## Steps to reproduce

```bash
yarn install
./node_modules/.bin/vue-cli-service build --target wc --name hello-slot && cp src/demo.html dist/
```

### Expected behaviour

It should prints `1234` (the slot content) 3 times.

### Actual behaviour

`1234` is printed only once (the third log).
