# v-for

## Code
```html
<!DOCTYPE html>
<html>
    <head>
        <title>v-for</title>
        <script src="https://unpkg.com/vue"></script>
    </head>
    <body>
        <div id="app">
            <ol>
                <li v-for="todo in todos">
                    {{ todo.text }}
                </li>
            </ol>
        </div>

        <script>
            var app = new Vue({
                el: '#app',
                data: {
                    todos: [
                        { text: 'Learn JavaScript' },
                        { text: 'Learn Vue' },
                        { text: 'Build something awesome' }
                    ]
                }
            })
        </script>
    </body>
</html>
```

## Result
```
1. Learn JavaScript
2. Learn Vue
3. Build something awesome
```

## Note
In the console, enter 
```
app.todos.push({ text: 'New item' }) 
```
You should see a new item appended to the list.