
# 🔢 Ejemplos de Algoritmos con Estructuras Secuenciales  

Desarrollé ejercicios en **PSeInt** y **C**, aplicando instrucciones en orden.  

>En esta unidad realice varios ejercicios para aplicar los algoritmos secuenciales, donde las instrucciones se ejecutan unas tras otra en orden. A continuación, presento dos ejemplos que se desarrolle en PSeInt y luego en C.

>***Captura Nro.1-2: Ejemplos de la estrucutura del pseudocodigo en PseInt y C***

<img width="350" height="300" alt="image" src="https://github.com/user-attachments/assets/367c94dc-61ef-4d71-b5d5-59b3cc8ea438" />
<img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/10b93e4c-7a5d-40af-9048-18778bc83aa7" />


### 🧮 Ejemplos de Pseudocódigo PSeInt y C
#### Ejercicio Nro.1 Calcular el Tiempo y Aceleracion de un Vehiculo.
>El primer ejercicio consiste en calcular el tiempo que tarda un vehículo en recorrer una distancia. Tenía los datos de la fuerza, la masa y las velocidades inicial y finales. Usando las fórmulas de la física, calcula la aceleración y luego el tiempo con la ecuación. El algoritmo siguió tres pasos: en la entrada recibe los datos de la fuerza, masa, velocidades inicial y final, en el proceso realizada los cálculos en las respectivas formulas y la salida muestra el valor de la aceleración y tiempo. Este ejercicio me ayudó a ver cómo las fórmulas se pueden convertir en pasos lógicos dentro de un programa.

***Pseudocodigo de PseInt***

```python
Algoritmo Calcular_el_Tiempo_Aceleracion_de_un_Vehiculo
	//1.Un usuario quiere determinar el tiempo que tarde en recorrer su vehículo, 
	// pero solo consta con los datos de la fuerza "N", la masa "Kg" de su vehículo, 
	// también con la velocidad inicial "m/s" y la velocidad final "m/s", 
	// realizar un programa donde al usuario se le muestre el tiempo que tardo en recorrer con su vehículo.
	
	//Tipos de Datos
	Definir aceleracion_vehiculo,masa_vehiculo,fuerza_vehiculo,tiempo_vehiculo,velocidad_incial_vehiculo,velocidad_final_vehiculo Como Real
	
	//Entrada
	Escribir "Ingrese la fuerza que realizo su vehiculo (N):";
	Leer fuerza_vehiculo;

	Escribir "Ingrese la masa de su vehiculo (kg):";
	Leer masa_vehiculo;
	
	Escribir "Ingrese la velocidad inicial que realizo su vehiculo (m/s):";
	Leer velocidad_incial_vehiculo
	
	Escribir "Ingrese la velocidad final que realizo su vehiculo (m/s):";
	Leer velocidad_final_vehiculo
	
	// Proceso 
	aceleracion_vehiculo= fuerza_vehiculo/masa_vehiculo; //Formula despejada F=m*a
	
	tiempo_vehiculo = (velocidad_final_vehiculo-velocidad_incial_vehiculo)/aceleracion_vehiculo; //Formula despejada a= Vf-Vi/t
	
	// Salida
	Escribir "La aceleracion de su vehiculo es (m/s^2):", aceleracion_vehiculo;
	Escribir "El tiempo de su vehiculo es (s) ", tiempo_vehiculo;
FinAlgoritmo
```
***Pseudocodigo  en C***
```python
/*1.Un usuario quiere determinar el tiempo que tarde en recorrer su vehículo, pero 
solo consta con los datos de la fuerza "N", la masa "Kg" de su vehículo, también 
con la velocidad inicial "m/s" y la velocidad final "m/s", realizar un programa 
donde al usuario se le muestre el tiempo que tardo en recorrer con su vehículo.*/

#include <stdio.h>

int main(){
    //Definir Datos
float aceleracion_vehiculo,masa_vehiculo,fuerza_vehiculo,tiempo_vehiculo,velocidad_incial_vehiculo,velocidad_final_vehiculo;

    //Entrada
printf("Ingrese la fuerza que realizo su vehiculo (N): \n");
scanf("%f", &fuerza_vehiculo);
printf("Ingrese la masa de su vehiculo (kg): \n");
scanf("%f", &masa_vehiculo);
printf("Ingrese la velocidad inicial que realizo su vehiculo (m/s): \n");
scanf("%f", &velocidad_incial_vehiculo);
printf("Ingrese la velocidad final que realizo su vehiculo (m/s): \n");
scanf("%f", &velocidad_final_vehiculo);

    //Proceso
aceleracion_vehiculo= fuerza_vehiculo/masa_vehiculo; //Formula despejada F=m*a = a=f/m
	
tiempo_vehiculo= (velocidad_final_vehiculo-velocidad_incial_vehiculo)/aceleracion_vehiculo; //Formula despejada a= Vf-Vi/t t= Vf-Vi/a

    //Salida
printf ("La aceleracion de su vehiculo es: %2.fm/s^2\n",aceleracion_vehiculo);
printf ("El tiempo de su vehiculo es: %2.fs\n",tiempo_vehiculo);
return 0;
}

```

