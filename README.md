//============================================================================
// Name        : tareanodo.cpp
// Author      : lester ostorga
// Version     :
// Copyright   : Your copyright notice
// Description : Hello World in C++, Ansi-style
//============================================================================

#include <iostream>
#include <stdlib.h>

using namespace std;

struct nodo{
	int info;      // declarando nuestra estructura de datos enteros
	struct nodo *siguientenodo;  // puntero para indicar el siguiente nodo
};
int main (){
	 nodo *tope;   //puntero para saber el tope de los nodos
	 nodo *nuevo;  //puntero para ingresar nuevos nodos
	tope=NULL;
	int d;
	int cant;
	int i=0;
	cout<<"ingrese la cantidad de nodos"<<endl; //definiendo nodos por el usuariao
	cin>>cant;

	while(i<cant){
		nuevo=(struct nodo *)malloc(sizeof(struct nodo));//estableciendo memoria
	nuevo->siguientenodo=tope;
	cout<<"ingrese el valor"<<endl;
	cin>>d;
	nuevo->info=d;//asignando posicion
	tope=nuevo;//
		i++;
	}
while(nuevo!=NULL){  //loop para mostrar la informacion que contiene cada nodo
	cout<<nuevo->info<<",";
	nuevo=nuevo->siguientenodo;
}
return 0;

}
