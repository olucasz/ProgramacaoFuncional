# ProgramacaoFuncional
Implementação: Aplicações da Programação Funcional - Atividade Della

O problema escolhido para o exemplo é um array de números inteiros, onde precisamos encontrar a soma dos quadrados dos números ímpares.

-Começando pela solução utilizando programação imperativa:

const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let sumOfSquaredOddNumbers = 0;

// Looping sobre cada número do array
for (let i = 0; i < numbers.length; i++) {
  // Verificando se o número é ímpar
  if (numbers[i] % 2 !== 0) {
    // Calculando o quadrado do número ímpar e adicionando à soma
    const squaredNumber = numbers[i] * numbers[i];
    sumOfSquaredOddNumbers += squaredNumber;
  }
}

console.log(sumOfSquaredOddNumbers); // Output: 165

-Agora com a sulução utilizando programação funcional:

const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
// Usando a função filter para filtrar apenas os números ímpares
const oddNumbers = numbers.filter(num => num % 2 !== 0);

// Usando a função map para calcular o quadrado de cada número ímpar
const squaredOddNumbers = oddNumbers.map(num => num * num);

// Usando a função reduce para somar os quadrados dos números ímpares
const sumOfSquaredOddNumbers = squaredOddNumbers.reduce((acc, num) => acc + num, 0);

console.log(sumOfSquaredOddNumbers); // Output: 165

Contudo, podemos perceber que a implementação funcional neste caso, é mais elegante, concisa e expressiva do que a solução que utiliza programação imperativa. Além disso, a solução funcional é mais fácil de ler e entender, pois as funções de array descrevem o que está sendo feito com o array, enquanto que o código imperativo descreve como está sendo feito.
Outra vantagem da solução funcional é que ela evita a necessidade de declarar variáveis desnecessárias, como no exemplo acima onde não precisamos de variáveis de controle adicionais para realizar a operação.
Por fim, a solução funcional é mais fácil de testar e depurar, pois as funções de array são imutáveis e não afetam o estado de outras variáveis no programa.
