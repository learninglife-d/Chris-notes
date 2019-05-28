# vue component example 1

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
                <todo-item
                    v-for="item in groceryList"
                    v-bind:todo="item"
                    v-bind:key="item.id"
                ></todo-item>
            </ol>
        </div>

        <script>
            Vue.component('todo-item', {
                props: ['todo'],
                template: '<li>{{ todo.text }}</li>'
            })

            var app = new Vue({
                el: '#app',
                data: {
                    groceryList: [
                        { id: 0, text: 'Vegetables' },
                        { id: 1, text: 'Cheese' },
                        { id: 2, text: 'Whatever else humans are supposed to eat' }
                    ]
                }
            })
        </script>
    </body>
</html>
```

## Result
```
1. Vegetables
2. Cheese
3. Whatever else humans are supposed to eat
```