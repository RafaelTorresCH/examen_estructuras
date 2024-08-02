# examen_estructuras
Este codigo busca a traves de 2 botones( izquierdo_A1 y derecho_A3), parpadear los leds de la placa arduino shield correspondiente un led
a cada boton, para eso se dejaron los dos botones como interrupciones del sistema, se activaron en el NVIC y y se dejaron definidas en el 
flanco de bajada falling edge.
Se uso la funcion callback para retornar el boton oprimido, y se activa la bandera correcpondiente con el numero de estados 
on y off del led respectivo al boton, para este caso, 6 veces(3 ON 3 OFF)
despues de eso se crearon las funciones encargadas de generar los cambios de estados, y reducir la bandera del boton correspondiente a cero
esto con el fin de terminar las ejecuciones, para detectar el tiempo que ha pasado se utiliza la condicion de que el ultimo segundo sea menor que el segundo actual para ejecutar la accion, tener en cuenta que el segundo actual inicia en cero y se le suman 500 millis si la bandera sigue en alto(>0)
Z
