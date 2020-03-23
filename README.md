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
````csharp
string hex = BitConverter.ToString(data);

textBox1.Text = hex;
````

# Consola 
### Centrar Texto 
````Csharp
// Horizontal
int x = 45;
// Vertical
int y = 10;

Console.SetCursorPosition(posX, posY);

Console.WriteLine("Este Texto se Centrará");
````

##
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