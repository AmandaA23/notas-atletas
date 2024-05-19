# notas-atletas

##Projeto: Calcular média dos atletas

Observações/especificações:

function calcularMedia(atletas) {
  atletas.forEach(atleta => {
    let notas = atleta.notas;
    
Inicialmente, foi criada uma função chamada calcularMedia, em seguida foi utilizada o metodo forEach(), que permite iterar cada elemento dentro da uma matriz, no código utilizamos uma função callback para percorrer cada objeto atleta no array atletas.

notas.sort((a, b) => a - b)
let notasEliminadas = notas.slice(1, 4)

Para eliminar a maior e menor nota de cada atleta foi preciso ordenar o array de notas de cada atleta, utilizanda o metodo .sort() que foi ordenada na forma crescente atribuida numa função callback, "a" e "b" são dois elementos do array que estão sendo comparados,a função retorna a diferença entre a e b.

em seguida, foi utilizado o metodo.slice() para eliminar a maior e menor nota de cada atleta, sem alterar o array original
  
  
