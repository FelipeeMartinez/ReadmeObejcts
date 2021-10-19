# TAREA OBJETOS  

## PARTICIPANTE
1. Juan Felipe Martinez ..........

##  #1 #1.1 #1.2
Crear un metodo constructor llamada persona. Sus atributos son: nombre, edad y cedula. Construye los siguientes métodos para la clase:

![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/11112.png)

## #2 #2.1 #2.2 #2.3
Crea un metodo constructor llamado cuenta que tendrá los siguientes atributos: titular (que es nombre de la persona) y cantidad. El titular será obligatorio y la cantidad es opcional. Construye los siguientes métodos para el metodo:
2.1 mostrar(): Muestra los datos de la cuenta. 2.2 ingresar(cantidad): se ingresa una cantidad a la cuenta, si la cantidad introducida es negativa, no se hará nada. 2.3 retirar(cantidad): se retira una cantidad a la cuenta. La cuenta puede estar en números rojos.

```javascript
function crear_cuenta(titular_ingresado, cantidad_ingresada ) {
    this.nombre_titular = titular_ingresado;
    this.cantidad = cantidad_ingresada;
}
var cuenta1 = new crear_cuenta("Pedro",500);

crear_cuenta.prototype.mostrar = function(){
    return ("Nombre: "+ this.nombre_titular + " Cantidad:" + this.cantidad);
}
crear_cuenta.prototype.ingresar = function(cantidad){
    if(cantidad <= 0){
        return cantidad = this.cantidad + 0;
    }else {
        return cantidad = this.cantidad + cantidad;
    }
}
crear_cuenta.prototype.retirar = function(cantidad){
    var resta = this.cantidad - cantidad;
    if(resta <= 0) {
        return `La cuenta puede estar en numeros rojos: $`+ resta; 
    }else {
        return  resta;
    }
}
```
![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/2212223.png)

## #3 #3.1 #3.2 #3.3 #3.4
Crear un metodo constructor llamado formulas. Construye los siguiente metodos para la clase:
3.1 sumar(entero, entero) 3.2 fibonacci(cantidad) a partir de una entero sacar los numeros 3.3 operacion_modulo(cantidad) a partir de una cantidad mostrar cuales dan residuo 0 3.4 primos(cantidad) a partir de una cantidad mostrar cuales son numeros primos

```javascript
var formulas = {
    sumar : function(valor_a, valor_b){
        var suma = valor_a + valor_b;
        return suma;
    },
    fibonacci : function(cantidad){
        var a=0;
        var b=1;
        for(i=0; i<cantidad;i++){
        var numeroTemporal=a;
        a=b;
        b=numeroTemporal+b;
    }
    return b;
    },
    operacion_modulo:function(cantidad){
        for (let i = 2; i <= cantidad; i++) { 

  for (let j = 2; j < i; j++) { 
    if (i % j == 0) continue nextPrime; 
  }

  alert( i ); 
}
    }

}
```
![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/331323334.png)







