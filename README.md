# chslang
Scripting language made for dynamic configurations

## basic Hello World
```js
import {chslang} from "./chslang.js"

const config = chslang(`
set author to from chslang!
print Hello World $(author)
`)
```

## more complicated Hello World
```js
import {chslang} from "./chslang.js"

const config = chslang(`
set first to Hello
set second to , world
set message to $(first) $(second) !

print our message is $(message)
`)

console.log(config)
```

## functions
```js
const config = chslang(`
function sayhello
  print Hi from the function!
  print arguments given: $(this)

sayhello Lorem ipsum der aben
`)
```

## connectivity with javascript
```js
const config = chslang(`
raw 8+8
print $(return)
// "return" variable is the "raw" function's output
`)
```

## lets get even further
```js
const config = chslang(`
js console.log("Hello, World from javascript!")
js console.log("js Command executes the given code in normal javascript")
`)
```
