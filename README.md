# ForYandex
#include <iostream>

using namespace std;

class Figure
{
public:
	virtual void P()
	{
		cout << NULL << endl;
	}
};

class Rectangle : protected Figure
{
private:
	int a;
	int b;
	int c;
	int d;

public:
	void get_Rectangle()
	{
		cout << "Введите сторону a: ";
		cin >> a;
		cout << "Введите сторону b: ";
		cin >> b;
		cout << "Введите сторону c: ";
		cin >> c;
		cout << "Введите сторону d: ";
		cin >> d;
	}
	void P()
	{
		cout << "Периметр прямоугольника = ";
		cout << a + b + c + d << endl;
	}
};

class Circle : protected Figure
{
private:
	int r;
	const double pi = 3.1415;

public:
	void get_Circle()
	{
		cout << "Введите радиус r: ";
		cin >> r;
	}
	void P()
	{
		cout << "Длина окружности (периметр круга) = ";
		cout << 2 * pi*r << endl;
	}
};

class Triangle : protected Figure
{
private:
	int a;
	int b;
	int c;

public:
	void get_Triangle()
	{
		cout << "Введите сторону a: ";
		cin >> a;
		cout << "Введите сторону b: ";
		cin >> b;
		cout << "Введите сторону c: ";
		cin >> c;
	}
	void P()
	{
		cout << "Периметр треугольника = ";
		cout << a + b + c << endl;
	}
};

class Rhomb : protected Figure
{
private:
	int a;

public:
	void get_Rhomb()
	{
		cout << "Введите сторону a: ";
		cin >> a;
	}
	void P()
	{
		cout << "Периметр ромба = ";
		cout << 4 * a << endl;
	}
};

void main()
{
	setlocale(LC_ALL, "Russian");

	cout << "Работа с прямоугольником А" << endl;
	Rectangle A;
	A.get_Rectangle();
	A.P();

	cout << "Работа с кругом Б" << endl;
	Circle B;
	B.get_Circle();
	B.P();

	cout << "Работа с треугольноком В" << endl;
	Triangle C;
	C.get_Triangle();
	C.P();

	cout << "Работа с ромбом Д" << endl;
	Rhomb D;
	D.get_Rhomb();
	D.P();

	system("pause");
}
