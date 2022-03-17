#include <iostream>
#include <stdio.h>
#include<string.h>

using namespace std;

struct consultorio {
	char paciente[100];
	char hrs[100];
	char nomtratamiento[100];
	float precio;
	int numero;
};


int main()
{
	int opcion, numc, cdt, total, put, pu,opcion2,repetidor, repetidor2,i,j;
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
		consultorio citas[3];
		
			switch (opcion)
			{
			case 1:
				
					for (i = 0; i < 3; i++)
					{
						cout << "Numero de cita" << endl;
						citas[i].numero = i + 1;
						cout << citas[i].numero << endl;
						cout << "Nombre del paciente" << endl;
						cin>>citas[i].paciente;
						cout << "Hora del tratamiento (en 24 hrs)" << endl;
						cin >> citas[i].hrs;
						cout << "Nombre del tratamiento" << endl;
						cin >> citas[i].nomtratamiento;
						cout << "Descripcion" << endl;
						cin.ignore();
						cin.getline(desc, 10000, '\n');
						cout << "Cantidad del tratamiento" << endl;
						cin >> cdt;
						cout << "Precio Unitario" << endl;
						cin >> citas[i].precio;
						total = citas[i].precio * cdt;
						cout << "Total: $" << total << endl;
						
					}

				
					cout << "Regresar al menu" << endl;
					cout << "1-si" << endl;
					cout << "2-no" << endl;
					cin >> repetidor;
				

				break;
			case 2:
				cout << "Ingrese el numero de cita para modificar" << endl;
				cin >> j;
				i = j - 1;
				for (i; i <j; i++)
				{
					cout << "Numero de cita" << endl;
					citas[i].numero = i + 1;
					cout << citas[i].numero << endl;
					cout << "Nombre del paciente" << endl;
					cin >> citas[i].paciente;
					cout << "Hora del tratamiento (en 24 hrs)" << endl;
					cin >> citas[i].hrs;
					cout << "Nombre del tratamiento" << endl;
					cin >> citas[i].nomtratamiento;
				}
				break;
			case 3:
				cout << "Ingrese la cita a eliminar" << endl;
				cin >> numc;
				cout << "Regresar al menu" << endl;
				cout << "1-si" << endl;
				cout << "2-no" << endl;
				cin >> repetidor;

				break;
			case 4:

				for (i = 0; i < 3; i++)
				{
					cout <<"El numero de cita  "<< citas[i].numero << endl;
					cout <<"Paciente: "<< citas[i].paciente << endl;
					cout << "Hora de cita: " << citas[i].hrs << endl;
					cout << "Tratamiento: "<< citas[i].nomtratamiento << endl;

				}
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
				repetidor = 1;
			

			}
			
		
	}while (repetidor == 1);
	
}
