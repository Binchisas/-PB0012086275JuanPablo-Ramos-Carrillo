# -PB0012086275JuanPablo-Ramos-Carrillo
#include <iostream>
#include <stdio.h>
#include<string.h>

using namespace std;


int main()
{
	int opcion, numc, cdt, total, put, pu,opcion2,repetidor;
	char pac[1000];
	char trt[1000];
	char desc[10000];
	char hrs[20];
	
	do{
		cout << "Bienbenidos al consultorio" << endl;
		cout << "1-Agendar cita" << endl;
		cout << "2-Modificar cita" << endl;
		cout << "3-Eliminar cita" << endl;
		cout << "4-Lista de citas vigentes" << endl;
		cout << "5-Limpiar pantalla" << endl;
		cout << "6-Salir" << endl;
		cin >> opcion;
		
		
			switch (opcion)
			{
			case 1:
				cout << "Numero de cita" << endl;
				cin >> numc;
				cout << "Nombre del paciente" << endl;
				cin.ignore();
				cin.getline(pac, 1000, '\n');
				cout << "Hora del tratamiento (en 24 hrs)" << endl;
				cin >> hrs;			
				cout << "Nombre del tratamiento" << endl;
				cin.ignore();
				cin.getline(trt, 1000, '\n');
				cout << "Descripcion" << endl;
				cin.ignore();
				cin.getline(desc, 10000, '\n');
				cout << "Cantidad del tratamiento" << endl;
				cin >> cdt;
				cout << "Precio Unitario" << endl;
				cin >> pu;
				total = pu * cdt;
				cout << "Total: $" << total << endl;
				cout << "Regresar al menu" << endl;
				cout << "1-si" << endl;
				cout << "2-no" << endl;
				cin >> repetidor;

				break;
			case 2:
				cout << "Numero de cita" << endl;
				cin >> numc;
				cout << "Ingrese el numero correspondiente al dato que desea modificar" << endl;
				cout << "1.Nombre del paciente" << endl;
				cout << "2.Hora del tratamiento" << endl;
				cout << "3.Nombre del tratamiento" << endl;
				cout << "4.Cantidad del tratamient" << endl;
				cout << "5.Precio Unitario" << endl;
				cin >> opcion2;


				switch (opcion2)
				{
				case 1:
					cout << "ingrese nuevo nombre" << endl;
					cin.ignore();
					cin.getline(pac, 1000, '\n');
					break;
				case 2:
					cout << "ingrese nueva hora" << endl;
					cin >> hrs;
					break;
				case 3:
					cout << "Ingres nuevo nombre del tratamiento" << endl;
					cin.ignore();
					cin.getline(trt, 1000, '\n');
					break;
				case 4:
					cout << "Ingrese nueva cantidad de tratamiento" << endl;
					cin >> cdt;
					break;
				case 5:
					cout << "ingrese nuevo precio Unitario" << endl;
					cin >> pu;
					break;
				default:
					cout << "Ingrese dato valido" << endl;
				}
				cout << "Regresar al menu" << endl;
				cout << "1-si" << endl;
				cout << "2-no" << endl;
				cin >> repetidor;

				break;
			case 3:
	                        cout<< "Ingrese el numero de cita a eliminar" << endl;
	                        cin>> numc;
				cout << "Regresar al menu" << endl;
				cout << "1-si" << endl;
				cout << "2-no" << endl;
				cin >> repetidor;

				break;
			case 4:
				cout << "Regresar al menu" << endl;
				cout << "1-si" << endl;
				cout << "2-no" << endl;
				cin >> repetidor;

				break;
			case 5:
				system("cls");
				cout << "Pntalla limpia" << endl;
				cout << "Regresar al menu" << endl;
				cout << "1-si" << endl;
				cout << "2-no" << endl;
				cin >> repetidor;

				break;
			case 6:
				cout << "Le agradecomos su preferencia" << endl;
	                        repetidor = 2;
				break;
			default:
				cout << "Ingrese una ocpion valida" << endl;
				cout << "Escoja una opcion" << endl;
				cout << "1-Agendar cita" << endl;
				cout << "2-Modificar cita" << endl;
				cout << "3-Eliminar cita" << endl;
				cout << "4-Lista de citas vigentes" << endl;
				cout << "5-Limpiar pantalla" << endl;
				cout << "6-Salir" << endl;
				cin >> opcion;

			}
			
		
	}while (repetidor == 1);
	
}
