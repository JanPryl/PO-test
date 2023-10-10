# PO-test
namespace PO
{
class bombaclat
{
static void Main(string[] args)
{
//zad1();
//zad2();
//zad3();
//zad4();
//zad5();
zad6();
}
static void zad1()
{
Console.Write("Podaj promień kola: ");
double r = Convert.ToDouble(Console.ReadLine());
if (r > 0)
{
double pole_kola = (r * r * 3.14);
Console.WriteLine("Pole kola wynosi: " + pole_kola);
}
else
{
Console.WriteLine("Niepoprawne Dane!");
}
}
static void zad2()
{
Console.Write("Podaj bok prostokata: ");
double a = Convert.ToDouble(Console.ReadLine());
if (a <= 0)
{
Console.WriteLine("Niepoprawne Dane!");
}
Console.Write("Podaj drugi bok prostokata: ");
double b = Convert.ToDouble(Console.ReadLine());
if (a <= 0)
{
Console.WriteLine("Niepoprawne Dane!");
}
double pole_prostokata = a * b;
if(a==b)
{
Console.WriteLine("To kwadrat o polu " + pole_prostokata);
}
else
{
Console.WriteLine("To prostokat o polu " + pole_prostokata);
}
}
static void zad3()
{
Console.Write("Podaj liczbe calkowita: ");
int a = Convert.ToInt32(Console.ReadLine());
if(a % 2 == 0)
{
Console.WriteLine(a + " jest liczba parzysta");
}
else if(a % 2 == 1)
{
Console.WriteLine(a + " jest liczba nieparzysta");
}
else
{
Console.WriteLine("Niepoprawne Dane!");
}
}
static void zad4()
{
int max;
Console.Write("Podaj pierwsza liczbe: ");
int a = Convert.ToInt32(Console.ReadLine());
Console.Write("Podaj druga liczbe: ");
int b = Convert.ToInt32(Console.ReadLine());
Console.Write("Podaj trzecia liczbe: ");
int c = Convert.ToInt32(Console.ReadLine());
if(a>b)
{
if(a>c)
{
max = a;
}
else
{
max = c;
}
}
else
{
if (b > c)
{
max = b;
}
else
{
max = c;
}
}
Console.WriteLine("najwieksza liczba to " + max);

}
00:26

static void zad5()
{
double x1, x2;
Console.WriteLine("Mamy rownanie kwadratowe postaci: ax^2 + bx + c");
Console.Write("Podaj a: ");
double a = Convert.ToDouble(Console.ReadLine());
Console.Write("Podaj b: ");
double b = Convert.ToDouble(Console.ReadLine());
Console.Write("Podaj c: ");
double c = Convert.ToDouble(Console.ReadLine());
double delta = (b * b) - 4 * a * c;
double pierw_delta;
if(delta>0)
{
pierw_delta = Math.Sqrt(delta);
x1 = (-b - pierw_delta) / (2 * a);
x2 = (-b + pierw_delta) / (2 * a);
Console.WriteLine("x1 = " + x1 + ", x2 = " + x2);
}
else if(delta==0)
{
pierw_delta = Math.Sqrt(delta);
x1 = -b / (2 * a);
Console.WriteLine("x0 = " + x1);
}
else
{
pierw_delta = Math.Sqrt(delta*(-1));
Console.WriteLine("x2 = " + (-b / (2 * a)) + " - " + pierw_delta / (2 * a) + "i");
Console.WriteLine("x2 = " + (-b / (2 * a)) + " + " + pierw_delta / (2 * a) + "i");
}
}
static void zad6()
{

Console.Write("Podaj liczbe zl: ");
double b;
double a = Convert.ToDouble(Console.ReadLine());
Console.Write("Podaj numer waluty na jaka chcesz przeliczyc swoje zl: \nEUR <- 1\nUSD <- 2\nGBP <- 3\n");
int waluta = Convert.ToInt32(Console.ReadLine());
switch (waluta)
{
case 1:
b = a / 4.57;
Console.WriteLine("Kurs -> 4.57zl\nMasz {0:f2} EUR", b);
break;
case 2:
b = a / 4.34;
Console.WriteLine("Kurs -> 4.34zl\nMasz {0:f2} USD", b);
break;
case 3:
b = a / 5.28;
Console.WriteLine("Kurs -> 5.28zl\nMasz {0:f2} GBP", b);
break;
default:
Console.WriteLine("N/A");
break;
}
}
}
}
