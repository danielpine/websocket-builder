# websocket-builder
websocket builder

```javascript
Vue.prototype.$webSocket = new WebSocketApi.WebSocketBuilder(
        `ws://${window.location.host}/socket`
      )
        .onMessage(function (event) {
          console.log(this)
          mes = JSON.parse(event.data)
          Vue.prototype.$notify({
            title: mes.message,
            message: mes.data,
            type: 'success',
            duration: 2000
          })
        })
        .build()
```
