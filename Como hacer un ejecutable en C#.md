# crear un ejecutable en C# y ejecutarlo C#:



Para crear un ejecutable en C# y ejecutarlo, sigue estos pasos:

1. Abre un editor de código o un entorno de desarrollo integrado (IDE) como Visual Studio Code, Visual Studio u otro de tu elección.

2. Crea un nuevo archivo con extensión ".cs" (por ejemplo, "Program.cs").

3. Escribe tu código en el archivo para realizar la funcionalidad deseada. Aquí tienes un ejemplo básico:

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("¡Hola, mundo!");
        Console.ReadKey();
    }
}
```

4. Guarda el archivo con el código.

5. Abre una ventana de terminal o símbolo del sistema y navega hasta la ubicación del archivo ".cs".

6. Compila el archivo utilizando el comando `csc` (el compilador de C#) seguido del nombre del archivo:

```
csc Program.cs
```

Esto generará un archivo ejecutable con el mismo nombre del archivo fuente (en este caso, "Program.exe").

7. Una vez compilado el programa, puedes ejecutarlo utilizando el siguiente comando:

```
Program.exe
```

Esto iniciará la ejecución del programa y mostrará la salida en la consola.

Recuerda que estos pasos asumen que tienes el SDK de .NET instalado en tu sistema. Además, asegúrate de tener configurado el entorno de desarrollo correctamente para poder compilar y ejecutar programas de C#.

Si estás utilizando un IDE como Visual Studio o Visual Studio Code, es posible que el proceso de compilación y ejecución sea más sencillo, ya que estos entornos proporcionan herramientas integradas para compilar y ejecutar proyectos de C#.

Espero que esto te sea útil. ¡Si tienes alguna otra pregunta, no dudes en preguntar!
