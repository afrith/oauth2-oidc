# Development

## Setup

Assuming you've got a NodeJS environment ready:

```
npm install
```

## Run Specs

```
npm test
```

## Run Specs Continuously

```
npm run watch
```

## Debug Specs

Run the specs with `--debug-brk` to make node wait for the debugger to attach:

```
node --debug-brk ./node_modules/jasmine/bin/jasmine.js
```

Run `node-inspector`:

```
./node_modules/.bin/node-inspector
```

... (does not work at the moment... why?)

# Testing

The example provider can be run with a REPL:

```
WITH_REPL=1 node examples/provider.js
```

Within the REPL, the following will be in the context: `provider`, `ontology`, `server`

This gives access to anything persisted like this:

```
ontology.collections.client.findOne({ id: 1 }).then((c) => { console.log('c', c) })
```
