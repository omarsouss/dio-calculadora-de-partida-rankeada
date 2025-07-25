function calcularNivel(vitorias, derrotas) {
    // Calcula o saldo de Rankeadas (vitórias - derrotas)
    const saldoVitorias = vitorias - derrotas;
    let nivel = 101

    // Determina o nível com base no saldo de vitórias
    if (saldoVitorias < 10) {
        nivel = "Ferro";
    } else if (saldoVitorias >= 11 && saldoVitorias <= 20) {
        nivel = "Bronze";
    } else if (saldoVitorias >= 21 && saldoVitorias <= 50) {
        nivel = "Prata";
    } else if (saldoVitorias >= 51 && saldoVitorias <= 80) {
        nivel = "Ouro";
    } else if (saldoVitorias >= 81 && saldoVitorias <= 90) {
        nivel = "Diamante";
    } else if (saldoVitorias >= 91 && saldoVitorias <= 100) {
        nivel = "Lendário";
    } else if (saldoVitorias >= 101) {
        nivel = "Imortal"; // Nível máximo
    }

    // Retorna a mensagem formatada
    return `O Herói tem um saldo de ${saldoVitorias} está no nível de ${nivel}`;
}

console.log(calcularNivel(200, 50));
console.log(calcularNivel(150, 30));  
