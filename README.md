# jlet numeroSecreto = Math.floor(Math.random() * 100) + 1; // Número aleatório de 1 a 100
let tentativas = 0;
let maxTentativas = 3; // Exemplo com 3 tentativas
let palpite;

while (tentativas < maxTentativas) {
    palpite = parseInt(prompt("Digite seu palpite (entre 1 e 100):"));

    // Validação do palpite
    if (isNaN(palpite) || palpite < 1 || palpite > 100) {
        console.log("Por favor, insira um número válido entre 1 e 100.");
        continue; // Volta ao início do laço
    }

    tentativas++;

    if (palpite === numeroSecreto) {
        console.log(`Parabéns! Você acertou o número ${numeroSecreto} em ${tentativas} tentativa(s).`);
        break; // Sai do laço, pois acertou!
    } else if (palpite < numeroSecreto) {
        console.log("Muito baixo! Tente novamente.");
    } else {
        console.log("Muito alto! Tente novamente.");
    }
    
    console.log(`Você ainda tem ${maxTentativas - tentativas} tentativa(s).`);
}

if (palpite !== numeroSecreto) {
    console.log(`Fim do jogo! O número certo era ${numeroSecreto}.`);ogo
