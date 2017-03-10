# weex-driver

> Weex driver for Rax.

## Install

```bash
$ npm install --save weex-driver
```

## Use

```jsx
import {createElement, Component, render} from 'rax';
import weexDriver from 'weex-driver';
import {isWeex} from 'universal-env';

class Example extends Component {
  render() {
    return (
      <div>
        <img width="560" height="560" src="https://img.alicdn.com/tps/TB1z.55OFXXXXcLXXXXXXXXXXXX-560-560.jpg" />
      </div>
    );
  }
}

render(<Example />, null, {
  driver: isWeex ? weexDriver : null
});
```

## Support elements

### div

### p

### img

- src
- width
- height
- placeholder: weex only
- resize: weex only

### a

- href

### video

- src
- controls
- autoplay: not sure
- play-status: weex only

### textarea

- placeholder
- disabled
- autofocus
- rows
- children: as value