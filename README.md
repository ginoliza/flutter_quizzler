# Quizzler

## Trucos
- Para tener un bloque centrado y expandido: un `Center` dentro de un `Padding`
- Colorear un boton:
```
TextButton(
  style: TextButton.styleFrom(
    backgroundColor: Colors.green,
  ),
  ...
)
```

## Lista de iconos
Declaramos una lista de iconos para que se muestre dentro del `row`
```
List<Icon> scoreKeeper = [
    Icon(
      Icons.check,
      color: Colors.green,
    ),
    Icon(
      Icons.close,
      color: Colors.red,
    ),
    Icon(
      Icons.check,
      color: Colors.green,
    ),
    Icon(
      Icons.close,
      color: Colors.red,
    ),
    Icon(
      Icons.close,
      color: Colors.red,
    ),
  ];
```

```
Row(
  children: scoreKeeper,
),
```

## Agregar iconos a la lista
Y luego podemos usar el metodo `.add` para añadir mas iconos a la lista
```
onPressed: () {
    setState(() {
      print("False got pressed");
      scoreKeeper.add(
        Icon(
          Icons.close,
          color: Colors.red,
        ),
      );
    });
  },
```