# Uebung-031  --  Star Square
<!--
## Lernziele:

## Aufgabenstellung:

### Beispiel:
### Beispielausgabe:

#### Hinweis:

-------------------------------
## *Zusatzaufgabe:*



-->
-------------------------------
# **SPOILER**

```c#
using System;
using System.Threading;
using System.Reflection.Metadata;

namespace StarSquare
{
  internal class Program
  {
    static void Main()
    {
      const int consoleWidth = 80;
      const int consoleHeight = 30;
      Console.SetWindowSize(consoleWidth, consoleHeight);

      string userInput;
      int userInteger;

      Console.Write("\n                 Starsquare                 " +
                    "\n============================================" +
                    "\n Welche Seitenlänge soll das Quadrat haben? " +
                    "\n ");
      userInput = Console.ReadLine();
      int.TryParse(userInput, out userInteger);

      for (int i = 0; i < userInteger; i++)
      {
        for (int j = 0; j < userInteger; j++)
        {
          Console.Write("*");
        }
        Console.Write("\n");
      }
      Thread.Sleep(1000);
      Console.Clear();

      /// put output into center:
      for (int i = 0; i < (consoleHeight - userInteger) / 2; i++)
      {
        Console.Write("\n");
      }
      for (int j = 0; j < userInteger; j++)
      {
        for (int k = 0; k < (consoleWidth - userInteger) / 2; k++)
        {
          Console.Write(" ");
        }
        for (int l = 0; l < userInteger; l++)
        {
          Console.Write("*");
        }
        Console.Write("\n");
      }
      
      /// wait for a key to remove the square
      Console.ReadLine();
      Console.Clear();

      Console.Write("\nZum Beenden bitte Eingabetaste drücken ...");
      Console.ReadLine();
      Console.Clear();

    }
  }
}

```
