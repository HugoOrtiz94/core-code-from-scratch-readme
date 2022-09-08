
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


####Example
Clases
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

objetos

El siguiente ejemplo demuestra cómo podemos crear el mismo objeto utilizando estas dos técnicas.
```
let planet = new Object();
let planet = {};
```
Un objeto puede tener propiedades definidas dentro de ellos. En el ejemplo que se presenta a continuación, hemos creado un Planeta de objetos con cuatro propiedades, nombre, galaxia, numberOfMoons y peso.
```
interface Planet{
	name: string;
	galaxy: string;
	numberOfMoons: number;
	weight: number;
}

//Object with properties
let planet: Planet = {
    name : "Earth",
    galaxy : "Milky Way",
    numberOfMoons : 1,
    weight : 100000
};

console.log("Planet Name :- " + planet.name);
console.log("Planet Galaxy :- " + planet.galaxy);
console.log("Planet Number of Moons :- " + planet.numberOfMoons);
console.log("Planet Weight :- " + planet.weight);
```

Un ejemplo la sintaxis que plantea TypeScript para implementar la herencia:

```
class Persona {
  protected nombre:string;
  protected edad:number;
  constructor(nombre:string, edad:number) {
    this.nombre = nombre;
    this.edad = edad;
  }

  imprimir() {
    console.log(`Nombre: ${this.nombre}`);
    console.log(`Edad: ${this.edad}`);
  }    
}

class Empleado extends Persona {
  private sueldo:number;
  constructor(nombre:string, edad:number, sueldo:number) {
    super(nombre, edad);
    this.sueldo = sueldo;
  }

  imprimir() {
    super.imprimir();
    console.log(`Sueldo: ${this.sueldo}`);      
  }

  pagaImpuestos() {
    if (this.sueldo>5000)
      console.log(`${this.nombre} debe pagar impuestos`);
    else
      console.log(`${this.nombre} no debe pagar impuestos`);
  }
}


const persona1=new Persona('Juan', 44);
persona1.imprimir();

const empleado1=new Empleado('Ana', 22, 7000);
empleado1.imprimir();
empleado1.pagaImpuestos();
```

Modificadores de accesos 
Existen cuatro tipos de modificadores dependiendo de qué tan visible querés que sea un atributo, estos modificadores son: public, private, protected y readonly

EJEMPLOS

```
class TodosSabenMisSecretos {
    secreto1='este atributo es público';
    public secreto2='este otro método también es público'
}

/* el mundo exterior */
let clasePublica = new TodosSabenMisSecretos();
console.log(clasePublica.secreto1); //OKA lectura
console.log(clasePublica.secreto2); //OKA lectura
clasePublica.secreto1 = ‘nuevo secreto’; //OKA escritura
clasePublica.secreto2 = ‘otro nuevo secreto; //OKA escritura
```

```
class SoloYoSeMisSecretos {
    private secretoSoloLectura='Mi secreto';
}

/* el mundo exterior */
let objetoConSecretos = new SoloYoSeMisSecretos();
console.log(objetoConSecretos.secretoSoloLectura); //ERROR LECTURA
objetoConSecretos.secretoSoloLectura = 'otro secreto' //ERROR ESCRITURA
```

```
class ClasePadre {
    protected atributoProtected:string;
}

class ClaseHija extends ClasePadre {
    constructor() {
    super();
       this.atributoProtected='Este es un secreto entre ClasePadre'
    }
}

let hija = new ClaseHija();
console.log('cuál es el secreto?', hija.atributoProtected) //esto nos tira un error
```

```
class SóloYoModificoMisSecretos {
    readonly secretoSoloLectura='este atributo es privado';
}

/* el mundo exterior */
let objetoSoloLectura = new SóloYoModificoMisSecretos();
console.log(objetoSoloLectura.secretoSoloLectura); //OK
objetoSoloLectura.secretoSoloLectura = 'otro secreto' //ERROR

```


```
class Persona {
    constructor(nuevoNombre:string, nuevoApellido:string) {
    }
}

class Persona {
    constructor(
       public nombre:string,
       readonly apellido:string,
       private direccion:string
    ) {    }
}
```

```
import Input from './Input';

export default class Main {
  singleInput = async (): Promise<void> => {
    // Get a single input prompt
    let input = await Input.getInput('Where are you from?');
    console.log(input);
  };

  formInput = async (): Promise<void> => {
    // Get a form prompt
    const formChoices = [
      { name: 'age', message: 'What is your age' },
      { name: 'lastName', message: 'What is your last name' },
      { name: 'movie', message: 'What is your favorite movie' },
    ];
    let input = await Input.getForm('Personal Information', formChoices);
    console.log(input);
  };

  selectInput = async (): Promise<void> => {
    // Get a select prompt
    const selectChoices = [
      { option: 1, message: 'Pizza' },
      { option: 2, message: 'Sandwich' },
      { option: 3, message: 'Cofee' },
      { option: 4, message: 'Lasagna' },
    ];
    let input = await Input.getSelect('Menu', selectChoices);
    console.log(input);
  };

  selectByIdInput = async (): Promise<void> => {
    // Get a select by id prompt
    const selectByIdChoices = [
      { name: '#64b5f6', message: 'Blue Lighten 2' },
      { name: '#009688', message: 'Purple Lighten 1' },
      { name: '#ec407a', message: 'Pink Lighten 1' },
      { name: '#f44336', message: 'Red' },
    ];
    let input = await Input.getSelectById('Select a color', selectByIdChoices);
    console.log(input);
  };

  confirmInput = async (): Promise<void> => {
    // Get a confirmation prompt
    let input = await Input.getConfirm('Are you a developer');
    console.log(input);
  };

  async start() {
    /**
     * ========================
     * Play with this class
     * ========================
     * You can remove the comments one by one and see how it behaves
     * Check how the functions work
     * Have fun!! :D
     */
    await this.singleInput();
    await this.formInput();
    await this.selectInput();
    await this.selectByIdInput();
    await this.confirmInput();
  }
}
```
