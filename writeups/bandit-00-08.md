# Bandit 00–08

**Fecha:** 2026-11-02
**Objetivo:** practicar comandos básicos de Linux en un entorno real.

## Nivel 0 → 1
**Comando:** `cat readme`
**Por qué funcionó:** el archivo estaba en el home y era texto plano.

## Nivel 1 → 2
**Comando:** `cat ./-`
**Por qué funcionó:** `-` solo lo interpreta el shell como "leer de stdin". Al anteponer `./` le indico que es un archivo del directorio actual. 

## Nivel 2 → 3
**Comando:** `cat "./spaces in this filename"`
**Por qué funcionó:** al poner "" agrupa todo el texto en un solo bloque

## Nivel 3 → 4
**Comando:** `ls -a` y luego `cat ./.hidden`
**Por qué funcionó:** `-a` muestra los archivos ocultos (los que empiezan con punto); `cat` lee su contenido.

## Nivel 4 → 5
**Comando:** `file ./*` `cat ./-file07`
**Por qué funcionó:** el primero muestra que ./-file07 era el unico con ascii y el otro evito el error del guion

## Nivel 5 → 6 
**Comando:** `find . -type f -size 1033c ! -executable`
**Por qué funcionó:** filtra las tres condiciones del nivel: archivo regular, 1033 bytes y que no sea ejecutable.

## Nivel 6 → 7 
**Comando:** `find / -user bandit7 -group bandit6 -size 33c 2>/dev/null`
**Por qué funcionó:** busca desde la raíz filtrando dueño, grupo y tamaño. `2>/dev/null` descarta los "Permission denied".

## Nivel 7 → 8 
**Comando:** `grep "millionth" data.txt`
**Por qué funcionó:** funciona ya que con las "" se filtra la palabra clave a localizar en el archivo data.txt


## Nivel 8 → 9
**Comando:** `sort data.txt | uniq -u`
**Por qué funcionó:** `sort` ordena las líneas (sin `cat`, que sería redundante) y `uniq -u` deja solo la que aparece una vez.
