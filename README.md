<p align="center">
  <a href="https://github.com/xavivzla" rel="noopener" target="_blank"><img width="150" src="https://raw.githubusercontent.com/xavivzla/Funnel-React/dev/logo.png" alt="Funnel-react logo"><span style="font-size:40px">2</span></a></p>
</p>
<h1></h1>

<div align="center">

[![NPM](https://img.shields.io/npm/v/funnel-react.svg)](https://www.npmjs.com/package/funnel-react) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

</div>

<p align="center">
  <a href="https://github.com/xavivzla" rel="noopener" target="_blank"><img width="600" src="https://github.com/whiteChess/Funnel-React/blob/master/react%20funnel%20example.png?raw=true" alt="Funnel-react logo"></a></p>
</p>


## Note
This package is forked from this [repo](https://github.com/xavivzla/Funnel-React). What is new in this package.
- Drop off perecentage between funnel stages.
- React callbacks to customize the rendering for labels, values, precentages and drop off precentages.
- Percentages now displayed nicely inside the funnel itself.

## Install

```bash
npm install --save funnel-react-2
```

> or

```bash
yarn add funnel-react-2
```

## Usage

```jsx

import { Funnel } from 'funnel-react-2';

```

##Simple example

```jsx

<Funnel
    height={252}
    colors={{
      graph: [ '#1890FF', '#BAE7FF' ],
      percent: 'red',
      label: 'yellow',
      value: 'orange'
    }}
    displayPercent={true}
    valueKey='quantity'
    width={800}
    data={data}
    renderLabel={(index, value) => {
      return (
        <span>
          {value}
        </span>
      );
    }}
    renderPercentage={(index, value) => {
      return (
        <span>
          {value}
        </span>
      );
    }}
    renderDropOffPercentage={(index, value) => {
        return (
          <span>{value} %</span>
        );
      }
    }}
    renderValue={(index, value) => {
      return (
        <span>
          {value}
        </span>
      );
    }}
  />

```

| props                   | Type            | Default Value          | Options      |
| ----------------------- |:--------------: | :--------------------  | :----------: |
| labelKey                | string          |                        |              |
| colors                  | object          |                        |              |
| valueKey                | string          |                        |              |
| width                   | number          | container width        |              |
| displayPercent          | boolean         | false                  | false / true |
| data                    | array           |                        |              |
| renderLabel             | function        | null                   |              |
| renderValue             | function        | null                   |              |
| renderPercentage        | function        | null                   |              |
| renderDropOffPercentage | function        | null                   |              |
## License

MIT © [xavivzla](https://github.com/xavivzla), [whitechess](https://github.com/whitechess)