#include <iostream>
using namespace std;

void obmen(int a, int b)
{
    int c = a;
    a = -b;
    b = c;
}
void obmen2(int *a, int *b)
{
    int c = *a;
    *a = *b;
    *b = c;
}
void show_mass(int* m, int size_m)
{
    for (int i = 0; i < size_m; i++)
    {
        cout << " | " << m[i];
    }
}
void show_mass2(int* m, int size_m)
{
    cout << "\n";
    for (int i = 0; i < size_m; i++)
    {
        cout << " | " << *m;
        m++;
    }
}
void mas(int* m, int size_m)
{
    if (m == nullptr)    // if (!m)
        return;
    int t = 9;
    for (int i = 0; i < size_m; i++)
    {
        *m = t - i;
        m++;
    }
}

int dlinna(char* p)
{
    char* e = p;
    for (; *e != '\0'; e++);
    return (e - p);
}
int dlinna2(char* p)
{
    int c = 0;
    for (; *p != '\0'; p++)
        c++;
    return c;
}
int dlinna3(char* p)
{
    int c = 0;
    for (int i = 0; p[i] != '\0'; i++)
        c++;
    return c;
}


int main()
{
    char m[] = "hello world";
    cout << m;
    int mi[5]{};
    cout << "\n" << mi;
    cout << "\n" << sizeof(m) / sizeof(m[0]);
    char b[] = { '2','3','4','\0'};
    cout << "\n" << b;
    cout<<"\n"<< dlinna(m);
    cout << "\n" << dlinna2(m);
    cout << "\n" << dlinna(m);
}



