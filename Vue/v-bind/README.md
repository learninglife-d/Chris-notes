# v-bind

```html
<!DOCTYPE html>
<html>
    <head>
        <title>v-bind</title>
        <script src="https://unpkg.com/vue"></script>
    </head>
    <body>
        <div id="app">
            <span v-bind:title="message">
                Hover your mouse over me for a few seconds
                to see my dynamically bound title!
            </span>
        </div>

        <script>
            var app = new Vue({
                el: '#app',
                data: {
                    message: 'Hello Vue!'
                }
            })
        </script>
    </body>
</html>
```