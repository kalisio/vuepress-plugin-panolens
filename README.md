# vuepress-plugin-panolens

[![Latest Release](https://img.shields.io/github/v/tag/kalisio/vuepress-plugin-panolens?sort=semver&label=latest)](https://github.com/kalisio/vuepress-plugin-panolens/releases)

This is a simple [VuePress](https://vuepress.vuejs.org/) plugin that provides a global component wrapping [Panolens](https://pchen66.github.io/Panolens/), _a Javascript Panorama Viewer_.

## Installation

You can install it with

```bash
yarn add -D vuepress-plugin-panolens
```

And then you just need to register the plugin in your `.vuepress/config.js`:

```js
module.exports = {
    // ...
    plugins: [
        'vuepress-plugin-panolens'
    ]
    // ...
}
```

## Usage

The recommended usage is to place your **panolens** declaration as an HTML element:

```md
<panolens  />
```

The tag handles the following attributes:

| Attribute | Description |
| --- | --- |
| `source` | the url to the panorama image. |
| `css-style` | The style to apply to the HTML container. The default value is `width: 100%; height: 50vh` |

## Contributing

Found a bug ? Missing a Feature ? Want to contribute ? check out our [contribution guidelines](./CONTRIBUTING.md) for details

## Authors

This project is sponsored by 

[![Kalisio](https://s3.eu-central-1.amazonaws.com/kalisioscope/kalisio/kalisio-logo-black-256x84.png)](https://kalisio.com)

## License

This project is licensed under the MIT License - see the [license file](./LICENSE) for details



