# v-model

## Code
```html
<!DOCTYPE html>
<html>
    <head>
        <title>v-model</title>
        <script src="https://unpkg.com/vue"></script>
    </head>
    <body>
        <div id="app">
            <p>{{ message }}</p>
            <input v-model="message">
        </div>

        <script>
            var app = new Vue({
                el: '#app',
                data: {
                    message: 'Hello Vue.js!'
                }
            })
        </script>
    </body>
</html>
```