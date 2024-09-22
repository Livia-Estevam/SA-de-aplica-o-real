#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    float valorHora, horasTrabalhadas, salarioBruto, irDesconto, inssDesconto, fgts, salarioLiquido, totalDescontos;

    cout << "Digite o valor da hora: ";
    cin >> valorHora;
    cout << "Digite a quantidade de horas trabalhadas no mes: ";
    cin >> horasTrabalhadas;

    salarioBruto = valorHora * horasTrabalhadas;

    if (salarioBruto <= 900) {
        irDesconto = 0;
    } else if (salarioBruto <= 1500) {
        irDesconto = salarioBruto * 0.05;
    } else if (salarioBruto <= 2500) {
        irDesconto = salarioBruto * 0.10;
    } else {
        irDesconto = salarioBruto * 0.20;
    }

    inssDesconto = salarioBruto * 0.10;
    fgts = salarioBruto * 0.11;
    totalDescontos = irDesconto + inssDesconto;
    salarioLiquido = salarioBruto - totalDescontos;

    cout << fixed << setprecision(2);
    cout << "Salário Bruto: ( " << valorHora << " * " << horasTrabalhadas << " ) : R$ " << salarioBruto << endl;
    cout << "(-) IR (" << (irDesconto / salarioBruto * 100) << "%) : R$ " << irDesconto << endl;
    cout << "(-) INSS (10%) : R$ " << inssDesconto << endl;
    cout << "FGTS (11%) : R$ " << fgts << endl;
    cout << "Total de descontos : R$ " << totalDescontos << endl;
    cout << "Salário Líquido : R$ " << salarioLiquido << endl;

    return 0;
}
