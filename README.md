# Curso-Python
Carpeta Curso Python lunes: contiene tres archivos.

El archivo Ana 01 contiene los primeros ejercicios que hicimos creando variables, imprimiendo el típico 'Hola, mundo', 
añadiendo comentarios, entendiendo errores, los tipos de objetos en Python (string, integer y float), preguntar el tipo de datos (type),
casting (cambiar tipo de dato), datos booleanos (True, False), expresiones y variables.

El archivo Ana 02 sigue hablando de variables y tipos, las listas, ejercicios con operadores, insertar variables en cadenas
y empezamos a crear condiciones (if, elif, else)... quedan aún algunos puntos sin explicar que, supongo, veremos hoy...

El archivo Ana 03 Condicionales, los operadores de comparación (==, !=, <, <=, >, >=) que devuelven valores booleanos (True, False)
y se pueden combinar con operadores lógicos (and, or, not) y seguimos con unos ejercicios de condicionales que no terminamos. Hoy más.

Carpeta Curso Python martes: contiene un archivo.

El archivo Ana - 10 - Pandas contiene los ejercicios que hicimos usando la Librería Pandas.

Obtener las primeras 3 filas de un objeto DataFrame. df.head(3)

Obtener las últimas 3 filas de un objeto DataFrame. df.tail(3) o df[-3:] #así cogería los 3 registros empezando por atrás. # no le ponemos el registro final -1 pq en el rango, el último no lo coge.

Seleccionar las columnas ['nombre', 'califico'] de un objeto DataFrame. df[Lista_columnas] df[['nombre', 'califico']]

Comprobar si este objeto DataFrame está vacío con empty. df = pd.DataFrame({'X': []}) df.empty Resultado: True

Determinar los datos en un DataFrame que son nulos (NaN). df.isnull().values.any() df.isnull()

Modificar un valor o entrada específico de un objeto DataFrame usando loc. ¿Cómo funciona loc? nombredelDataFrame.loc['fila','columna'] nos localiza un dato situado en un cruce de fila x columna. Si quiero seleccionar dos filas, en el lugar de la 'fila' le ponemos una lista formada por las dos filas, es decir, ['filaa', filab'] que sería df.loc[['filaa', 'filab'], 'columna']. Si quiero todas las filas de dos columnas ponemos df.loc[:,['columna1', 'columna2']] Una vez localizado el valor, podemos reemplazarlo simplemente escribiendo igual = y el nuevo valor.

Acceder a un valor o entrada específico de un objeto DataFrame usando loc. También podemos usar iloc (loc indexado), si quiero seleccionar utilizando el número de fila o de columna en lugar de su nombre. Hay que tener en cuenta que python empieza a contar en 0 y no coge el último valor de una lista... Si sólo le ponemos un dato son las filas. Por ejemplo, df.iloc[1], trae la fila 1. Si quiero varias hay que hacer una lista: df.iloc[[1, 3, 4]]. Si quiero un intervalo df.iloc[3:5]. Si quiero solo un dato, una intersección df.iloc[numerofila,numerocolumna] Para coger columnas df.iloc[:, 2] (cogería todas las filas de la columna 2 (que es la tercera)

Sumar los valores de la columna intentos con sum. Suma_intentos = df["intentos"].sum() print (Suma_intentos)

Eliminar una fila de un DataFrame con la función drop. Nombre_de_la_nueva_df = df.drop('nombredelafila'). Podemos borrar dos filas creando una lista, poniendo sus nombres dentro de corchetes, entre comillas y separados por coma. Ejemplo new_df = df.drop([fila1, fila2]) Si son columnas lo que queremos eliminar, tenemos que escribir df.drop(columns=['nombrecolumna1', 'nombrecolumna2'])
