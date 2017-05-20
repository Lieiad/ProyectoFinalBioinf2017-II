### README


A continuación se explica la organización del proyecto, los directorios que lo conforman y el orden de los scripts a correr. 

**Nota:** Los programas Fastqc, Trimmomatic y Velvet se corrieron en un contenedor de Docker, el primero obtenido de Biocointainers. Los últimos en un entorno Ubuntu en el que fueron instalados los programas. 

**Directorios**

+ **Bin.** Contiene los scripts a correr en cada programa. Están nombrados iniciando por el número en que deben ser corridos:
    1. Obtener las secuencias crudas de la base de datos de SRA de NCBI, por medio de sra_toolkit.
    2. Evaluar la calidad de las secuencias con Fastqc.
    3. Realizar el filtrado de calidad con Trimmomatic, dependiendo de los resultados observados en Fastqc.
    4. Correr Velveth de Velvet, con la creación de carpetas de acuerdo al k-mero indicado.
    5. Correr Velvetg de Velvet, para obtener el ensamblaje final de acuerdo al valor del k-mero usado con Velveth.
    6. Observar el ensamblaje con la versión gráfica de Mauve y compararlo con alguna secuencia conocida de un organismo cercano.


+ **Data.** Este directorio está dividido en los siguientes subdirectorios:
     1. *SRA_fastq_gz*. Contiene las secuencias crudas descargadas de SRA NCBI. Al ser lecturas pareadas, existe una carpeta correspondiente a cada especie con dos archivos fastaq comprimidos en formato qzip. 
      2. *Fasqc_report*. Informes iniciales de las sequencias tras correr Fastqc por especie (cada informe en su respectiva carpeta por especie).
      3. *Trimmomatic*. Secuencias una vez aplicados los filtros de calidad. A su vez, subdirectorios por especie que contengan un informe de Fastq tras el uso de Trimmomatic.
      4. *Velvet*. Los resultados de correr Velvet. Es el subdirectorio más extenso, ya que está dividido en subdirectorios por especie, los cuales a su vez, están divididos por directorios que indican el k-mero empleado para hacer el análisis.
      5. *Genomas*. Los genomas finales, divididos en directorios por especie y k-mero empleado.
      
+ **Metadata.** Los datos de las corridas del proyecto depositado en SRA del que se obtuvieron las secuencias crudas, en un archivo de texto con formato csv. Información adicional sobre la biología de los organismos empleados. Informes sobre las secuencias, proporcionados por los programas corridos.

+ **Images**. Gráficas e imágenes, producto del trabajo. Al interior:
	+ *Bin*. Scripts para realizar cualquier gráfica producida.
	
