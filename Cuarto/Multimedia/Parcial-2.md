# PARCIAL 2

## Compresión sin perdida

### Codificación Huffman

* Código prefijo
* Óptimo
* Simbolos mas frecuentes igual a menos longuitud
* Solo cambia el último bit

![Screenshot_20231211_133436](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/c0a3a262-e2e0-4337-9a37-93c626c4b66c)

### Huffman mínima varianza

* Hace que el anterior metodo sea óptimo cuando tenemos mucho de 1 letra, ya sea por que sobra o porque falta.

![Screenshot_20231211_133712](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/ffd6a255-1318-4262-91c1-479051762f93)

### Codificación Tunstall

* Todas las palabras clave tienen la misma longuitud
* Código prefijo

#### Pasos

![Screenshot_20231211_134532](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/eef1d602-4a78-4733-85fd-c57620954dac)

* Comprobamos si la formula es verdadera y en caso de que si expandimos el nodo con mayor probabilidad

![Screenshot_20231211_134920](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/3ca7e691-7959-4d77-8999-0500b9321aac)

* Recalculamos probabilidades y seguimos expandiendo mientras la formula sea correcta

![Screenshot_20231211_135330](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/2fc24c58-c1d8-4495-be71-9401d90b8f32)

* Como el código es de 3 bits asignamos como queramos valores a cada cadena

![Screenshot_20231211_135521](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/ed7203cb-8b43-4c70-8f16-fe672b38a81e)

* Por último como tenemos 2 cadenas sin asginar le asignamos el código indererminado + el código fijo

![Screenshot_20231211_135745](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/0de247b5-336e-45b4-acd3-55b320c23d30)

### Codificación Aritmética

* Tenemos tantos intervalos disjuntos en [0,1) iniciales como letras tenga el alphabeto

#### Pasos

![Screenshot_20231211_141025](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/2ebaa2d0-ebe8-4035-88c4-26c937c664cb)

* Funciones de distribución

![Screenshot_20231211_141216](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/c081ac5f-5082-4293-9010-686bb73633fe)

* Sustituimos la cadena por números

![Screenshot_20231211_141325](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/1f44c251-8063-4396-875b-079078d96913)

* Definimos los casos base

![Screenshot_20231211_141417](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/64aaec2f-a877-415f-b800-f3554fc1b70c)

* Ahora aplicamos el algoritmo recursivo para calcular el Límite inferior y superior

![Screenshot_20231211_141816](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/73afd410-c235-44f2-b82c-315cf14523a1)

![Screenshot_20231211_141948](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/023e4629-7011-4a3c-8d69-d327089939a8)

* Según el ejemplo seria:

![Screenshot_20231211_141612](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/dd5f32c7-9bff-4238-a406-18027b36a83d)


![Screenshot_20231211_142136](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/2a953f77-7eb5-40e6-b805-b588af9e92bd)


![Screenshot_20231211_142159](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/9e15c205-940e-44af-b44c-7660bfc7ef88)


![Screenshot_20231211_142233](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/7255bed5-03ad-432e-9de4-d33a7d3795b5)


![Screenshot_20231211_142311](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/e1241b28-df4a-4aee-a2d9-46b660d72ffa)

* Por último obtenemos un valor de esa franja

![Screenshot_20231211_142400](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/5902d3ca-f278-4352-a114-fe89e5c7b1af)

### Codificador adaptativo aritmético

* La probabilidad se calcula en funcion de la llegada de letras

### Codificador LZ77

* Coges la cadena de caracteres y la vas avanzando y creando patrones con el conjunto (P,L,C)
    * P= estado inicial del patron dentro del diccionario (El buffer) desplazandote a la izq desde dnd esta el separador
    * L= Cantidad de caracteres que tienes que leer despues de dezplazarte
    * C= La letra siguiente que cojes
* Puedes coger hasta valores despues del separador si te coinciden


![Screenshot_20231211_172139](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/2861ce5b-7b9c-46a2-bc92-ae21eef59726)

### Codificador LZ88

* Avanzas añadiendo patrones al diccionario (Los añades todos) asi creas un diccionario

![Screenshot_20231211_172655](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/0dbd521f-2297-434e-84ba-81ea7b3738f4)

* Se crea una dubla (P,C)
  * P = Corresponde al indice del patro por el q empiece (Si quitas la ult letra q sera la C lo que teienes en ese patron ya esta en el diccionaio con un indice pues el q sea)
  * C = Valor final del patron añadido al diccionario

* Se le da valores binarios

![Screenshot_20231211_173132](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/0f4e310a-4269-4403-987e-8e40f5c485ff)

### Codificador LZW

* El diccionario empieza precargado con 256 entradas del ASCII y una para el fin de archivo

### Otros métodos


![Screenshot_20231211_175317](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/d25bd2ab-9782-4a43-a92e-aca0b7c156f2)

