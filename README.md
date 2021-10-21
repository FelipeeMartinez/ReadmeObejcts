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

## #4 #4.1 #4.2 #4.3
4.1 calcularIMC(): calculara si la persona esta en su peso ideal (peso en kg/(altura^2 en m)), si esta fórmula devuelve un valor menor que 20, la función devuelve un -1, si devuelve un número entre 20 y 25 (incluidos), significa que esta por debajo de su peso ideal la función devuelve un 0 y si devuelve un valor mayor que 25 significa que tiene sobrepeso, la función devuelve un 1. Te recomiendo que uses constantes para devolver estos valores. 4.2 esMayorDeEdad(): indica si es mayor de edad, devuelve un booleano. 4.3 comprobarSexo(char sexo): comprueba que el sexo introducido es correcto. Si no es correcto, sera H.

```javascript
var persona = {
  nombre: "Maria",
  edad: "17",
  dni: "115214",
  sexo: "M",
  peso: 60,//en kilogramos
  altura: 1.60,//en metros
  calcularMC: function(){
    var peso = this.peso;
    var altura = this.altura;
    var peso_ideal = (peso/(altura*altura));
    if(peso_ideal > 25) {
      return 1;
    } else if(peso_ideal < 20) {
      return -1
    }else if(peso_ideal > 20 && peso_ideal < 25)
    return 0;
  },
  esMayorDeEdad : function() {
    if(this.edad >= 18) {
      return true;
    } else {
      return false;
    }
  },
  comprobarSexo : function(sexo) {
    if(sexo == this.sexo) {
      return "Sexo correcto";
    } else {
      return "Sexo = H"
    }
  }
}
```
![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/4414243.png)