>***Captura Nro.3: Diagrama de Flujo***

<img width="400" height="500" alt="image" src="https://github.com/user-attachments/assets/0c029f87-4d1d-481f-8e07-820aecc7bb25" />

>***Captura Nro.4: Ejecucion en Pseint y C***

> Se puede observar como en ambos lenguajes el programa se ejecuta correctamente sin ningun error, ademas en C se aprecia la copilacion y ejecucion del codigo
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/904cd076-9437-423f-9e89-34cdc9dbc4f8" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/245b8092-b440-4702-8e01-562c40dd3c8f" />

>***Captura Nro.5: Pruebas de Escritorio***

<img width="500" height="450" alt="image" src="https://github.com/user-attachments/assets/b4b91e0e-adeb-4a71-8eec-1ac3843dfeb0" />

#### Ejercicio Nro.2 Porcentaje de Poder
>El segundo ejercicio fue mas creativo: calcular el poder total de un personaje de videojuego. Su poder aumentaba un 55% pero los enemigos lo reducían un 30%. El programa debía mostrar el poder final después de aplicar ambos porcentajes. En este algoritmo, la entrada es el poder base del personaje. Durante el proceso, se calcula primero el aumento del 55%, luego se suma al poder base y después se aplica una reducción del 30% causada por los enemigos. Finalmente, la salida muestra el poder total que tendrá el personaje al finalizar la batalla.


>***Captura Nro.6: Pseudocodigo de PseInt***
```python
Algoritmo Porcentalidad_Poder
	//El usuario quiere determinar el porcentaje total de poder que tendrá, su personaje favorito de su videojuego, 
	//al momento que este active una habilidad, donde dice que su poder, aumenta en un 55%, pero los enemigos 
	//contrarrestan ese poder con un objeto que le reduce su poder en un 30%, ¿cuál será el poder total que tendrá su personaje en batalla? 
	
	//Tipos de Datos
	Definir aumento_de_poder, disminucion_de_poder,poder_base Como Real
	
	//Entrada
	Escribir "Ingresa el poder base que tiene su personaje";
	Leer poder_base;
	
	//Proceso
	aumento_de_poder= (poder_base*155)/100; // 100%+55% = 155%
	disminucion_de_poder= (aumento_de_poder*70)/100; //100%-30% = 70%
	
	//Salida
	Escribir "Su personaje aumentara su poder en:",aumento_de_poder;
	Escribir "Su personaje disminuira su poder en:",disminucion_de_poder
	
FinAlgoritmo
```
>***Captura Nro.7: Pseudocodigo  en C***
```python
/*El usuario quiere determinar el porcentaje total de poder que tendrá, su personaje favorito de su videojuego, al momento 
que este active una habilidad, donde dice que su poder, aumenta en un 55%, pero los enemigos contrarrestan ese poder con 
un objeto que le reduce su poder en un 30%, ¿cuál será el poder total que tendrá su personaje en batalla?*/

#include <stdio.h>

int main(){

//Definir Datos
float aumento_de_poder, disminucion_de_poder,poder_base;

//Entrada
printf("Ingrese el poder base de su personaje: \n");
scanf("%f",&poder_base);

//Proceso
aumento_de_poder= (poder_base*155)/100;  // 100%+55% = 155%
              
disminucion_de_poder= (aumento_de_poder*70)/100;  //100%-30% = 70%

printf ("Su personaje aumentara su poder en un valor de:%2.f\n",aumento_de_poder);
printf ("Su personaje disminuera su poder en un valor de:%2.f\n",disminucion_de_poder);


return 0;
}
```
>***Captura Nro.8: Diagrama de Flujo***

<img width="400" height="500" alt="image" src="https://github.com/user-attachments/assets/5070720f-bdae-44ec-b70f-da9d2b6918e8" />

>***Captura Nro.9: Ejecucion en Pseint y C***

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/24afbf7a-6ec8-440c-8dd9-89df90f45187" />
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/a176a0d9-92e5-426f-a852-613c7df3ef18" />

>***Captura Nro.10: Pruebas de Escritorio***

<img width="500" height="450" alt="image" src="https://github.com/user-attachments/assets/59e290c9-6a64-4197-8a6f-97542d820c2b" />


>Los escribí primero en PSeInt, para comprobar la lógica, y luego lo programé en C, viendo cómo los cálculos se mostraban correctamente en pantalla. Ambos ejercicios me ayudaron a reforzar el pensamiento lógico, la secuencia de pasos y la forma en que los programas funcionan internamente para resolver problemas reales y cotidianos.


[🔢 Ir a los ejemplos](https://drive.google.com/drive/folders/1Xqky4Df5yLluXnuHkBSvUvoEFzRBBqPj?usp=sharing)

#### Nota 1. Porque se debe realizar las pruebas de escritorio?

#### Nota 2. Cuales son los pasos para copilar y ejecutar el codigo en C?

[⬅️ Volver al índice de la Unidad 1](unidad1.md)
