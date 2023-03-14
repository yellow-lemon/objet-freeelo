# Accesseurs

## Variable
A ne pas faire :
```cs
unePersonne.m_age = 12;
int x = unePersonne.m_age;
```

## Propriétés
Les propriétés sont la bonne façon d'accéder aux variables.
```cs
public int Age
{
  get { return m_age; }

  set 
  {
    m_age = value;
  }
}
```
utilisé ainsi :
```cs
unePersonne.Age = 10;
int x = unePersonne.Age;
```