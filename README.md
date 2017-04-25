# RadioKit JS Toolkit: Broadcast Metadata

High-level JavaScript API for querying metadata of [RadioKit](http://www.radiokit.org)-powered channels.

# Example

In the web browser:

```javascript
var metadataListener = new window.RadioKit.Toolkit.Broadcast.Metadata.MetadataListener("your_access_token", "fd9a7d1c-a387-40a0-b876-2799668d6f9d");

metadataListener.setUpdateCallback(function(metadata) { 
    console.log("Metadata: ", metadata); 
});

metadataListener.setPositionCallback(function(position, duration) { 
    console.log("Position: ", position, "Duration: ", duration); 
});

metadataListener.start()
    .then(() => console.log("Started"))
    .catch((reason) => console.warn("Failed", reason));
```

In the Node.JS:

```javascript
import { MetadataListener } from 'radiokit-toolkit-metadata-broadcast';

var metadataListener = new MetadataListener("your_access_token", "fd9a7d1c-a387-40a0-b876-2799668d6f9d");

metadataListener.setUpdateCallback(function(metadata) { 
    console.log("Metadata: ", metadata); 
});

metadataListener.setPositionCallback(function(position, duration) { 
    console.log("Position: ", position, "Duration: ", duration); 
});

metadataListener.start()
    .then(() => console.log("Started"))
    .catch((reason) => console.warn("Failed", reason));
```

# Development

* Clone the repo
* Enter dir with the project
* Install NPM packages: `npm install` (you can use also `yarn install`)

# Compatibility

* For IE9 and older compatibility use any Promise polyfill.
* For IE8 compatibility use [ES5-shim](https://github.com/es-shims/es5-shim).

# Building browser bundle

* Type `npm run browser`

Browser-compatible version will be located in `dist/browser/`.

# Authors

Marcin Lewandowski <marcin@radiokit.org>

# License

MIT