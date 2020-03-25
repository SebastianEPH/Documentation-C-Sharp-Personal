# Documentación Personal de C# 
**Ultima Modificación:**  `22/03/20`

En este documento solo encontrará ciertas caracteristicas de C#, las cuales no son comunes en encontrar, u ciertos pequeños pedazos de código que eh podido realizar en el transcurso de mi proceso de aprendizaje


# Tipo de Datos
## Inicializar Array 
### Tipo de datos - Bytes
````csharp
byte[] data = new byte[] {0x43, 0x00, 0x61,.....}
````

````csharp
byte[] data;

data = "43,00,61,00,6e,00,6f,00,6e,00,20,00,4d,00,50,00,37,00,38,00,30,00,20,00,53,00,65,00,72,00,69,00";
```` 
## Conversión de tipo de Datos

### Convertir a HEX
````Csharp
byte[] data = new byte[] {0x43, 0x00, 0x61,.....}

string hex = BitConverter.ToString(data);

textBox1.Text = hex;
````
# Métodos
## Split - String
### Saltos de Linea con una palabra
````CSharp
string phrase = "The quick brown fox jumps over the lazy dog.";
string[] words = phrase.Split(' ');

foreach (var word in words)
{
    System.Console.WriteLine($"<{word}>");
}
````
Resultado: 
````
Salida Consola:

<The>
<quick>
<brown>
<fox>
<jumps>
<over>
<the>
<lazy>
<dog.>
````
### Salto de lineas con Palabras expecifica
````CSharp
char[] delimiterChars = { ' ', ',', '.', ':', '\t' };

string text = "one\ttwo three:four,five six seven";
System.Console.WriteLine($"Original text: '{text}'");

string[] words = text.Split(delimiterChars);
System.Console.WriteLine($"{words.Length} words in text:");

foreach (var word in words)
{
    System.Console.WriteLine($"<{word}>");
}
````
Salida:
````
Original text: 'one	two three:four,five six seven'
7 words in text:
<one>
<two>
<three>
<four>
<five>
<six>
<seven>
````
### Convertir un String a String []
````CSharp

Console.Write("Ingrese los datos separandolos con una , : ");

String valueData = Console.ReadLine();  // Obtiene datos del consola
string [] salida;
salida = valueData.Split(',');   // Separa las palabras por , obtenidas del la consola
````
### Array Mostrar en consola - Byte
Con List:
````CSharp
var fibNumbers = new List<int> { 0, 1, 1, 2, 3, 5, 8, 13 };
int count = 0;
foreach (int element in fibNumbers)
{
    count++;
    Console.WriteLine($"Element #{count}: {element}");
}
Console.WriteLine($"Number of elements: {count}");
````
Con Array:
````CSharp
int[] fibNumber = new int { 0, 1, 1, 2, 3, 5, 8, 13 };
int count = 0;
foreach (int element in fibNumbers)
{
    count++;
    Console.WriteLine($"Element #{count}: {element}");
}
Console.WriteLine($"Number of elements: {count}");
````
### Promedio de números de un Array
````csharp
//Contador
int sumar = 0;
//Arrray de números
int [] array = { 9, 9, 9, 9, 9, 9, 9, 9 };
//sumando todos los valores del array en la variable sumar
for (int i = 0; i < array.Length; i++) {
    sumar = sumar + array [i];
}
// Sacando promedio
double promedio = sumar / array.Length;
Console.WriteLine("El promedio de los Numeros es: "+promedio);
Console.ReadKey();     
```` 
# Consola 
### Centrar Texto 
````Csharp
// Horizontal
int x = 45;
// Vertical
int y = 10;

Console.SetCursorPosition(X, Y);    // El texto siguiente , se centrará

Console.WriteLine("Este Texto se Centrará");
````
*Salida:*
![Windows Registry Tools v3.1 - Consola Version](https://i.imgur.com/po52Gi8.png)
## Realizar un Animación de espera en Consola 
````Csharp
int X = 40, Y = 10;

string simbolos = "^>v<";
byte simboloActual = 0;
bool terminado = false;

do {
    Console.Clear();
    Console.SetCursorPosition(posX, posY);  // Centra 
    Console.Write(simbolos [simboloActual]);
    Thread.Sleep(500);
    if (Console.KeyAvailable) {
        ConsoleKeyInfo tecla = Console.ReadKey(true);
        if (tecla.Key == ConsoleKey.RightArrow) X++;
        if (tecla.Key == ConsoleKey.LeftArrow) X--;
        if (tecla.Key == ConsoleKey.Escape) terminado = true;
    }
    simboloActual++;
    if (simboloActual > 3) simboloActual = 0;
}
while (!terminado);
````
##
##
##
##
##
##
# By Developer
**SebastianEPH**
- [Github](https://github.com/SebastianEPH)
- [Facebook](https://www.facebook.com/SebastianEPH)
- [Linkedin](https://www.linkedin.com/in/sebastianeph/)
---