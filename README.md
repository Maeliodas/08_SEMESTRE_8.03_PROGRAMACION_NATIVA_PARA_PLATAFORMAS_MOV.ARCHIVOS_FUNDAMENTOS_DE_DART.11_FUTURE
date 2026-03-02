Decimo primer codigo de dart, Future, el equivalente al Promise de JS, este es el codigo

```dart
void main() {
  print('Inicio del programa');
  
  //print(httpGet());
  
  httpGet().then((value){/*añadir dentro de httpGet la url cuando exista api*/
    print(value);
  }).catchError((err){
    print('Error: $err');
  });
(11)_FUTURE
solo almacena 
  
  print('Fin del programa');
}

Future<String> httpGet(){/*añadir String url dentro de httpGet()*/
  return  Future.delayed(const Duration(seconds:3), (){
    throw 'Error en la petición http';
    //return "Respuesra de la peticion http";
  }); //Equivalente al promise de JS indica que tendra un valor a futuro
  
}
```
Como podemos ver usamos Future para indicarle que recibira un valor a futuro
