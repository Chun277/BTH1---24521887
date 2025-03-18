#include <iostream>
using namespace std;
struct PHANSO {
    int ts, ms;
};
int TimUSCLN(int a, int b) { // ham tim uoc so chung lon nhat
    a = a < 0 ? -a : a;
    b = b < 0 ? -b : b;
    if (a == 0 || b == 0)
        return a + b;
    while (a != b) {
        if (a > b)
            a -= b;
        else
            b -= a;
    }
    return b;
}
void RutGon(PHANSO &ps) { // ham rut gon phan so bang cach chia ca tu va mau cho uoc so chung lon nhat cua tu va mau
    int USCLN = TimUSCLN(ps.ts, ps.ms);
    if (USCLN > 0) {
        ps.ts /= USCLN;
        ps.ms /= USCLN;
    }
    if (ps.ms < 0) {
        ps.ts = -ps.ts;
        ps.ms = -ps.ms;
    }
}
void NhapPhanSo(PHANSO &ps) // ham nhap phan so
{
    cout << "Nhap tu so: ";
    cin >> ps.ts;
    do {
        cout << "Nhap mau so: ";
        cin >> ps.ms;
    } while (ps.ms == 0);
}
void XuatPhanSo(PHANSO ps) // ham xuat phan so
{
    RutGon(ps);
    if (ps.ms < 0)
    {
        cout << -ps.ts << "/" << -ps.ms;
    }
    else if (ps.ms == -1)
    {
        cout << -ps.ts;
    }
    else if (ps.ms == 0)
    {
        cout << "Khong Xac Dinh";
    }
    else if (ps.ms == 1)
    {
        cout << ps.ts;
    }
    else
    {
        cout << ps.ts << "/" << ps.ms;
    }
}
int main()
{
    PHANSO ps;
    NhapPhanSo(ps);
    RutGon(ps);
    XuatPhanSo(ps);
    return 0;
}
