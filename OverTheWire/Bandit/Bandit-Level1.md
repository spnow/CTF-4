#Bandit Level 1 → Level 2

##Level Goal

The password for the next level is stored in a file called - located in the home directory

##Commands you may need to solve this level

ls, cd, cat, file, du, find

Helpful Reading Material



## Write Up Iker

La contraseña la hemos sacado en el anterior apartado:

**FLAG** = {boJ9jbbUNNfktd78OOpsqOltutMc3MY1} 

Utilizamos esta contraseña para acceder al siguiente nivel 

```bash 
$ ssh bandit1@bandit.labs.overthewire.org
```
Entramos en la carpeta y hacemos un ls para saber que ficheros hay. Solamente hau un fichero con un guión **-**

Probamos a hacer **cat -** pero nos salta un error porque el guión es bash es un caracter especial por lo que lo hacemos de la siguiente manera indicandole el nombre del fichero en el mismo directorio.

```bash 
bandit1@melinda:~$ ls -l
total 4
-rw-r----- 1 bandit2 bandit1 33 Nov 14  2014 -
bandit1@melinda:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
bandit1@melinda:~$ 
```

**FLAG** = {CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9}
