# Algoritmo para actualizar archivos

## Español

### Caso de estudio

En una empresa sanitaria, es necesario mantener actualizada la lista de direcciones IP autorizadas para acceder a los registros de pacientes. Este algoritmo recibe una lista de IPs que deben eliminarse, busca esas direcciones en el archivo de autorización y actualiza el archivo con las direcciones restantes.

### ¿Cómo funciona?

La función `update_file(import_file, remove_list)`:

1. Abre el archivo de entrada en modo lectura con `open()` dentro de una sentencia `with`.
2. Lee el contenido y lo convierte en una lista de direcciones IP separadas por espacios.
3. Recorre las direcciones y comprueba con `if` si cada una está en `remove_list`; si coincide, la elimina.
4. Une las direcciones restantes y sobrescribe el archivo original con `write()` dentro de otra sentencia `with`.

Si una IP de `remove_list` no aparece en el archivo, no se elimina ninguna dirección por esa entrada. Después de actualizar el archivo, el ejemplo vuelve a abrirlo y muestra su contenido.

### Uso

El ejemplo incluido procesa `allow_list.txt` y solicita eliminar estas IPs:

```python
update_file(
    "allow_list.txt",
    ["192.168.25.60", "192.168.140.81", "192.168.203.198"]
)
```

El archivo `allow_list.txt` debe estar disponible en el directorio desde el que se ejecuta el programa. El archivo se sobrescribe, por lo que conviene conservar una copia de seguridad cuando sea necesario.

### Nota sobre la implementación

La función elimina elementos de la lista mientras la recorre. Si hay varias IPs que deben eliminarse una junto a otra, el recorrido puede saltarse alguna. Para garantizar que se eliminen todas las coincidencias, conviene construir una lista nueva que excluya las IPs de `remove_list`.

## English

### Case study

A healthcare company needs to keep its list of IP addresses authorized to access patient records up to date. This algorithm takes a list of IPs to remove, searches for those addresses in the authorization file, and updates the file with the remaining addresses.

### How it works

The `update_file(import_file, remove_list)` function:

1. Opens the input file for reading with `open()` inside a `with` statement.
2. Reads the contents and converts them into a list of IP addresses separated by whitespace.
3. Iterates through the addresses and uses `if` to check whether each one is in `remove_list`; if it matches, it removes it.
4. Joins the remaining addresses and overwrites the original file with `write()` inside another `with` statement.

If an IP in `remove_list` is not present in the file, that entry does not remove any address. After updating the file, the example opens it again and displays its contents.

### Usage

The included example processes `allow_list.txt` and requests the removal of these IPs:

```python
update_file(
    "allow_list.txt",
    ["192.168.25.60", "192.168.140.81", "192.168.203.198"]
)
```

The `allow_list.txt` file must be available in the directory from which the program is run. The file is overwritten, so keep a backup when needed.

### Implementation note

The function removes items from the list while iterating over it. If multiple IPs to remove appear consecutively, the iteration may skip one of them. To ensure that every match is removed, build a new list that excludes the IPs in `remove_list`.
