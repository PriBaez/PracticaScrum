# Lectura y escritura en un archivo de texto utilizando C#

## Leer un archivo de texto

El código siguiente usa la clase `StreamReader` para abrir, leer y cerrar el archivo de texto. Puede pasar la ruta de acceso de un archivo de texto al constructor `StreamReader` para abrir el archivo automáticamente. El método `ReadLine` lee cada línea de texto e incrementa el puntero de archivo a la siguiente línea a medida que lee. Cuando el método `ReadLine` llega al final del archivo, devuelve una referencia nula.
1. Cree un archivo de texto de ejemplo en Bloc de notas. Siga estos pasos:
  - Pegue el texto *hello world* en Bloc de notas.
  - Guarde el archivo como *Sample.txt*.
2. Inicie Microsoft Visual Studio.
3. En el menú **Archivo**, seleccione **Nuevo** y luego **Proyecto**.
4. Seleccione **Proyectos en Visual C#** en Tipos de proyecto y luego seleccione **Aplicación de consola** en **Plantillas**.
5. Agregue el código siguiente al principio del archivo *Class1.cs*:
```csharp
using System.IO;
```
6. Agregue el código siguiente al método `Main`:  

```csharp
String line;
try
{
    StreamReader sr = new StreamReader("C:\\Sample.txt");
    line = sr.ReadLine();
    while (line != null)
    {
        Console.WriteLine(line);
        line = sr.ReadLine();
    }
    sr.Close();
    Console.ReadLine();
}
catch(Exception e)
{
    Console.WriteLine("Exception: " + e.Message);
}
finally
{
    Console.WriteLine("Executing finally block.");
}
```
7. En el menú Depurar, seleccione Inicio para compilar y ejecutar la aplicación. Presione Entrar para cerrar la ventana Consola. 
La ventana Consola muestra el contenido del archivo Sample.txt:
> Hello world


## Escribir un archivo de texto

El código siguiente usa la clase StreamWriter para abrir, escribir y cerrar el archivo de texto. De forma similar a la clase StreamReader, puede pasar la ruta de acceso 
de un archivo de texto al constructor StreamWriter para abrir el archivo automáticamente. El método WriteLine escribe una línea de texto en el archivo de texto creado.

1. Inicie Visual Studio.
2. En el menú Archivo, seleccione Nuevo y luego Proyecto.
3. Seleccione Proyectos en Visual C# en Tipos de proyecto y luego seleccione Aplicación de consola en Plantillas.
4. Agregue el código siguiente al principio del archivo Class1.cs:
```csharp
using System.IO;
```
5. Agregue el código siguiente al método Main:  
```csharp
try
{
    StreamWriter sw = new StreamWriter("C:\\Test.txt");
    sw.WriteLine("Hello World!!");
    sw.WriteLine("From the StreamWriter class");
    sw.Close();
}
catch(Exception e)
{
    Console.WriteLine("Exception: " + e.Message);
}
finally
{
    Console.WriteLine("Executing finally block.");
}
```
6. En el menú Depurar, seleccione Inicio para compilar y ejecutar la aplicación. Este código crea un archivo denominado Test.txt la unidad C. Abra Test.txt en un editor de texto, como Bloc de notas. Test.txt contiene dos líneas de texto.
> Hello World!!  
> From the StreamWriter class
