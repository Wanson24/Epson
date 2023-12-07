# Epson

 
	TITULO 
TIPO 	Guía Práctica EPSON RC + 7.0 - Básica 
EQUIPO 	SCARA T6 
FECHA ELABORACIÓN 	13-10-2023 
ING ENCARGADO CDM 	Ing. Diego Castro 
 
Recursos: 
•	Software EPSON RC + 7.0 – Versión 7.5.2 
•	Robot SCARA T6 
Objetivo General:  lograr consolidar en el estudiante, los conocimientos básicos para la puesta en marcha de un Robot SCARA T3 o T6 de EPSON, por medio del software EPSON RC + 7.0.  
Objetivos Específicos: 
•	Consolidar como realizar la instalación física y eléctrica del robot, y los requisitos para energizarlo. 
•	Conexión al software EPSON RC + 7.0. 
•	Afianzar manejo del Robot Manager.  
•	Consolidar el uso de los comandos Go, Move, Jump, Pallet y Pallet Outside, en el simulador y con el Robot. 
Tomar como referencia para la realización de esta practica la presentación : 
Capacitación básica EPSON RC + 7.0 SCARA SERIE T 131023 
Practica Simulador: 
1.	Abrir EPSON RC + 7.0, crear una conexión virtual y configurar un robot SCARA T6 en la 
Configuración del Sistema (Presentación: Pág. 62-74). 
 
  
 
 
2.	Abra un proyecto nuevo y luego con el Robot Manager configure una posición de home como en la siguiente imagen: 
 
   
3.	Crear tres puntos por medio de las herramientas de JOG&TEACH, con las siguientes coordenadas (Presentación: Pág. 87). 
 
   
4.	Realizar un programa en SPEL+ con la estructura básica mencionada en la presentación, que haga navegar al robot entre los tres puntos creados, con un retardo entre movimientos de 500 ms,  por medio del comando Go, seguidamente con Jump y luego Move, dentro de un bucle infinito (Presentación: Pág. 99-106).  
 
   
 
 
 
 
5.	Genere una función llamada “paletizado_z”, configure un Pallet con el comando del mismo nombre, de 3 x 3 posiciones, y luego de terminar de ejecutar los movimientos del punto anterior, llame esta función de “paletizado_z” y ejecute un bucle FOR que navegue por las nueve posiciones con el comando Jump en orden ascendente (Presentación: Pág. 120-121). 
 
6.	Programe una segunda función llamada “paletizado_s”, en el que recorra las nueve posiciones generando un Track Render en forma de “S”, es decir, recorrer las posiciones de la siguiente manera: 1,2,3,6,5,4,7,8,9. Esta función será ejecutada después de “paletizado_z”. 
 
 
7.	Codifique un condicional que ejecute el “paletizado_z” solo si la entrada digital número 9 esta en ON, y otro que ejecute “paletizado_s” solo si la entrada digital número 10 está en ON. Además programe dos salidas digitales, 11 y 12, para cuando se esté ejecutando  “paletizado_z” y “paletizado_s” respectivamente. 
 
	 	 
 
 
8.	Genere una tercera función llamada “paletizado_externo”, en el cual se utilizará el comando Pallet Outside, para configurar con los mismos 3 puntos creados al inicio, un pallet que agregue una cuarta fila y columna que vaya más allá del espacio circunscrito entre los puntos. Genere una rutina dentro de esta función que permita que el robot navegue por los 16 puntos del pallet. Esta función se ejecutará solo si la entrada digital 11 está activada. 
 
 
Practica Robot SCARA T6: 

9.	Verifique la instalación mecánica y eléctrica de ROBOT SCARA T6, verifique que el pulsador de emergencia este activado y energice el robot.(Presentación:Pág. 36-38).

10.	Abra el software EPSON RC + 7.0, cierre cual cualquier proyecto abierto, y conéctese por medio del puerto USB al robot. (Presentación:Pág. 126). 
11.	Abra el proyecto que creo en la práctica con el simulador, luego con el Robot Manager configure una posición de home como en la siguiente imagen:
 
12.	En el código que desarrollo anteriormente, comente las líneas concernientes a velocidad, aceleración y desaceleración, y repítalas, pero limitadas a un 30% para Accel y Speed, y 100 para AccelS y SpeedS. Ejecute “Run Windows”, y active el checkbox de “Low Power”, a continuación ejecute el programa.  
 




https://github.com/Wanson24/Epson/assets/144077425/705951ea-b1e5-48fc-9af6-0577b4dc8c8e

