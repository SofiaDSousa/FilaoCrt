export function criarFila(tamanho = 10){
    return [... new Array (tamanho)];
}

export function inserirItemFila(queue, item){
    const spacePosition = queue.indexOf(undefined);
    if(spacePosition === -1){
        console.log("Está cheio");
        return;
    }
    queue[spacePosition] = item;
}

export function retirarItemFila(queue){
    if(queue[0] == undefined) {
        return;
    }

    let itemPegado = queue[0];

    for(let i = 0; i < queue.length; i++) {
        queue[i] = queue[i + 1];
    }

    return itemPegado;
}

export function filaVazia(queue) {
    if (queue[0] == undefined) {
        console.log("----");
        return;
    }
}

export function limparFila(queue) {
    queue.forEach(item => {
        item = undefined;
    });
}

export function verificarTamanhoFila(queue) {
    return queue.length;
}

export function verificarPrimeiroElemento(queue) {
    filaVazia(queue);
    return queue[0];
}

export function verificarElementoFila(queue, elemento) {
    return queue.includes(elemento);
}

export function verificarPosicaoFila(queue, elemento) {
    if (queue.indexOf(elemento) === -1) {
        console.log("Fila não possui esse elemento");
        return;
    }
    return queue.indexOf(elemento);
}

export function verificarFilaCheia(queue) {
    if (queue[queue.length - 1] != undefined) {
        console.log("Fila cheia");
        return;
    }
}

export function verificarUltimo(queue) {
    filaVazia(queue);
    return queue[queue.indexOf(undefined) - 1];
}


import { criarFila, inserirItemFila, retirarItemFila, filaVazia, limparFila, verificarTamanhoFila, verificarPrimeiroElemento, verificarElementoFila, verificarPosicaoFila, verificarFilaCheia, verificarUltimo } from './fila.js';

console.log("");
console.log("Minha fila!");
console.log("");

const queue = criarFila(3);

// Insere os itens na fila.
inserirItemFila(queue, "dado");
inserirItemFila(queue, "tabuleiro");
inserirItemFila(queue, "monopoly");

console.log("Fila", queue);

// Retira dois itens da fila.
retirarItemFila(queue);
retirarItemFila(queue);

console.log("Fila", queue);
