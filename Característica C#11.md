# Característica nueva de C# 11

Dentro de las novedades que trae C# 11 se puede destacar:

## Compatibilidad matemática genérica

Hay varias características de lenguaje que habilitan la compatibilidad matemática genérica:

* `static virtual` miembros en interfaces
* Operador definido por el usuario checked
* operadores de desplazamiento relajado
* Operador de desplazamiento a la derecha sin signo

Puede agregar `static abstract` o `static virtual` miembros en interfaces para definir interfaces que incluyan operadores sobrecargables, otros miembros estáticos y propiedades estáticas. El escenario principal de esta característica es usar operadores matemáticos en tipos genéricos. Por ejemplo, puede implementar la interfaz de `System.IAdditionOperators<TSelf, TOther, TResult>` en un tipo que implementa `operator +`. 

Otras interfaces definen otras operaciones matemáticas o valores bien definidos. Puede obtener información sobre la nueva sintaxis en el artículo sobre interfaces. Las interfaces que incluyen métodos de `static virtual` suelen ser interfaces genéricas. Además, la mayoría declarará una restricción que el parámetro de tipo implementa en la interfaz declarada.

Las matemáticas genéricas han creado otros requisitos en el lenguaje.

* Operador de desplazamiento a la derecha sin signo: antes de C# 11, para forzar un desplazamiento a la derecha sin signo, había que convertir cualquier tipo entero con signo en un tipo sin signo, llevar a cabo el desplazamiento y, después, convertir el resultado en un tipo con signo. A partir de C# 11, puede usar `>>>`, el operador de desplazamiento sin signo.
* Requisitos de operador de desplazamiento menos estrictos: C# 11 elimina el requisito de que el segundo operando debe ser un `int` o convertible implícitamente en `int`. Este cambio permite que los tipos que implementan interfaces matemáticas genéricas se usen en estas ubicaciones.
* Operadores definidos por el usuario checked y unchecked: los desarrolladores ya pueden definir los operadores aritméticos `checked` y `unchecked`. El compilador genera llamadas a la variante correcta en función del contexto actual.
