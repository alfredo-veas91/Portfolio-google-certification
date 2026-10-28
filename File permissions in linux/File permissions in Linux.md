# Permisos de archivo en Linux

## Descripción del proyecto

Se necesita examinar los permisos existentes y modificarlos cuando corresponda para autorizar a los usuarios apropiados y restringir accesos no autorizados.

## Verificar detalles de archivos y directorios

Para revisar los contenidos del directorio y sus permisos, utilizamos:

```bash
ls -l
```

![][image1]

## Describir la cadena de permisos

La cadena de permisos tiene la siguiente estructura:

```text
drwxrwxrwx
```

- `d`: indica un directorio; `-` indica un archivo regular.
- Primer `rwx`: permisos del propietario.
- Segundo `rwx`: permisos del grupo.
- Tercer `rwx`: permisos de otros usuarios.

Las letras `r`, `w` y `x` representan lectura, escritura y ejecución, respectivamente. Un guion (`-`) indica la ausencia del permiso correspondiente.

## Cambiar permisos de archivo

Para quitar el permiso de escritura a otros usuarios sobre el archivo `project_k.txt`, utilizamos:

```bash
chmod o-w project_k.txt
```

![][image2]

## Cambiar permisos de un archivo oculto

Primero revisamos los permisos, incluyendo los archivos ocultos:

```bash
ls -la
```

La opción `-l` muestra información detallada y `-a` incluye los archivos ocultos, cuyos nombres comienzan con un punto. En este caso, el archivo es `.project_x.txt`.

Se requiere que el propietario y el grupo puedan leerlo, pero no modificarlo. Como el grupo aún no tiene permiso de lectura, aplicamos:

```bash
chmod u-w,g-w,g+r .project_x.txt
```

![][image3]

## Cambiar permisos de directorio

Los permisos de directorio se revisan en el listado:

```bash
ls -l
```

El carácter inicial `d` identifica los directorios. En ellos, el permiso de ejecución (`x`) permite atravesarlos y acceder a sus entradas, sujeto a los demás permisos aplicables.

Para retirar el permiso de ejecución al grupo sobre el directorio `drafts`, utilizamos:

```bash
chmod g-x drafts
```

![][image4]

## Resumen

La gestión de permisos permite aplicar el principio de mínimo privilegio: otorgar únicamente los accesos necesarios para realizar las tareas. En este ejercicio se ajustaron los permisos del directorio `projects` y sus contenidos según los requisitos del caso, utilizando `chmod`.

Para revisar los permisos resultantes, utilizamos:

```bash
ls -la
```

