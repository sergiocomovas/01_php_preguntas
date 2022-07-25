PREGUNTA | RESPUESTA | COMENTARIOS
--|--|--
❓¿Cuál es la diferencia entre GET y POST a la hora de enviar un formulario?|↪️El método GET: los datos se ven en la URL. El método POST los envía por detrás|🟢
❓¿Si quieres enviar un archivo por formulario que atributo tienes que poner?|↪️multipart/form-data|🟢 HTML forms provide three methods of encoding: application/x-www-form-urlencoded (the default), multipart/form-data and text/plain
❓¿Qué diferencia hay entre INCLUDE y REQUIRE?|↪️REQUIRE es más extricto y obliga a que el archivo esté incluído.|🟢
❓¿Qué es un array asociativo?|↪️Los índices no se texto: puedo elegir un dato dentro del array por su nombre, su ínicide asociativo (alfanumérico)|🟢 <code> $age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43"); <hr> $age['Peter'] = "35"; $age['Ben'] = "37"; $age['Joe'] = "43"; </code>
❓¿Qué diferencia hay entre SESSION y COOKIE?|↪️LA SESSION se pierde cuando el navegador se cierra. Las COOKIES son más persistentes|🟢
❓¿Qué es el MVC?|↪️Es el MODELO VISTA CONTROLADOR es un patrón de diseño para organizar la aplicación web. MODELO es la parte que se comunica directamente con la base de datos. El modelo pasa la vista al CONTROLADOR que la procesa. La VISTA es la parte visual.|🟢
❓Dime dos forma de ejecutar SQL dentro de PHP|↪️ Usar la función MYSQLi y PDO|🟢 <code>$mysqli = new mysqli("localhost", "my_user", "my_password", "world");</code><hr><code>$gbd = new PDO($dsn, $usuario, $contraseña);</code>
❓¿Cómo harías un formulario para registrarse?|↪️Crear un formulario con el ACTION que apunte a un fichero PHP que me permita validar el formulario o devolver un error, guardar los datos con un instert y redirigir el usuario a un pantalla de confirmación (y email) |🟢
❓¿Cómo harías un buscador dentro de PHP?|↪️Crear un formularioc con un botón de buscar: Hacer un select en la base de datos con un WHERE con comodines y recoger el resultado de la consulta SQL y se muestran los datos.|🟢 <code>if ($resultado = $mysqli->query($consulta)) <br> {<br> /* obtener el array de objetos */ <br><br> while ($fila = $resultado->fetch_row()) <br><br>{ printf ("%s (%s)\n", $fila[0], $fila[1]); }<br><br> /* liberar el conjunto de resultados */ $resultado->close();<br><br>}</code>
❓¿Cómo harías un login en PHO?|↪️Crear un formulario, se envian por POST a una página para recoger la infomación y procesarla con un SELECT y si coinciden los datos esta informaicón se recoge y se genera un COOKIE o una SESSION|🟢
❓¿Cómo ver la cantidad de letras que tiene un string?|↪️Strlen() function |🟢
❓¿Cómo encriptarias una contraseña en PHP?|↪️SHA256 o CRIPT|🟢<code>$hashed_password = crypt('mypassword');</code><hr> https://www.php.net/manual/es/function.password-hash.php
❓¿Qué librería usarias para enviar un mail?|↪️PHP MAILER o la propia del framework|🟢
❓¿Para que sirve el CONTRUCTOR de una clase?|↪️ Es el primer método que se ejecuta dentro de la clase. Y se suele usar para iniciar el valor de las propiedades.|🟢
❓¿Para qué sirve la función UNSET?|↪️Para eliminar un ínicide de un array o un dato en una sesión|🟢
❓¿Cómo saber la IP de un visitante?|↪️Usando la variable superglobales: $_SERVER|🟢$_SERVER['REMOTE_ADDR']
❓Dime cinco frameworkd de dearrollo pho|↪️Laravel, Symphony, Zenframework, Codeingnite, Gframework, Falcon,,,, |🟢 https://laravel.com/ https://symfony.com/ https://codeigniter.com/ https://getlaminas.org/ https://www.yiiframework.com/ https://cakephp.org/ https://www.slimframework.com/ https://phalcon.io/es-es https://fuelphp.com/ https://fatfreeframework.com/3.8/home 

PREGUNTAS RÁPIDAS | RESPUESTA
-- | --
¿Cual es la etiqueta de PHP? | <?php>
¿Quíen fue el creador de PHP? | RASMUS
¿Cómo obtienes la IP del cliente usando PHP? | $_SERVER["REMOTE_ADDR"]
¿Qué significa la siglas PHP? | PHP: Hypertext procesor
¿Cuál es el símbolo para una variable en php? | $
¿En dónde se ejecuta el código PHP? | SERVIDOR
¿Cuál de las instrucciones es correcta? |  ``` if($a==0){echo "hola";}```
Formas de pasar parámetros en PHP | GET Y POST
¿Cuál es la función para obtener la longitud de una cadena? | strlen
¿Cual es el ejemplo de un array en PHP? | array("fresa)
¿Qué función que sirve para copia? | copy
Array que tiene variables de sesión | $_SESSION
¿Cuál es un ejemplo de instancia? | $a = new F();
¿Cuál es contructor en PHP? | __construct()
¿Cuál es la clase para conectarse a la base de datos? | PDO
Sirve para incluir archivos externos | INCLUDE
¿Qué nombre de la variable NO es válido? | $5estado
¿Qué funcion sirve para escribir texto con formato? | printf()
Función para conar un arreglo | count()
Librería para contecarse a SQL SERVER | mssql
¿Cuál e la constate PHO para el separador de directorio en el servicor? | DIRECTORY_SEPARATOR
¿Cuál es la librería para minupar imágenes? | GD
¿Cuál de las variables está mal definida? | $.2
Devuelve el residuo de una división | fmod
Permite redondear las fracciones hacia arriba | ceil
La función permite repetir un cadena | str_repeat
La función devuelve parte de una cadena | substr


ARRAY DE OBJETOS:<br>

    The above getResult() function returns an array of objects.
    Example: $row->title

ARRAY DE ÍNDICES:<br>

    The above getResultArray() function returns an array of standard array indexes.
    Example: $row['title']


EN CODEIGNITER:  https://codeigniter.com/user_guide/database/query_builder.html

    <?php

    $data = [
    'title' => $title,
    'name'  => $name,
    'date'  => $date,
    ];

    $db->table('mytable')->insert($data);
    // Produces: INSERT INTO mytable (title, name, date) VALUES ('{$title}', '{$name}', '{$date}')

A partir de PHP 5.4 también se puede usar la sintaxis de array corta, la cual reemplaza array() con [].