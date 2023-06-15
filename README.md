## Curso-Python
##Carpeta Curso Python lunes: contiene tres archivos.

- El archivo Ana 01 contiene los primeros ejercicios que hicimos creando variables, imprimiendo el típico 'Hola, mundo', 
añadiendo comentarios, entendiendo errores, los tipos de objetos en Python (string, integer y float), preguntar el tipo de datos (type),
casting (cambiar tipo de dato), datos booleanos (True, False), expresiones y variables.

- El archivo Ana 02 sigue hablando de variables y tipos, las listas, ejercicios con operadores, insertar variables en cadenas
y empezamos a crear condiciones (if, elif, else)... quedan aún algunos puntos sin explicar que, supongo, veremos hoy...

- El archivo Ana 03 Condicionales, los operadores de comparación (==, !=, <, <=, >, >=) que devuelven valores booleanos (True, False)
y se pueden combinar con operadores lógicos (and, or, not) y seguimos con unos ejercicios de condicionales que no terminamos. Hoy más.

##Carpeta Curso Python martes: contiene un archivo.

- El archivo Ana - 10 - Pandas contiene los ejercicios que hicimos usando la Librería Pandas.

Obtener las primeras 3 filas de un objeto DataFrame. df.head(3)

Obtener las últimas 3 filas de un objeto DataFrame. df.tail(3) o df[-3:] #así cogería los 3 registros empezando por atrás. # no le ponemos el registro final -1 pq en el rango, el último no lo coge.

Seleccionar las columnas ['nombre', 'califico'] de un objeto DataFrame. df[Lista_columnas] df[['nombre', 'califico']]

Comprobar si este objeto DataFrame está vacío con empty. df = pd.DataFrame({'X': []}) df.empty Resultado: True

Determinar los datos en un DataFrame que son nulos (NaN). df.isnull().values.any() df.isnull()

