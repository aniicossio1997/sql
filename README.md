[Ver TP-2](https://sqliteonline.com/)

# TP1 SQL

Realizado con [SQLite](https://sqliteonline.com/)

1.  Cree una tabla llamada CURSO con los atributos:
1.  Código de curso (clave primaria, entero no nulo)
1.  Nombre (varchar no nulo)
1.  Descripcion (varcha)
1.  Turno (varchar no nulo)
    Código:

```
CREATE TABLE curso (codigo integer PRIMARY KEY NOT NULL, nombre varchar NOT NULL, descripcion varchar, turno varchar)
```

2.  Agregue un campo “cupo” de tipo numérico
    ```
        ALTER TABLE curso ADD column cupo INTEGER
    ```
3.  Inserte datos en la tabla:

    1.  (101, “Algoritmos”,”Algoritmos y Estructuras de Datos”,”Mañana”,35)

        ```
        Consulta:
        insert into curso(codigo, nombre, descripcion,turno,cupo)
        VALUES (101, "Algoritmos","Algoritmos y Estructuras de Datos","Mañana",35);
        ```

        **Resultado**:
        ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e3-1.png)

    2.  (102, “Matemática Discreta”,””,”Tarde”,30)

    ```
        Consulta:
        insert into curso(codigo, nombre, descripcion,turno,cupo)
        VALUES (102, "Matemática Discreta","","tarde",30);

    ```

    **Resultado**:

    ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e3-2.png)

4.  Intente ingresar un registro con el nombre nulo y verifique que no funciona.

    ```
    Consulta:
    insert into curso(codigo, nombre, descripcion,turno,cupo)
    VALUES (103, NULL,"otra materia","tarde",30);

    ```

    **Resultado**

    ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e4.png)

5.  Intente ingresar un registro con la clave primaria repetida y verifique que no funciona.

    ```
    Consulta:
    insert into curso(codigo, nombre, descripcion,turno,cupo)
    VALUES (102, "Logica e Inteligencia artificial","otra materia","tarde",30);

    ```

    **Resultado**

    ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e-5.png)

6.  Actualice, para todos los cursos, el cupo en 25.

    Antes de la actualización:

    ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e-6-prev.png)

    ```
    Consulta:
    UPDATE curso SET cupo = 25;
    ```

    Después de la actualización

    ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e-6-after.png)

7.  Elimine el curso Algoritmos.

    ```
    Consulta:
    DELETE FROM CURSO WHERE nombre = "Algoritmos"
    ```

    ![enter image description here](https://github.com/aniicossio1997/sql/blob/main/e-7.png)