## #5 #5.1 #5.2 #5.3
Crear un metodo constructor llamado contraseña. Sus atributos longitud y contraseña Construye los siguiente metodos para la clase:
5.1 esFuerte(): devuelve un booleano si es fuerte o no, para que sea fuerte debe tener mas de 2 mayúsculas, mas de 1 minúscula y mas de 5 números. 5.2 generarPassword(): genera la contraseña del objeto con la longitud que tenga. 5.3 seguridadPaswword(); indicar si la contraseña es debil contiene entre 1 a 6 caracteres (caracteres numeros y letras), media (7 a 10 caracteres numeros y letras) o fuerte (11 a 20 caracteres letras y caracteres especiales

```javascript
var contrasennia = {
  longitud : 12,
  contrasennia : "Contraseña12",

  esFuerte : function() {
    var contadorMayus = 0;
    var contadorMinus = 0;
    var contadorNums = 0;
    var arr = this.contrasennia.split(" ");
    for(i=0; i < arr.length; i++) {
      if(arr[i] = arr[i].toUpperCase) {
        contadorMayus++;
      } else if(arr[i] = arr[i].toLowerCase) {
        contadorMinus++;
      } else if(arr[i] >= 0) {
        contadorNums++;
      }
    }
    if(contadorMayus >= 2 && contadorMinus >= 5 && contadorNums > 5 ) {
      return true;
    } else {
      return false;
    }
  },
  generarPassword: function() {
    var salidaPassword = "";
    var posibleChars  = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
    for (var i = 0; i < this.longitud; i++) {
        salidaPassword += posibleChars.charAt(Math.floor(Math.random() * posibleChars.length));
    }
    return salidaPassword;
  },
  seguridadPassword: function() {
    var contadorChars = 0;
    var arr = this.contrasennia.split(" ");
    for(i=0; i < arr.length; i++) {
      if(contadorChars <= 6 ) {
      return "Seguridad baja";
    } else if(contadorChars >= 7 && contadorChars <= 10) {
      return "Seguridad media"
    }else if(contadorChars >= 11 && contadorChars <= 20) {
    return "Seguridad Alta";
      }
    }
  }
}
```
![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/5515253.png)

## #6 #6.1 #6.2 #6.3 #6.4 #6.5
Implementar un objeto que modele un contador. Un contador se puede incrementar o decrementar, recordando el valor actual. Al resetear un contador, se pone en cero.
Además es posible indicar directamente cual es el valor actual. Este objeto debe entender los siguientes mensajes: 6.1 reset() 6.2 inc() 6.3 dec() 6.4 valorActual() 6.5 valorActual(nuevoValor) P.ej. si se evalúa la siguiente secuencia contador.valorActual(10) contador.inc() contador.inc() contador.dec() contador.inc() contador.valorActual() el resultado debe ser 12.

```javascript
var contador = {
    incremento : 10,
    decremento : 5,
    memoria: 12,

  reset : function() {
    return (this.incremento*0);
    this.memoria = 0;
  },
  inc : function() {
     this.memoria = (this.memoria + this.incremento);
     return this.memoria;
  },
  dec : function() {
     this.memoria = (this.memoria - this.decremento);
     return this.memoria;
  },
  valorActua : function() {
    var valorAct = this.memoria;
    return valorAct;
  },
  valorActual : function(nuevoValor) {
    var valorActual = nuevoValor;
    return valorActual 
  }
}
```
![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/66162636465.png)

## #7
Agregar al contador del ejercicio 6, la capacidad de recordar un String que representa el último comando que se le dio. Los Strings posibles son "reset", "incremento", "decremento" o "actualizacion" (para el caso de que se invoque valorActual con un parámetro). Para saber el último comando, se le envía al contador el mensaje ultimoComando().

![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/7.png)

## #8 #8.1 #8.2 #8.3
mplementar un objeto que modele a Chimuela, una dragona de la que nos interesa saber qué energía tiene en cada momento, medida en joules. En el metodo constructor simpli�cado que nos piden implementar, las únicas acciones que vamos a contemplar son: cuando Chimuela come una cantidad de comida especi�cada en gramos, en este caso adquiere 4 joules por cada gramo, y cuando Chimuela vuela una cantidad de kilómetros, en este caso gasta un joule por cada kilómetro, más 10 joules de �costo �jo� de despegue y aterrizaje. La energía de Chimuela nace en 0. El objeto que implementa este metodo constructor de Chimuela, debe entender los siguientes mensajes: 8.1 comer(gramos) 8.2 volar(kilometros) 8.3 energia() P.ej. si sobre un REPL(Read-Eval-Print-Loop)(Lectura-Evaluación-Impresión) recién lanzado se evalúa la siguiente secuencia Chimuela.comer(100) Chimuela.volar(10) Chimuela.volar(20) Chimuela.energia() el resultado debe ser 350.

```javascript
var chimuela = {
    energi : 0,
    gramos : 0,
    kilometros : 0,

    comer : function(gramos) {
        var conversion = (gramos*4);
        energia = conversion + this.energi;
        return energia;
    },
    volar : function(kilometros) {
        energia = (energia - kilometros)-20;
    },
    chimuelaEnergia: function() {
        return energia;
    }
}
```
![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/8818283.png)

## #9
Agregar al metodo constructor de Chimuela del ejercicio 8, la capacidad de entender estos mensajes: estaDebil(), Chimuela está débil si su energía es menos de 50. estaFeliz(), Chimuela está feliz si su energía está entre 500 y 1000. cuantoQuiereVolar(), que es el resultado de la siguiente cuenta. De base, quiere volar (energía / 5) kilómetros, p.ej., si tiene 120 de energía, quiere volar 24 kilómetros. Si la energía está entre 300 y 400, entonces hay que sumar 10 a este valor, y si es múltiplo de 20, otros 15. Entonces, si Chimuela tiene 340 de energía, quiere volar 68 + 10 + 15 = 93 kilómetros. Para probar esto, sobre un REPL recién lanzado darle de comer 85 a Chimuela, así la energía queda en

![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/9.png)

## #10 #10.1 #10.2 #10.3 #10.4 #10.5
Implementar un objeto que represente una calculadora sencilla, que permita sumar, restar y multiplicar. Este objeto debe entender los siguientes mensajes: 10.1 cargar(numero) 10.2 sumar(numero) 10.3 restar(numero) 10.4 multiplicar(numero) 10.5 valorActual() P.ej. si se evalúa la siguiente secuencia calculadora.cargar(0) calculadora.sumar(4) calculadora.multiplicar(5) calculadora.restar(8) calculadora.multiplicar(2) calculadora.valorActual() el resultado debe ser 24.

![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/10101102103104105.png)

## #11 
Crear un metodo constructor llamado Libro. Sus atributos título del libro, autor, número de ejemplares del libro y número de ejemplares prestados los siguiente metodos para la clase:
préstamo() que incremente el atributo correspondiente cada vez que se realice un préstamo del libro. No se podrán prestar libros de los que no queden ejemplares disponibles para prestar. Devuelve true si se ha podido realizar la operación y false en caso contrario. devolucion() que decremente el atributo correspondiente cuando se produzca la devolución de un libro. No se podrán devolver libros que no se hayan prestado. Devuelve true si se ha podido realizar la operación y false en caso contrario. toString() para mostrar los datos de los libros.

![li](https://github.com/FelipeeMartinez/ReadmeObejcts/blob/master/Imagenes/11.png)



















