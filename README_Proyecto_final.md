# README

Esta carpeta contiene un script para correr un análisis filogenetico a partir de secuencias en formato fasta 
 
#### Para que todo corra correctamente SE DEBE DEFINIR el WD en carpeta bin, p. ej.:

Línea de comando ``` $ cd /somewhere/proyecto_final_Bioinf2017-2_GTC/bin ```

En R ``` $ setwd ("~/somewere/proyecto_final_Bioinf2017-2_GTC/bin")```

=========================================================
#### IMPORTANTE ####

Se deben tener los siguientes programas instalados. Las versiones que se utilizaron en este script son:

* muscle v3.8.31 by Robert C. Edgar 
* mafft v7.215
* RAxML v.8.0.26 released by Alexandros Stamatakis on June 25 2014 (https://github.com/stamatak/standard-RAxML)

========================================================


### Scripts


*************************
El script "script_commandLine.sh" en formato shell contiene las instrucciones para hacer el alineamiento (Muscle y Mafft) y la hipótesis filigenética (RaxML) para cada alineamiento.

```
Se debe correr así:

	$ ./script_commandLine.sh
```

-------- Muscle se usó de la siguiente manera:
```
 $ muscle -in  -out 
```

-------- Mafft se usó de la siguiente manera: 

```
 $ mafft input > output 

	# para correr con los parámetros como Default 
		# *Gap opening penalty: 1.53
		# *Maximum number of iterative refinement:0
		# *Output:fasta format
		# *Outorder: input order
	# para especificar y/o explorar otros valores os remito al manual 

``` 

-------- RaxML se usó de la siguiente manera:


```
 $ raxml -f a  -x -p  -#20 -m -s -n 

	donde:
	(-f a) indica un análisis de Bootstrap rápido
	(-x) valor "semilla" seleccionado al azar
	(-p) valor "semilla" seleccionado al azar
	(-#) Réplicas de Bootstrap
	(-m) modelo de substitución
	(-s) nombre del archivo input
	(-n) nombre del archivo output
```

**************************


**************************
Editado del Árbol en R

El script "RMakeMeATree.R" contiene el codigo comentado que se usó para editar los árboles

**************************

### Estructura del repositorio 


Carpetas:

```
/bin
Contiene dos scripts, uno para correr en la terminal y el otro en R
	* script_commandLine.sh
	* RMakeMeATree.R

```

```
/data
Contiene los datos que se usarán en el análisis
	
	/data/sec_fasta
	
	Aquí estan las secuencias sin alinear
	
	/data/sec_alin
	
	Aquí se guardarán las secuencias alineadas
	
```
```
/tree
Contiene los archivos del análisis filogenético que originó RaxML 
```
```
/edited_tree
Contiene el árbol editado en R
```






