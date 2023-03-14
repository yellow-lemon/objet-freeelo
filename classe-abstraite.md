Une classe qui ne sera jamais instanciée. \
Par exemple, Astre serait une classe absraite

# Méthode abstraite
C'est le squelette d'une méthode. Elle est **obligé** d'être **override** par ses enfants \
Si l'enfant est abstrait aussi, il **n'a pas à override**. \
La règle : Le **premier enfant concrait** doit l'override
```cs
public abstract class Toto
{
  abstract public int MethodeA();
}
```

```cs
public class Tata : Toto
{
  public override methodA()
  {
    ///...
  }
}
```

# Méthode virtuel
Contient du code, mais peut être overridé
```cs
public abstract class Toto
{
  public virtual int methodB()
  {
    //...
  }
}
```

# Base
le keyword `base` est l'équivalent du `this` pour le parent.

# Sealed
Une classe sealed ne peut pas être héritée.
```cs
  public sealed class CFinale
  {
    //...
  }
```

