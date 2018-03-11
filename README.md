# fa-bundle

This repo exists to show a tree shaking bug in @fortawesome/fontawesome-free-solid using the destructuring import syntax.

# Reproducing the bug
After clone this repo you should run the following commands:

    yarn install
    yarn build

The webpack-bundle-analyzer opens a tab in http://127.0.0.1:8888/ and you can see the whole font-awesome icons library inside the `main.bundle.js` because our code use just ONE icon in `App.js`.
