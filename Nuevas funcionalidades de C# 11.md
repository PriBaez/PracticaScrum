# Nueva funcionalidades de C#:

El modificador abstract y El modificador virtual


Aquí tienes ejemplos de cómo utilizar cada uno de estos modificadores por separado:

```csharp
public class MiClase
{
    // Ejemplo de miembro estático
    public static void MetodoEstatico()
    {
        // Código del método estático
    }

    // Ejemplo de método virtual
    public virtual void MetodoVirtual()
    {
        // Código del método virtual
    }
}

public class ClaseDerivada : MiClase
{
    public override void MetodoVirtual()
    {
        // Código del método virtual reemplazado
    }
}
```


Aquí tienes un ejemplo de cómo utilizar cada modificador por separado:

```csharp
public abstract class MiClaseAbstracta
{
    // Ejemplo de método abstracto
    public abstract void MetodoAbstracto();

    // Ejemplo de campo estático
    public static int CampoEstatico;
}
```

En el ejemplo anterior, MiClaseAbstracta es una clase abstracta que contiene un método abstracto MetodoAbstracto, que no tiene implementación en la clase base y debe ser implementado en una clase derivada. Además, la clase abstracta también puede contener miembros estáticos como el campo CampoEstatico.
