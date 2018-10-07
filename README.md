# Redux Saga for Network Status

A simple `redux-saga` solution for Network Status using the `NetInfo` api of `react-native`. This module provides a "saga" which can then be used for modeling asynchronous behavior.


## Getting Started

- [Installation](#installation)
- [Basic Usage](#basic-usage)
- [Advanced Usage](#advanced-usage)
- [Properties](#properties)
- [Contribution](#contribution)
- [Questions](#questions)

### Installation

```bash
$ npm i react-native-network-status-saga --save
```

### Basic Usage
In your app's main saga, import the module and Spawn/fork it.
```
import networkStatusSaga from "react-native-network-status-saga";
    
...
yield spawn(networkStatusSaga);
```

### Advanced Usage
Using your custom action name
```
yield spawn(networkStatusSaga, {
  syncAction: 'CONNECTION_STATUS'
});
```

Using delay by either action or interval
```
yield spawn(networkStatusSaga, {
  delayByInterval: 10 * 60,
  delayByAction: "APP_STARTED"
});
```

### Properties
| Prop  | Default  | Type | Description |
| :------------ |:---------------:| :---------------:| :-----|
| syncAction | `CONNECTION_STATUS` | `string` | Custom action name to sync the network change values |
| delayByInterval | `0` | `number` | Custom Delay Interval (in seconds)) |
| delayByAction | `null` | `string` | Custom Delay Action |


## Contribution

- [@pritishvaidya](mailto:pritishvaidya94@gmail.com) The main author.

## Questions

Feel free to [contact me](mailto:pritishvaidya94@gmail.co) or [create an issue](https://github.com/pritishvaidya/react-native-network-status-saga/issues/new)
