# material-snackbar-supplier

Implement with **new react context api** that help you use [material-ui](https://material-ui.com//) SnackBar anywhere in your react-components with no pain

### Installation
Available as npm package.
```bash
npm install --save material-snackbar-supplier

-- or

yarn add material-snackbar-supplier

```

### Usage
Wrap your root component with SnackBarSupplier and applying any options based on [Snackbar](https://material-ui.com/api/snackbar/).
Then use provided HOC anywhere you need handle Snackbar.make sure you have installed @material-ui/core and @material-ui/icons

```js
import { SnackBarSupplier } from 'material-snackbar-supplier';

<SnackBarSupplier settings={{ autoHideDuration: 1500 }}>
  <App />
</SnackBarSupplier>
```


```js
import { withSnackBar } from 'material-snackbar-supplier';

class App {
  componentDidMount () {
    this.props.message({
      message: 'Hello World!',
      variant: 'success',
    });
  }
}

export default withSnackBar(App)
```

### Settings
All of settings for `SnackBarSupplier` is based on material-ui SnackBar API Props Doc. For more information read [this link](https://material-ui.com/api/snackbar).
