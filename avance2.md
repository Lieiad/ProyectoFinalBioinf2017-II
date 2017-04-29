## Proyecto final Bioinf2017-II

### Avances
Hasta este momento se ha descargado los 27 especies que constituyen el proyecto PRJNA298058 en SRA de NCBI, de los datos obtenidos por Zhang *et al.* (2015) para la familia Vitaceae. Estos datos se descargaron mediante un loop en formato sra y, han sido convertidos en fastaq.gzip mediante sra_toolkit/fastq_dump. 
Se han obtenido las imágenes para Velvet y Bowtie2 de Biocontainers (ver referencias), así como leído la literatura asociada a su funcionamiento y manuales respectivos. Aún falta conocer en más detalles las opciones para los *paired-end runs*, que son el tipo de datos crudos que obtuvieron Zhang *et al.* (2015). 
Hasta ahora sólo he 
aventurado comandos con velvet sobre una de las especies, como 
```velveth K ```, que es para probar una longitud determinada del k-mero, a partir de la cual construir la gráfica de Bruijin.

He leído que Velvet requiere mucha memoria para correr los análisis. En un principio, quería reproducir los análisis de Ripma *et al.* (2014) con los datos de Zhang, pero en vista del tiempo que puede llevar sólo el ensamblaje *de novo*, además de que los métodos de ambos artículos están un poco oscurecidos, estoy optando por reproducir únicamente el método de Zhang *et al.* (2015). En principio estaba en duda si llegaría a los análisis filogenéticos. Ahora estoy dudando de hacer los ensamblajes *de novo* con las 27 especies o, enfocarme en un menor número, quizá cinco, pero probar más opciones que ofrecen los programas al momento de ensamblar, y también en la obtención de plastomas. Es decir, sacrificar cantidad en búsqueda de dominar -por decirlo así- los programas y opciones, lo cual servirá cuando obtenga datos propios. Lo anterior me genera la duda sobre qué gráfica puedo presentar, ya que mayormente estaría recuperando secuencias anotadas y homólogas, que son de interés filogenético. Ya Ripma *et al.* (2014) lo advierten cuando dicen que los plastomas obtenidos no son para estudiar evolución molecular.

Lo anterior es la justificación para un cambio de objetivos iniciales.

También se han leído otros trabajos que usan Genome Skimming con objetivos de diversificación, además de lo filogenético.  


#### Referencias consultadas
+ Bock D. G., N. C. Kane, D. P. Ebert & L. H. Rieseberg. 2014. Genome skimming reveals the origin of the Jerusalen Artichoke tuber crop species: neither from Jerusalem nor an artichoke.  *New Phytologist* **201**: 1021-1030.
+ Dodsworth S. 2015. Genome skimming for next-generation biodiversity analysis. *Trends in plant science* **20**(9):525-527.
+ Langmead B. Manual Bowtie 2 -version 2.3.1. Disponible en http://bowtie-bio.courceforge.net/bowtie2/manual.shtml
+ Ripma L. A., M. G. Simpson & K. Hasenstab-Lehman. 2014. Geneious! Simplified genome skimming methods for phylogenetic systematic studies: a case study in *Oreocarya* (Boraginaceae). *Applications in Plant Sciences* **2**(15): 1400062.
+ Zerbino D. R. & E. Birney. 2008. Velvet: Algorithms for *de novo* assembly using de Bruijin graphs. *Genome Research*  **18**(5):821-829.
+ Zerbino D. 2008. Velvet Manual - version 1.1. Disponible en http://www.ebi.ac.uk/~zerbino/velvet/Manual.pdf
+ Zhang N., J. Wen & E. A. Zimmer. 2015. Congruent deep relationships in the grape family (Vitaceae) based on sequences of chloroplast genomes and mitocondrial genes via genome skimming. *PLoS* *ONE* **10**(12): e0144701. 
+ Zimmer E. A. & J. Wen. 2015. Using nuclear gene data for plant phylogenetics: Progress and prospects II. Next-gen approaches. *Journal of Systematics and Evolution* **53**(5): 371-379.
+ https://github.com/BioContainers/sandbox/blob/master/velvet/1.2.10/Dockerfile
+ https://github.com/BioContainers/containers/tree/master/bowtie2
