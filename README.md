# ![image](https://gist.github.com/assets/158230496/635cb489-12f2-4c17-af33-322550c29cb9)

 ```ASM
; Problema 1:
; Imprimir los números enteros del 9 al 43
; Instituto Técnologico de Tijuana
; Ing en Sistemas Computacionales
; Autor: Nuño Reyes Gerardo @nickname GeraNuno
; Documentador: Almeida Valles josé de jesús @Nickname JoseAlmeida21
; Fecha: 01/03/2024
; Repositorio: 

.begin:	
	clra            ; Limpiar el registro acumulador A
	mov Rb, 9       ; Mover el valor 9 al registro Rb
	mov Rc, 0       ; Mover el valor 0 al registro Rc
	mov Ra, 42      ; Mover el valor 42 al registro Ra
	
.loop:
	
	add Rc, Rb      ; Sumar el contenido de Rb al contenido de Rc y almacenarlo en Rc
	
	mov Rd, Rc      ; Mover el contenido de Rc al registro Rd
	mov Rc, 1       ; Mover el valor 1 al registro Rc
	mov Rb, Rd      ; Mover el contenido de Rd al registro Rb
	
	cmp Ra, Rb      ; Comparar el contenido de Ra con el contenido de Rb
	jo .begin       ; Si el resultado de la comparación indica un desbordamiento, volver al inicio (.begin)
	
	jmp .loop       ; Saltar al marcador .loop para repetir el bucle
  
       address    | data
                |                            ; .begin:
 0   : 00000000 | 00110111          ; clra
 1   : 00000001 | 00001111 00001001 ; mov Rb, 9
 3   : 00000011 | 00010111 00000000 ; mov Rc, 0
 5   : 00000101 | 00000111 00101010 ; mov Ra, 42
                |                            ; .loop:
 7   : 00000111 | 11001110          ; add Rc, Rb
 8   : 00001000 | 00011010          ; mov Rd, Rc
 9   : 00001001 | 00010111 00000001 ; mov Rc, 1
 11  : 00001011 | 00001011          ; mov Rb, Rd
 12  : 00001100 | 11111000          ; cmp Ra, Rb
 13  : 00001101 | 00111010 00000000 ; jo .begin
 15  : 00001111 | 00101111 00000111 ; jmp .loop
   ```
  
   ```C++
  #include <iostream>

/*Problema 1:
Imprimir los numeros enteros del 9 al 43
Autor: López Contreras Jesús Rafael @Nickname Jesusrlc
Documentador: Almeida Valles josé de jesús @Nickname JoseAlmeida21
Fecha: 01/03/2024
Repositorio: 
*/

void Contar()   //Creación del procedimiento
{
      for (int i = 9; i <= 43; ++i)   //Ciclo for, i empieza en 9 y mientras i sea menor que 43 suma 1
      {
     std::cout << i << " \n";    // Imprimir el valor actual de i
      }
}

int main()    //Creacion del main
{    
 
 Contar();  //Llamada del procedimiento
}

 ```
 