Modificar un valor o entrada específico de un objeto DataFrame usando loc. ¿Cómo funciona loc? nombredelDataFrame.loc['fila','columna'] nos localiza un dato situado en un cruce de fila x columna. Si quiero seleccionar dos filas, en el lugar de la 'fila' le ponemos una lista formada por las dos filas, es decir, ['filaa', filab'] que sería df.loc[['filaa', 'filab'], 'columna']. Si quiero todas las filas de dos columnas ponemos df.loc[:,['columna1', 'columna2']] Una vez localizado el valor, podemos reemplazarlo simplemente escribiendo igual = y el nuevo valor.

Acceder a un valor o entrada específico de un objeto DataFrame usando loc. También podemos usar iloc (loc indexado), si quiero seleccionar utilizando el número de fila o de columna en lugar de su nombre. Hay que tener en cuenta que python empieza a contar en 0 y no coge el último valor de una lista... Si sólo le ponemos un dato son las filas. Por ejemplo, df.iloc[1], trae la fila 1. Si quiero varias hay que hacer una lista: df.iloc[[1, 3, 4]]. Si quiero un intervalo df.iloc[3:5]. Si quiero solo un dato, una intersección df.iloc[numerofila,numerocolumna] Para coger columnas df.iloc[:, 2] (cogería todas las filas de la columna 2 (que es la tercera)

Sumar los valores de la columna intentos con sum. Suma_intentos = df["intentos"].sum() print (Suma_intentos)

Eliminar una fila de un DataFrame con la función drop. Nombre_de_la_nueva_df = df.drop('nombredelafila'). Podemos borrar dos filas creando una lista, poniendo sus nombres dentro de corchetes, entre comillas y separados por coma. Ejemplo new_df = df.drop([fila1, fila2]) Si son columnas lo que queremos eliminar, tenemos que escribir df.drop(columns=['nombrecolumna1', 'nombrecolumna2'])

##Carpeta Curso Python miércoles: contiene tres archivos.

El miércoles comenzamos finalizando la corrección de los ejercicios del día anterior.

- El archivo Ana Prophet v2 - Predecir el valor de bitcoin contiene todo el ejercicio que hicimos para ver cómo funciona Prophet y lo usamos para predecir el valor futuro de los bitcoin.

- El archivo Ana M4 - 06- Bucles contiene la información y los ejercicios que realizamos para aprender sobre los bucles. Vimos las ventajas de usar for en lugar de while. También usamos break y continue.

Los ejercicios que hicimos: Dada una cadena de texto, indique el número de vocales que contiene: texto = 'holaestoesunapruebaenpython'. contador = 0. for letra in texto:
  if letra == "a" or letra  == "e" or letra == "i" or letra == 'o' or letra == 'u':. contador += 1. print (contador)
  
Luego generamos secuencias de datos: La función range() devuelve un flujo de números en el rango especificado, sin necesidad de crear y almacenar previamente una larga estructura de datos. Esto permite generar rangos enormes sin consumir toda la memoria del sistema. El uso de range() es similar a los slices: range(start, stop, step). Podemos omitir start y el rango empezaría en 0. El único valor requerido es stop y el último valor generado será el justo anterior a este. El valor por defecto de step es 1, pero se puede ir "hacia detrás" con -1. range() devuelve un objeto iterable, así que necesitamos obtener los valores paso a paso con una sentencia for ... in (o convertir el objeto a una secuencia como una lista). for x in range(0, 3):. print(x)

Escribe un bucle for que imprima todos los elementos entre -5 y 5 usando la función de rango. for x in range(-5,6):. print(x)

Imprime los elementos de la siguiente lista: Genres=[ 'rock', 'R&B', 'Soundtrack', 'R&B', 'soul', 'pop'] Asegúrate de seguir las convenciones de Python. Generos=['rock', 'R&B', 'Soundtrack', 'R&B', 'soul', 'pop']
for genero in Generos:. print (genero)

Escribe un blucle for que imprima la siguiente lista: squares=['red', 'yellow', 'green', 'purple', 'blue'] squares=['red', 'yellow', 'green', 'purple', 'blue']. for color in squares:. print (color)

Escribe un bucle while para mostrar los valores del Rating de una lista de reproducción de un álbum almacenada en la lista PlayListRatings. Si la puntuación es inferior a 6, sal del bucle. La lista PlayListRatings está dada por: PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10] (Lo hicimos con for pq Luís nos recomienda no complicarnos...
PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]
for valor in PlayListRatings:
  if valor < 6:
    break
  print (valor)
  
Escribe un bucle while (for) para copiar los string 'orange' de la lista squares a la lista new_squares. Para y sal del bucle si el valor de la lista no es 'orange':
squares = ['orange', 'orange', 'purple', 'blue ', 'orange']
new_squares = []
for color in squares:
  if color == 'orange':
    new_squares.append(color)
  if color != 'orange':
    break
print(new_squares)

Imprima los 100 primeros números de la secuencia de Fibonacci:  0,1,1,2,3,5,8,13,21,34,55,89,…
a = 0
b = 1
Bucle: En esta secuencia cada número es suma de los dos anteriores. Es decir c=a+b pero no podemos crear una secuencia de sumas infinita... Entonces podemos traducirlo como que a=b y b=c, al que llamaremos siguiente. Como es un bucle, va cogiendo uno por uno cada elemento de la lista... y el bucle se repite tantas veces como el rango que le hemos dado. El guión bajo se usa por poner algo pq no va a ser una variable que vayamos a usar. En lugar de ese guión podíamos poner ListaFibonacci.

for ListaFibonacci in range(100):
  print(a)
  siguiente = a + b
  a = b
  b = siguiente

- El archivo Ana SpaceX - 4 - EDA with Data Visualization son ejercicios realizados con pandas, numpy, matplotlib.pyplot y seaborn.
Con los datos importados sobre las misiones espaciales de Space X hemos aprendido a hacer gráficas e interpretarlas.
