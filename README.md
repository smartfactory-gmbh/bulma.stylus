# Bulma Stylus
> Pure Stylus implementation of [Bulma.css](https://github.com/jgthms/bulma)

#### Notice! This package is used to integrate Bulma with Stylus, it does NOT includes builded css files.

![Bulma-Stylus banner](docs/images/bulma-stylus-banner.png)

## Install
_This package version is synchronous with Bulma, every difference between the same version of Bulma
will be logged in [Changelog](CHANGELOG.md)._

### NPM
```sh
npm install @shirohana/bulma-stylus
```

__or__

### Yarn
```sh
yarn add @shirohana/bulma-stylus
```

## Links
- [📚 Offical documentation](https://bulma.io/documentation/overview/start)
- [📜 Changelog](CHANGELOG.md)

## Difference between Bulma
- Support 4k container (Disable: `$4k-enabled = false`)
- All possible floating numbers are round to 4 digits after the period

#### New Feature
- Dynamic `rem` for better user experience on high-resolution screens

  [![high resolution comparation](docs/images/responsiveness-compare.png)](https://raw.githubusercontent.com/shirohana/bulma.stylus/dev/docs/images/responsiveness-compare.png)

  If enabled, the page will be scale in ratio when device width exceeds `$body-auto-scale` (default: `$fullhd`).

  You can try a higher value and find out the best in your situation like `$body-auto-scale = $fullhd + 20*16px`.

  Set `$body-auto-scale` to any falsy value to disable this feature.

#### Internal
- Use `em/rem` instead `px` in every elements, components and helpers
- Replace `lighten()` function with `sass-lighten()` which implements sass-like `lighten`
- Replace `darken()` function with `sass-darken()` which implements sass-like `darken`
- Remove `powerNumber()` function (Use Stylus [`exponent-operator`][stylus-operator-exponent] instead)
- Remove `colorLuminance()` function (Use Stylus built-in function [`luminosity()`][stylus-bifs-luminosity] instead)

[stylus-operator-exponent]: http://stylus-lang.com/docs/operators.html#exponent-
[stylus-bifs-luminosity]: http://stylus-lang.com/docs/bifs.html#luminositycolor

## Inherited copyright and license
© 2018 Jeremy Thomas. Code released under [the MIT license](https://github.com/jgthms/bulma/blob/master/LICENSE).
