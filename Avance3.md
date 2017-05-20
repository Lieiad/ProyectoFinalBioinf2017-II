## Proyecto final Bioinf2017-II

### Avances

Tras conocer en carne viva a qué se refería Zerbino (2008) con que más de 12 GB de memoria RAM para correr Velvet no era lujuría, aunque se tengan los scripts preparados para sólo dejarlos correr y obtener los genomas ensamblados de algunas especies de Vitaceae de los datos de Zhang *et al.* (2015), utilizando diferentes longitudes del valor *k*, esta aspiración se declina puesto que en más de dos semanas no se ha terminado de crear el *Roadmap* por ```velveth``` para **una sola especie**, a partir del cual se creará la gráfica de Bruijin para realizar el ensamblaje.  

Dadas estas circunstancias, aunque se ha aprendido mucho en la instalación y manejo de varios programas, como sra_toolkit de NCBI para bajar las secuencias crudas; Fastqc, para evaluar la calidad de las secuencias; Trimmomatic, para recortar éstas; Velvet, para realizar el ensamblaje *de novo* y, Mauve, para visualizar la calidad del ensamblaje y compararlo con un genoma de referencia, se pretende realizar los pasos anteriores con un genoma mas pequeño, como el de una bacteria, para terminar de aprender este proceso (como intención principal y última de este trabajo final).

Aun cuando se ha dejado correr el programa para completar el ensamblaje del genoma de *Leea guineensis* (Vitaceae), en este momento lleva 4,382,185 lecturas de 17,410,966, con un uso de memoria de 90% (lo cual se dejará registrado como una captura de pantalla).

La revisión de bibliografía para un genoma más asequible a los recursos de mi computadora (8 GB de memoria RAM), no permite siquiera aventurar a ensamblar una angiosperma para el tiempo disponible de este trabajo final. El genoma más pequeño registrado pertenece a *Genlisea margaretae* (Lentibulariaceae), con 63 Mbp (Greilhuber *et al.* 2006). Genomas de bacterias, como *Bartonella*, rondan un máximo de 2.6 Mpb (Engel & Dehio, 2009) y son, por el momento, la elección para llegar al final del proceso de ensamblaje. De esta suerte, se desea presentar un genoma ensamblado; probar, si es posible dado el cómputo requerido, algunos valores de *k* y, hacer una gráfica que compare las calidades de los genomas obtenidos con base en estos valores. De no poder manejar varios valores de *k*, al menos se espera poder obtener un genoma y compararlo con alguno publicado de la misma especie utilizando Mauve y quizá, el paquete genoPlotR de R (Guy *et al.* 2010).

Hay genomas de bacterias disponibles en SRA  bajo el proyecto PRJNA231221.

El [README](https://github.com/Lieiad/ProyectoFinalBioinf2017-II/blob/master/Readme.md)  del proyecto en construcción. Es un esquema general, será modificado para dar cabida a esta última opción o meter ambos conjuntos de script.

![alt text](https://github.com/Lieiad/ProyectoFinalBioinf2017-II/blob/master/Captura%20de%20pantalla%20de%202017-05-19%2022:48:19.png)
![alt text][image]
[image]: https://github.com/Lieiad/ProyectoFinalBioinf2017-II/blob/master/Captura%20de%20pantalla%20de%202017-05-12%2008:02:21.png


#### Referencias

+ Engel P. & C. Dehio. 2009. Genomics of Host-Restricted Pathogens of the Genus *Bartonella*. *Genome Dyn. Basel, Karger* **6**: 158-169.
+ Guy L., J. R. Kultima & S. G. Andersson. 2010. genoPlotR: comparative gene and genome visualization in R. *Bioinformatics Applications Note* **26**(18): 2334-2335.
+ Greilhuber J., T. Borsch, K. Müller, A. Worberg, S. Porembski & W. Barthlott. 2006. Smallest Angiosperm Genomes Found in Lentibulariaceae, with Chromosomes of Bacterial Size. *Plant Biology* __8__: 770-777.
+ Zerbino D. 2008. Velvet Manual - version 1.1. Disponible en http://www.ebi.ac.uk/~zerbino/velvet/Manual.pdf
+ Zhang N., J. Wen & E. A. Zimmer. 2015. Congruent deep relationships in the grape family (Vitaceae) based on sequences of chloroplast genomes and mitocondrial genes via genome skimming. *PLoS* *ONE* **10**(12): e0144701. 



