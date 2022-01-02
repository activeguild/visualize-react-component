<h1 align="center">visualize-react-component ⚡ Welcome 😀</h1>

<p align="left">
  <a href="https://github.com/actions/setup-node"><img alt="GitHub Actions status" src="https://github.com/activeguild/vite-plugin-sass-dts/workflows/automatic%20release/badge.svg" style="max-width:100%;"></a>
</p>

## visualize-react-component

Analyze the component tree of react and display it in a diagram.

![スクリーンショット 2022-01-02 3 53 37](https://user-images.githubusercontent.com/39351982/147858017-5545345b-ab53-42d0-92a9-41b7d72c7a54.png)

## Motivation

It plays an auxiliary role in visualizing the component design during implementation and activating smooth discussions.

It will lead to shrinking the cost of development.

## Install

```bash
npm i -D visualize-react-component
```

## Usage

By specifying the React root file and the component files, it will parse them and output the `stats.html` file.

```
npm run virot ./src/main.tsx
```

## Config

The following options can be set in the configuration file.
Prepare a `virot.config.js` file with the following properties.

| Property | Type  | Description                                |
| -------- | ----- | ------------------------------------------ |
| alias    | Array | Specify multiple aliases for entry points. |

`alias Property`
| Property | Type | Description |
| -------- | ----- | ----------- |
| find | String | Entry point alias. |
| replacement | String | Resolve aliases by specifying absolute paths. |

#### Sample

```js
import path from 'path'

module.exports = {
  alias: [
    {
      find: '@',
      replacement: path.resolve('./src'),
    },
  ],
}
```

## Principles of conduct

Please see [the principles of conduct](https://github.com/activeguild/visualize-react-component/blob/master/.github/CONTRIBUTING.md) when building a site.

## License

This library is licensed under the [MIT license](https://github.com/activeguild/visualize-react-component/blob/master/LICENSE).
