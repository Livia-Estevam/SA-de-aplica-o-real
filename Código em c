#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    double valorHora, horasTrabalhadas;
    
    cout << "Digite o valor da sua hora: ";
    cin >> valorHora;
    cout << "Digite a quantidade de horas trabalhadas no mês: ";
    cin >> horasTrabalhadas;

    double salarioBruto = valorHora * horasTrabalhadas;
    
    double descontoIR = 0;
    if (salarioBruto > 2500) {
        descontoIR = salarioBruto * 0.20;
    } else if (salarioBruto > 1500) {
        descontoIR = salarioBruto * 0.10;
    } else if (salarioBruto > 900) {
        descontoIR = salarioBruto * 0.05;
    }
    
    double descontoINSS = salarioBruto * 0.10;
    double fgts = salarioBruto * 0.11;
    double totalDescontos = descontoIR + descontoINSS;
    double salarioLiquido = salarioBruto - totalDescontos;

    cout << fixed << setprecision(2);
    cout << "Salário Bruto: (" << valorHora << " * " << horasTrabalhadas << ") : R$ " << salarioBruto << endl;
    cout << "(-) IR (" << (descontoIR / salarioBruto) * 100 << "%) : R$ " << descontoIR << endl;
    cout << "(-) INSS (10%) : R$ " << descontoINSS << endl;
    cout << "FGTS (11%) : R$ " << fgts << endl;
    cout << "Total de descontos : R$ " << totalDescontos << endl;
    cout << "Salário Líquido : R$ " << salarioLiquido << endl;

    return 0;
}
