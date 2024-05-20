# notas-atletas

##Projeto: Calcular média dos atletas

Observações/especificações:

a)A média é calculada com base nas três notas do meio, desconsiderando a maior e menor nota.
b)Apresentar ao usuário o nome de cada atleta, seguido das notas e média calculada.


1.

function calcularMedia(atletas) {
  atletas.forEach(atleta => {
    let notas = atleta.notas;
    
Inicialmente, foi criada uma função chamada calcularMedia, em seguida foi utilizado o metodo forEach(), que permite iterar cada elemento dentro da uma matriz, no código utilizamos uma função callback para percorrer cada objeto atleta no array atletas.

2.

notas.sort((a, b) => a - b)
let notasEliminadas = notas.slice(1, 4)

Para eliminar a maior e menor nota de cada atleta foi preciso ordenar o array de notas, utilizanda o metodo .sort() que foi ordenada na forma crescente atribuida numa função callback, "a" e "b" são dois elementos do array que estão sendo comparados, a função retorna a diferença entre "a" e "b".

Em seguida, foi utilizado o metodo.slice() para ter um subconjunto do array, sendo selecionados os elementos nos índices 1 a 3 (inclusive), sobrando as notas do meio de cada atleta, e sem modificar o array original.

3.

let soma = 0;
    for (let i = 0; i < notasEliminadas.length; i++) {
      soma += notasEliminadas[i];
    }

Aqui, uma variável chamada soma é declarada e inicializada com o valor 0. Esta variável será usada para acumular a soma dos elementos do array notasEliminadas.
Esta linha inicia um laço(loop) "for" que irá iterar sobre todos os elementos do array notasEliminadas.

  let i = 0; inicializa a variável de controle i com o valor 0, indicando que o laço começará pelo primeiro elemento do array (índice 0).
  i < notasEliminadas.length; é a condição de continuação do laço. O laço continuará enquanto i for menor que o comprimento do array notasEliminadas.
  i++ incrementa o valor de i em 1 após cada iteração, movendo-se para o próximo elemento do array.

Dentro do laço, esta linha adiciona o valor do elemento atual (notasEliminadas[i]) à variável soma.

  notasEliminadas[i] acessa o elemento do array notasEliminadas na posição i.
  soma += notasEliminadas[i]; é uma forma abreviada de escrever soma = soma + notasEliminadas[i];.
  Esta operação adiciona o valor do elemento atual à soma acumulada.

4.
   let media = soma / notasEliminadas.length

  
Para calcular a media, foi atribuida a variavel soma que é uma variável previamente calculada que contém a soma de todos os elementos do array notasEliminadas.

notasEliminadas é o array que contém os elementos cujas notas queremos calcular a média.

.length é uma propriedade do array que retorna o número de elementos nesse array. 

5.
    console.log(`Atleta: ${atleta.nome}`);
    console.log(`Notas Obtidas: ${atleta.notas.join(",")}`);
    console.log(`Média Válida: ${media}`);
    console.log('');
  });
}

calcularMedia(atletas);

Finalmente, calcularMedia(atletas) executa a função calcularMedia, passando o array atletas como argumento.
A função processa cada atleta no array, calcula a média válida das notas (excluindo a menor e a maior), e exibe os resultados no console.
No console é exibido o nome de cada atleta, as notas obtidas e a media.

  


    


  
  
