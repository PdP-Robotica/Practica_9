# Practica_9

## Integrantes:
- **Luis Fernando Duarte Reséndiz**
- **Mauricio Alberto Gómez Arroyo**
- **Diego Brandon Guzmán Sierra**
- **Bryan Hiadim Vera Hernández**

## Introducción:
Los brazos robóticos son herramientas esenciales en la automatización industrial debido a su precisión y eficiencia en tareas repetitivas. Uno de los usos clave de estos sistemas robóticos es en el acomodo de piezas, como bloques y fusibles, en procesos de ensamblaje o producción. Estos brazos robóticos, como el modelo Epson C4, pueden realizar movimientos controlados y precisos para manipular componentes, asegurando que cada pieza se coloque en su posición específica sin error. Este tipo de automatización es particularmente útil en industrias que requieren ensamblajes eléctricos o electrónicos, donde el manejo preciso de fusibles y bloques es fundamental para mantener la integridad del producto final y reducir tiempos de producción.

La precisión y repetitividad de los brazos robóticos permiten optimizar estos procesos, logrando una distribución y colocación uniforme de los componentes sin errores comunes en los procesos manuales. Además, el uso de brazos robóticos en tareas como estas minimiza el riesgo de accidentes, mejora la eficiencia en la línea de producción y reduce los costos a largo plazo, al eliminar la variabilidad humana. Por estas razones, los brazos robóticos se han convertido en una solución altamente efectiva para aplicaciones de ensamblaje y acomodación de piezas en múltiples sectores industriales.

