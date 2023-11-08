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

## Listas en Dart
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

## Clases en Dart
Deben empezar con mayusculas. Se necesita inicializar tanto `questionText` debido a conflicto de tipos y `q` porque queremos pasar parametros nombrados
```
class Question {
  String questionText = '';
  bool questionAnswer = true;

  Question({String q = '', bool a = true}) {
    questionText = q;
    questionAnswer = a;
  }
}

List<Question> questionBank = [
    Question(
        q: 'You can lead a cow down stairs but not up stairs.', 
        a: false),
    Question(
        q: 'Approximately one quarter of human bones are in the feet.',
        a: true),
    Question(
        q: 'A slug\'s blood is green.', 
        a: true),
  ];

questionNumber = 0; // se incrementara de uno en uno

String question = questionBank[questionNumber % questionBank.length].questionText
bool correctAnswer =questionBank[questionNumber % questionBank.length].questionAnswer;
```
