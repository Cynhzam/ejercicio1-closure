# ejercicio1-closure

En el código inicial se puede observar que existe un closure (función hijo dentro de una función padre). La función hijo es una función anónima y no cuenta con un parámetro, es por eso que al momento de dar los valores a las funciones, la única que los toma es la función padre, ya que es la única que cuenta con un parámetro definido;
```javascript
var num2 = 0;

function suma(num1) {
    return function() {
        return num1 + num2;
    }
} 
var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado
var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.
```

En la solución planteada observamos que a la función que inicialmente era anónima se le ha agregado un parámetro (num2), para que esta pueda tomar los valores asignados y de esta manera, el código nos de el resultado esperado.
```javascript
var num2 = 0;

function suma(num1) {
    return function(num2) {
        return num1 + num2;
    }
} 
var suma2 = suma(2);
console.log(suma2(5));
var suma12 = suma(12);
console.log(suma12(76))
```
