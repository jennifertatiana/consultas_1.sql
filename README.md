# consultas1

#  EJERCICIOS CONSULTAS SQL

## Tabla usuario

![tabla usuario](img/tabla_usuario.png "Tabla usuario")

## COMANDO SELECT 

1. Para visualisar toda la informacion que contiene la tabla `usuario` se puede incluir con la instruccion SELECT el caracter '*' o cada uno de los campos de la tabla
`select * from usuario` 

![Consulta1](img/consulta1.png "consulta1")

2. Visualizar solamente la identificacion del usuario.

`select identificacion from usuario`

![Consulta2](img/consulta2.png "consulta2")


3. Se desea obtener los registros cuya identificacion sean mayores o iguales a 150, se debe utilizar la clausula WHERE que especifica las condiciones que deben reunir los registros que se van a seleccionar.

`SELECT * FROM usuario WHERE Identificación >='150'`

![consulta3](img/consulta3.png)

4. si se desea obtener los registros cuyo apellido sean Vanegas o Celina, se debe utilizar el operador IN que especifica los registros que se quieren para visualizar de una tabla. 

`select apellidos from usuario where apellidos IN ('Vanegas' , 'Celina')`

![consulta4](img/consulta4.png "consulta4")

o se puede utilizar el operador OR.

`select apellidos from usuario where apellidos-'Vanegas' OR apellidos-'Celina'`

![consulta4](img/consulta4.png "consulta4")

5. si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'cali', se debe utilizar el operador AND.

`SELECT * FROM usuario WHERE Identificación<='110' AND ciudad_nac='cali'`

![consulta5](img/consulta5.png "consulta5")


6. si se desea obtener los registros de cuyos nombre empiecen por la letra 'A' se debe utilizar el operador LIKE que uutiliza los patrones '%' (todos) y '_' (caracter).

`SELECT * FROM usuario WHERE nombre LIKE 'A%'`


![consulta6](img/consulta6.png "consulta6")

7. si desea obtener los registros cuyos nombres contengan la letra 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '%a%'`

![consulta7](img/consulta7.png "consulta7")

8. si se desea obtener los registros donde la cuarta letra del nombre sea una 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '_____a%`

![consulta8](img/consulta8.png "consulta8")

9. si se desea obtener registros cuya identificacion este entre intervalo 110 y 150, se debe utilizar  la clausula BETWEEN, que sirve para especificar un intervalo de valores. 

`SELECT * FROM usuario WHERE identificacion BETWEEN '110` AND '150'

![consulta9](img/consulta9.png "consulta9")

## COMANDO DELET 

10. para eliminar solamente los registros cuya identificacion sea mayor de 130.

`DELETE FROM usuario WHERE identificacion>'130'

![consulta10](img/consulta10.png "consulta10")
![consulta10_2](img/consulta10_2.png "consulta10_2")

## COMANDO UPDATE

11. para actualizar la ciudad de naciminiento de Cristian Vanegas, cuya identificacion es 114.

`UPDATE usuario SET ciudad_nac = ' Manizales' WHERE identificacion=114`

![consulta11](img/consulta11.png "consulta11")
![consulta11_2](img/consulta11_2.png "consulta11_2")

## INNER JOIN 

permite obtener datos o mas tablas. cuando se realiza la concatenacion de las tablas, no necesariamente se deben mostrar todos los datos de las tablas.
 