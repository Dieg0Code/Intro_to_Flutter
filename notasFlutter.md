# Intro to Flutter

## Dart

### ¿Por qué Dart?

Tanto Dart como Flutter fueron creados por Google, lo cual nos asegura una buena compatibilidad entre el lenguaje Dart y el framework Flutter.

Principales características de Dart:

- AOT (Ahead Of Time): Compilado a un rápido y predecible código nativo. (Totalmente personalizable).
- Puede ser JIT ( Just In Time): Compilado para una velocidad excepcional de desarrollo. (Esto incluye el popular Hot Reload).
- Hace fácil la creación de animaciones y transiciones que corren a 60fps (frames per second).
- Al ser compilado a código nativo, no hay puentes innecesarios para correr el código.
- Dart le permite a Flutter evitar el desarrollo de diseños en archivos independientes como JSX, XML o bien interfaces separadas.
- Dart es relativamente fácil de aprender.

### ¿Cómo luce un código en Dart?

```dart
void main() {
    // Punto inicial!
}
```

**Ciclos**:

```dart
for (int i = 0; i < 10; i++) {
    // do something here!
}
```

**Dart es un lenguaje con tipos de datos**:

```dart
String nombre; // null
```

**Clases**:

```dart
class Heroe {

}
```

**Para utilizar la clase**:

```dart
var spiderman = new Heroe();

var ironman = Heroe();
```

### Hola Mundo

En Dart las funciones deben especificar el tipo que retornan. Para decir que una función no retorna nada se utiliza la palabra **void**.

Dart debe finalizar en cada linea con un **;**

Se pueden comentar lineas en Dart usando ctrl + /

```dart
void main() {
    print('Hola Mundo');
}
```

String interpolation

```dart
void main() {
    var nombre = 'Diego';

    print('Hola $nombre');
}
```

Podemos declarar variables con **var** pero no es recomendable, es mejor usar los tipos ya que Dart los tiene.

### Tipos de datos Números y String

```dart
void main() {
    // Números
    int empleados = 10; // pueden ser negativos o positivos
    double pi = 3.14;
    double numero = 1.0;

    print('$empleados - $pi - $numero');

    // String
    String nombre = 'Diego';
    print(nombre);  // Diego
    print(nombre[0]);   // D
    print(nombre[nombre.length - 1]);   // o
}
```

### Tipos de datos Booleanos y condiciones

Los valores **booleanos** son especialmente importantes cuando estamos trabajando con condiciones:

```dart
void main() {
    bool activado = true;
    print(activado);    // true

    if (activado) {
        print('El motor esta funcionando!');
    } else {
        print('Está apagado');
    }
}
```

### Tipo de dato Lista

Es una colección de información que tiene algo en común

```dart
void main() {
    List<int> numeros = [1,2,3,4,5];
    print( numeros );   // [1,2,3,4,5]

    numeros.add(6);
    print( numeros );   // [1,2,3,4,5,6]

    // Podemos definir listas de tamaño fijo
    List masNumeros = List(10);
    
}
```

### Tipo de dato Map

Un map son pares de valores (key - value).

En Dart es importante manejar siempre el tipado de datos.

Los Maps también suelen ser conocidos como **diccionarios** de datos.

```dart
void main() {
    Map<String, dynamic> persona = {
        'nombre' :  'Diego',
        'edad'   :  25,
        'soltero':  true,
    };

    print( persona['nombre'] ); // Diego
    print( persona['edad'] );   // 25

    Map<int, String> personas {
        1:  'Pedro',
        2:  'Juan',
        3:  'Diego'
    }

    personas.addAll( { 4: 'Carlos' } );
    print(personas);    // {1: Pedro, 2: Juan, 3: Diego, 4: Carlos}
    print(personas[2]); // Juan
}
```