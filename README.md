# React Deck Swiper

[![NPM](https://img.shields.io/npm/v/react-deck-swiper.svg)](https://www.npmjs.com/package/react-deck-swiper) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

This is a simple React module that introduces a tinder-like swipeable component.

![Preview](https://media.giphy.com/media/US0kvefmSueoiIpZwU/giphy.gif)

## Preview

Online example [here](https://jungsoft.github.io/react-deck-swiper/).

## Install

You can use `yarn` or `npm`.


### Yarn

```bash
yarn add react-deck-swiper
```

### npm

```bash
npm install --save react-deck-swiper
```

## Usage

```
import * as React from 'react';

import { Swipeable, direction } from 'react-deck-swiper';

const Component = () => {
  const handleOnSwipe = (swipeDirection) => {
    if (swipeDirection === direction.RIGHT) {
      // handle right swipe
      return;
    }

    if (swipeDirection === direction.LEFT) {
      // handle left swipe
      return;
    }
  }

  return (
    <Swipeable onSwipe={handleOnSwipe}>
      <div className="card">
        Your card content here
      </div>
    </Swipeable>
  );
};

export default Component;
```

## Props

Name | Type | Required | Default value | Description
:--- | :--- | :--- | :--- | :---
`children` | `React.ReactChild` | _required_ | - | component that will be swipeable
`onBeforeSwipe` | `(forceSwipe, cancelSwipe, direction) => void` | _optional_ | `undefined` | callback executed on swipe start
`onSwipe` | `(direction) => void` | _optional_ | `undefined` | callback executed on swipe end
`onAfterSwipe` | `() => void` | _optional_ | `undefined` | callback executed right after onSwipe end
`onOpacityChange` | `(opacity) => void` | _optional_ | `undefined` | callback executed when the card opacity changes on swipe
`wrapperHeight` | `string` | _optional_ | `100%` | `height` prop for swipeable wrapper
`wrapperWidth` | `string` | _optional_ | `100%` | `width` prop for swipeable wrapper
`swipeThreshold` | `number` | _optional_ | `120` | offset in px swiped to consider as swipe
`fadeThreshold` | `number` | _optional_ | `40` | offset when opacity fade should start
`renderButtons` | `({right, left}) => React.Component` | _optional_ | `undefined` | function to render buttons to force swipes

## Contributing

Pull requests are welcome! If you have any feedback, issue or suggestion, feel free to open [a new issue](https://github.com/jungsoft/react-deck-swiper/issues/new) so we can talk about it 💬.

## License

MIT

## Special Thanks

Thanks to [goncy](https://github.com/goncy/) for the first version of this lib.

Made with ❤️ by [Pedro Bini](https://github.com/pedro-lb/) @ [Jungsoft](https://jungsoft.io/).