## Instrucciones.
1. Lo primero que haremos será descargar las posiciones proporcionadas por el profesor. En este archivo encontraremos las ubicaciones de las cajas rojas y de los fusibles, además de la trayectoria que el robot deberá seguir para tomar cada uno de los elementos necesarios para realizar la práctica.
 ![image](https://github.com/user-attachments/assets/0748df88-803b-4d44-9b4b-4a1a057e0ef9)

2. Una vez que descarguemos el archivo, abriremos un nuevo archivo en Epson RC+, donde importaremos todas las posiciones que descargamos anteriormente. Devido a la gran cantidad de posiciones que tenemos para esta practica no se mostran detalladamente estos puntos.

3. Una vez que tengamos los puntos, comenzaremos con la programación del robot para realizar lo indicado, que consiste en agarrar dos cajitas de fusibles rojas, las cuales tienen dos espacios para fusibles. En ellas vamos a colocar estos dos fusibles. A continuación, se mostrará el código utilizado para realizar dicha práctica.
```plaintext
Function main
	Reset
	Motor On
	Home
	Power High
	Speed 30
	Accel 30, 30
	SpeedS 600
	AccelS 6000, 6000
	
	On 2
	Go Caja_Izq_4 CP
	Go Caja_Izq_3 CP
	Go Caja_Izq_2 CP
	Go Caja_Izq_1
	Off 2
	Go Caja_Izq_1
	Go Caja_Izq_2 CP
	Go Caja_Izq_3 CP
	Go Caja_Izq_4 CP
	
	Go Base1_4 CP
	Go Base1_3 CP
	Go Base1_2 CP
	Go Base1_1
	On 2
	Go Base1_1
	Go Base1_2 CP
	Go Base1_3 CP
	Go Base1_4 CP
	
	Go Caja_Der_4 CP
	Go Caja_Der_3 CP
	Go Caja_Der_2 CP
	Go Caja_Der_1
	Off 2
	Go Caja_Der_1
	Go Caja_Der_2 CP
	Go Caja_Der_3 CP
	Go Caja_Der_4 CP
	
	Go Base2_4 CP
	Go Base2_3 CP
	Go Base2_2 CP
	Go Base2_1
	On 2
	Go Base2_1
	Go Base2_2 CP
	Go Base2_3 CP
	Go Base2_4 CP

	Go Fusible1_izq_4, Fusible1_izq_3, Fusible1_izq_2 CP
	Go Fusible1_izq_1
	Off 2
	Go Fusible1_izq_1, Fusible1_izq_2, Fusible1_izq_3, Fusible1_izq_4 CP
	
	Go Base1_Fus_Izq_4, Base1_Fus_Izq_3, Base1_Fus_Izq_2 CP
	Go Base1_Fus_Izq_1
	On 2
	Go Base1_Fus_Izq_1, Base1_Fus_Izq_2, Base1_Fus_Izq_3, Base1_Fus_Izq_4 CP
	
	Go Fusible2_izq_4, Fusible2_izq_3, Fusible2_izq_2 CP
	Go Fusible2_izq_1
	Off 2
	Go Fusible2_izq_1, Fusible2_izq_2, Fusible2_izq_3, Fusible2_izq_4 CP
	
	Go Base1_Fus_Der_4, Base1_Fus_Der_3, Base1_Fus_Der_2 CP
	Go Base1_Fus_Der_1
	On 2
	Go Base1_Fus_Der_1, Base1_Fus_Der_2, Base1_Fus_Der_3, Base1_Fus_Der_4 CP
	

	Go Fusible1_Der_4, Fusible1_Der_3, Fusible1_Der_2 CP
	Go Fusible1_Der_1
	Off 2
	Go Fusible1_Der_1, Fusible1_Der_2, Fusible1_Der_3 CP
	Go Fusible1_Der_4
	
	Go Base2_Fus_Izq_4, Base2_Fus_Izq_3, Base2_Fus_Izq_2 CP
	Go Base2_Fus_Izq_1
	On 2
	
	Go Base2_Fus_Izq_1, Base2_Fus_Izq_2, Base2_Fus_Izq_3, Base2_Fus_Izq_4 CP
	
	Go Fusible2_Der_4, Fusible2_Der_3, Fusible2_Der_2 CP
	Go Fusible2_Der_1
	Off 2
	Go Fusible2_Der_1, Fusible2_Der_2, Fusible2_Der_3, Fusible2_Der_4 CP
	
	Go Base2_Fus_Der_4, Base2_Fus_Der_3, Base2_Fus_Der_2 CP
	Go Base2_Fus_Der_1
	On 2
	Go Base2_Fus_Der_1, Base2_Fus_Der_2, Base2_Fus_Der_3, Base2_Fus_Der_4 CP
	
	Home
Fend
```
4. Teniendo el código, lo siguiente será probarlo en el robot para observar si realiza lo indicado o no. El orden consiste en acomodar primero las dos cajitas y luego colocar los dos fusibles en la primera, seguidos de los dos fusibles en la segunda.

## Video de ejecución de práctica
https://github.com/user-attachments/assets/53c41f64-6439-4aaf-8fa4-143521592e80

## Conclusión:
- **Luis Fernando Duarte Reséndiz**
El uso de brazos robóticos, como el Epson C4, permite mejorar la precisión y eficiencia en el acomodo de piezas delicadas como bloques y fusibles, reduciendo errores y tiempos de producción.
  
- **Mauricio Alberto Gómez Arroyo**
La incorporación de tecnología robótica en tareas de acomodo mejora significativamente la productividad, permitiendo que los trabajadores enfoquen sus habilidades en tareas más complejas y de mayor valor agregado.
  
- **Diego Brandon Guzmán Sierra**
Implementar robots para el acomodo de componentes es una solución segura y efectiva para la industria, ya que disminuye los riesgos asociados a la manipulación manual de piezas pequeñas.
  
- **Bryan Hiadim Vera Hernández**
La automatización de tareas de ensamblaje mediante brazos robóticos asegura una colocación uniforme y precisa de los componentes, minimizando la variabilidad y aumentando la confiabilidad en el proceso.

## Referencias.
[1] De proyectos, A. y. D. (s/f). Manual del usuario. Epson.com. Recuperado de https://files.support.epson.com/far/docs/epson_rc_pl_70_users_guide_spanish_(v73r2).pdf

[2] Robot Epson C4 de 6 ejes compactos. (s. f.). Productos | Epson México. https://epson.com.mx/Para-el-trabajo/Rob%C3%B3tica/6-Ejes/Robot-Epson-C4-de-6-ejes-compactos/p/RC4-A601ST75
