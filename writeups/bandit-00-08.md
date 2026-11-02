# Bandit 00–08

**Fecha:** 2026-11-02
**Objetivo:** practicar comandos básicos de Linux en un entorno real.

## Nivel 0 → 1
**Comando:** `cat readme`
**Por qué funcionó:** el archivo estaba en el home y era texto plano.

## Nivel 1 → 2
**Comando:** `cat ./-`
**Por qué funcionó:** es la ruta exacta del archivo 

## Nivel 2 → 3
**Comando:** `cat "./spaces in this filename"`
**Por qué funcionó:** al poner "" agrupa todo el texto en un solo bloque

## Nivel 3 → 4 
**Comando:** `ls -a`
**Por qué funcionó:** al usar -a lista todos los archivos incluyendo los ocultos

## Nivel 4 → 5
**Comando:** `file ./*` `cat ./-file07`
**Por qué funcionó:** el primero muestra que ./-file07 era el unico con ascii y el otro evito el error del guion

## Nivel 5 → 6 
**Comando:** `find . -size 1033c`
**Por qué funcionó:** porque filtra por tamaño en este caso 1033 bytes

## Nivel 6 → 7 
**Comando:** `find / -user bandit7 -group bandit6 -size 33c`
**Por qué funcionó:** funciono porque con / indicamos que busque desde la raiz y luego con los otros parametros filtramos exactamente lo que queremos.

## Nivel 7 → 8 
**Comando:** `grep "millionth" data.txt`
**Por qué funcionó:** funciona ya que con las "" se filtra la palabra clave a localizar en el archivo data.txt


## Nivel 8 → 9
**Comando:** `cat data.txt | sort | uniq -u`
**Por qué funcionó:** cat lee el archivo, toma el texto y lo ordena en filas identicas consecutivas y uniq -u solo deja la linea que no se repite
