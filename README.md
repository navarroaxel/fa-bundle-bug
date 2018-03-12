# fa-bundle-bug

This repo exists to show a tree shaking bug in `@fortawesome/fontawesome-free-solid` using the destructuring import syntax.

## Related issues

https://github.com/FortAwesome/react-fontawesome/issues/70

https://github.com/webpack/webpack/issues/6724

## Reproducing the bug
After clone this repo you should run the following commands:

    yarn install
    yarn build

The webpack-bundle-analyzer opens a tab in http://127.0.0.1:8888/ and you can see the whole font-awesome icons library inside the `main.bundle.js` because our code use just ONE icon in `App.js`.

## 2nd Test with sideEffects off

Edit `src/fa-bundle/node_modules/@fortawesome/fontawesome-free-solid/package.json` adding "sideEffects": false and run `yarn build` again.
