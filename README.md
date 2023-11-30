# TarefaNatal
cpp Tabuada

#include "cTab.h"

cTab::cTab() {
}

cTab::cTab(const cTab& orig) {
}

cTab::~cTab() {
}

#include <iostream>

using namespace std;

int cTab::tabuadaRecursiva(int numero, int multiplicador = 1, int acumulado = 0) {
    if (multiplicador > 10) {
        return acumulado;
    }

    int resultado = numero * multiplicador;
    acumulado += resultado;

    cout << numero << " x " << multiplicador << " = " << resultado << endl;

    
    return tabuadaRecursiva(numero, multiplicador + 1, acumulado);
}

void cTab::coletarDados(){
    int valor;

    cout << "Digite um valor para calcular a tabuada: ";
    cin >> valor;

    int resultadoAcumulado = tabuadaRecursiva(valor);

    cout << "Resultado acumulado: " << resultadoAcumulado << endl;

}

.h tabuada


#ifndef CTAB_H
#define CTAB_H

class cTab {
public:
    cTab();
    cTab(const cTab& orig);
    virtual ~cTab();
    void coletarDados();
    int tabuadaRecursiva(int numero, int multiplicador, int acumulado); 
private:

};

#endif /* CTAB_H */











cpp fibonacci

#include "cFibonacci.h"

cFibonacci::cFibonacci() {
}

cFibonacci::cFibonacci(const cFibonacci& orig) {
}

cFibonacci::~cFibonacci() {
}

#include <iostream>

using namespace std;

int cFibonacci:: fibonacci(int n) {
    if (n <= 1) {
        return n;
    }

    return fibonacci(n - 1) + fibonacci(n - 2);
}

void cFibonacci:: coletarDados() {
    int termo;

    cout << "Digite o termo desejado da série de Fibonacci: ";
    cin >> termo;

    if (termo < 0) {
        cout << "Digite um número não negativo para o termo.\n";
    } else {
        int resultado = fibonacci(termo);
        cout << "O " << termo << "º termo da série de Fibonacci é: " << resultado << endl;
    }
}


.h fibonacci

#ifndef CFIBONACCI_H
#define CFIBONACCI_H

class cFibonacci {
public:
    cFibonacci();
    cFibonacci(const cFibonacci& orig);
    virtual ~cFibonacci();
    void coletarDados();
    int fibonacci(int n);
private:

};

#endif /* CFIBONACCI_H */







cpp fatorial


#include "cRecu.h"
#include<iostream>
using namespace std;
cRecu::cRecu() {
}

cRecu::cRecu(const cRecu& orig) {
}

cRecu::~cRecu() {
}

void cRecu::coletarDados(){
    int num;
    float f;
    cout<<"Informe o numero do fatorial: ";
    cin>>num;
    
    f = Fatorial(num);
    cout<<"Fatorial: "<<f;
    
}

float cRecu::Fatorial(int num){
    float vfat;
    
    if(num<=1){
        return (1);
    }else{
        vfat = num * Fatorial(num - 1);
        return (vfat);
    }
}

.h fatorial

#ifndef CRECU_H
#define CRECU_H

class cRecu {
public:
    cRecu();
    cRecu(const cRecu& orig);
    virtual ~cRecu();
    void coletarDados();
    float Fatorial(int num);
private:

};

#endif /* CRECU_H */
















