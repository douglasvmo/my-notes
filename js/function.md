# Funções

## composição de funções
Agrupando funções middlewares, semelhante ao framework Express.js.

```js
function compose(...fns) {
    return function next(value) {
        const func = fns.shift();
        if(typeof func === 'function'){
            func(value, next)
        }
        return value
    }
}
```

```js script
function middleware(value, next){
    value += 1;
    next(value)
}
```
executando a composição, e passando para a função composta o *significado da vida, do universo e tudo mais* como parametro

```js
const myComposedFunction = compose(middleware, middleware, ...);

const init = 42;
myComposedFunction(init)
```