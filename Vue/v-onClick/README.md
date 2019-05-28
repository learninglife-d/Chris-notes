# v-if

## Code
```html
<!DOCTYPE html>
<html>
    <head>
        <title>v-on:click</title>
        <script src="https://unpkg.com/vue"></script>
    </head>
    <body>
        <div id="app">
            <p>{{ message }}</p>
            <button v-on:click="reverseMessage">Reverse Message</button>
        </div>

        <script>
            var app = new Vue({
                el: '#app',
                data: {
                    message: 'Hello Vue.js!'
                },
                methods: {
                    reverseMessage: function () {
                        this.message = this.message.split('').reverse().join('')
                    }
                }
            })
        </script>
    </body>
</html>
```

## Result After click button
```
!sj.euV olleH
```