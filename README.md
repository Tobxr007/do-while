#include <iostream>
using namespace std;

int main() {
    int opcion;
    float saldo = 1000, dinero;

     do {
        cout << "\n--- CAJERO AUTOMATICO ---" << endl;
        cout << "1. Consultar saldo" << endl;
        cout << "2. Depositar dinero" << endl;
        cout << "3. Retirar dinero" << endl;
        cout << "4. Salir" << endl;
        cout << "Elija una opcion: ";
        cin >> opcion;

        switch (opcion) {
            case 1:
                cout << "Su saldo es: $" << saldo << endl;
                break;

            case 2:
                cout << "Cuanto desea depositar: $";
                cin >> dinero;

                if (dinero > 0) {
                    saldo = saldo + dinero;
                    cout << "Deposito realizado." << endl;
                } else {
                    cout << "Cantidad no valida." << endl;
                }
                break;

            case 3:
                cout << "Cuanto desea retirar: $";
                cin >> dinero;

                if (dinero > 0 & dinero <= saldo) {
                    saldo = saldo - dinero;
                    cout << "Retiro realizado." << endl;
                } else {
                    cout << "Cantidad no valida o saldo insuficiente."
                         << endl;
                }
                break;

            case 4:
                cout << "Gracias por usar el cajero." << endl;
                break;

            default:
                cout << "Opcion incorrecta." << endl;
        }

    } while (opcion != 4);

    return 0;
}
