# Reload Client

Client-side script for triggering page and resource reload over WebSockets.

```sh
npm install @m59/reload-client
```

```javascript
import Client from '@m59/reload-client'
Client(reloadServerUrl)
```

## JS API

### Client(reloadServerUrl, options)

Makes a websocket connection to the given url to listen for reload messages.

- `options: object`
  - `quiet: boolean, false` disable logging to console
- **returns**: `object`
  - socket: the WebSocket
  - ...helpers

## WebSocket API

- `string JSON`
  - `type: string` type of reload
    - reload
    - refreshCSS
    - refreshImages
  - `path: string` path to a changed file (for logging)

## Helpers

### refreshCSS()
```
import refreshCSS from '@m59/reload-client/refresh-css'
refreshCSS()
```

### refreshImages()
```
import refreshImages from '@m59/reload-client/refresh-images'
refreshImages()
```
