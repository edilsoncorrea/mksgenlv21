## Offset do Eixo Z
A diferença entre a ponta do bico e a ponta da sonda quando está liberada chama-se offset. 

![Z_Offset](/Z_offset.jpg "Z Offset")

### Quando o sensor de auto nivelamento também é o endstop do eixo Z

Em impressoras com BLTouch ou 3D Touch o ponto zero do eixo Z da mesa é determinado pela sonda, ou seja, o sensor de nivelamento também atua como endstop do Eixo Z. Sendo assim, quando executamos um Auto Home e os 3 eixos ficam em 0, a sonda está exatamente no mesmo nível da mesa. O eixo Z está zerado.

Se executarmos um comando que sobe o eixo Z em, digamos, 5 mm, em seguinda jogarmos os eixos X e Y para o centro da mesa, e descermos o bico gradativamente até que este prenda levemente um pedaço de papel, a difereça entre o valor que estiver mostrando no eixo Z e 5mm será o valor do offset do eixo Z. Este valor deverá ser informado no item de menu de ofsset do eixo Z e estará muito próximo do valor final de offset.


### Quando o sensor de auto nivelamento e o sensor de endstop do Eixo são independentes
