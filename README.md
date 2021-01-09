# Lab_11
class Triangle
{
    private double a, b, c;
    private string name = "";
 
    public Triangle() { }
    public Triangle(string n) { name = n; }
    public Triangle(double aa, double bb, double cc) { a = aa; b = bb; c = cc; }
 
    public void Print()
    {
        Console.WriteLine($"a = {a}, b = {b}, c = {c}");
    }
 
    public double Perimeter() => a + b + c;
    public double Square()
    {
        double p = Perimeter() / 2;
 
        return Math.Sqrt(p * (p - a) * (p - b) * (p - c));
    }
 
    public double A
    {
        get => a;
        set { if (value > 0) a = value; }
    }
 
    public double B
    {
        get => b;
        set { if (value > 0) b = value; }
    }
 
    public double C
    {
        get => c;
        set { if (value > 0) c = value; }
    }
 
    public string Name
    {
        get => name;
    }
 
    public bool isValid
    {
        get => a + b > c && b + c > a && a + c > b && a > 0 && b > 0 && c > 0;
    }
}
