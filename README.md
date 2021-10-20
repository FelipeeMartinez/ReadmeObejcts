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










