
* $Abstracción
* $Herencia
* $Polimorfismo
* $Encapsulación
* $Clase
* $Objeto
* $Instancia
* $Interfaz
* $Modificadores de acceso
* $Constructores
* $Después de eso, tend


* $¿Qué es TypeScript?
En resumen, TypeScript es un superconjunto de JavaScript que tiene escritura opcional y compila en JavaScript simple.

En palabras más simples, TypeScript técnicamente es JavaScript con tipado estático , siempre que quieras tenerlo.


Example
```
class Persona {
  nombre: string;
  edad: number;

  constructor(nombre:string, edad:number) {
    this.nombre = nombre;
    this.edad = edad;
  }

  imprimir() {
    console.log(`Nombre: ${this.nombre} y edad:${this.edad}`);
  }
}

let persona1: Persona;
persona1 = new Persona('Juan', 45);
persona1.imprimir();

```
