# Avance 2

####Datos crudos 

* Referente a los datos crudos, estos provienen de un secuenciador Abi prism y el formato de salida es .Ab1 intenté correrlo en FastQC y no admite dicho formato. Aun no se si hay manera de convertirlos. De la forma que encontré que podia hacerse el pre-procesamiento  es con Geneious sin embargo no cuenta con una versión en linea de comando.  

#### A la fecha he revisado estos papers con especial atencion en la metodología:


* Compartive mitogenomics of leeches (Annelidae: Clitellata): Genome conservation and Placobdella-specific trnDGene Duplication (2016). Oceguera-Figueroa et al.
	
	: De este descubrí que el anlineamiento se puede hacer con MAFFT. buscando en la pagina del sofware vi que  tiene un versión en linea de comando corriendo el programa con:

´´´

	$ /path/mafft-linux64/mafft.bat input.txt > output.txt	
´´´	
* Are "uneversal" DNA primers really universal? (2014). Sharma & Kobayashi

* Arhynchobdellida (Annelida: Oligochaeta: Hirudinida):phylogenetic relationships and evolution (2004). Siddall & Borda.

* DNA-barcoding eveidence for widespread introductions of a leech from the south american Helobdella triserialis complex (2004). Siddall & Budinoff 

En la gran mayoria de los articulos hacian los alineamientos con ClustalX 
busque y este sofware pude correrse en la  linea de comandos:

![](./clustalX_CommandLine) 


-Chequé el repositorio de un dude que ofrecía una paqueteria de R para análisis filogenéticos (phytools) espero me ayude a correr algunos analisis en R, ya que en los comentarios del Avance 1, se me suguirió incorporar los analisis a linea de comando o en R. 

	[](http://blog.phytools.org/)
	
	pero aun me falta checar bien que analisis ofrece... 

####Y hasta ahí voy

El siguiente paso será empezar a pasar los pasos a un script 
y checar si de otros programas de análisis filogenéticos hay forma de correrlos en linea de comandos, ejemplos de estos: TNT, PAUP, MrBAyes McClade, etc. 

:)

