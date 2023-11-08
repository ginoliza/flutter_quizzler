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

## Listas
```
List<String> myList = [
  'Angela',
  'James',
  'Katie',
  'Jack'
];

void main(){
  // acceder por indice
  print(myList[2]);
  
  // acceder por método
  print(myList.first);
  
  // obtener indice de elemento
  print(myList.indexOf('Jack'));
  
  // agregar elemento al final
  myList.add('Ben');
  print(myList);
  
  // agregar elemento en el indice x
  myList.insert(2, 'Gino');
  print(myList);
}
```

## Historial de codigo
Se puede viajar en el tiempo con el historial
`File -> Local History -> Show history`

## Ignorar typos
`Mouse encima->Añadir a diccionario`

## Comillas dentro de un string
Con backslash
`'gino\'s favorite food'`

