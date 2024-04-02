fila.js

export function criarFila(tamanho = 10){

    return [... new Array (tamanho)]
   
   }
   
   export function  inserirItemFila (fila,item){
       const spacePosition = fila.indexOf(undefined);
       if(spacePosition === -1){
        console.log("Esta cheio");
        return; 
       }    
        
       fila[spacePosition] = item;
    }
   
   // 
   
   export function retirarItemFila (fila){
       if(fila[0] == undefined) {
           return
       }
   
       let itemPegado = fila[0]
   
       for(let i = 0; i < fila.length; i++) {
           fila[i] = fila[i + 1]
       }
   
       return itemPegado
    }



index.js

import  {criarFila, inserirItemFila, retirarItemFila}  from './fila.js'

console.log ("");
console.log("Minha fila!");
console.log ("");

const fila = criarFila(3)

//insere os itens na fila.
inserirItemFila(fila, "dado")
inserirItemFila(fila, "tabuleiro")
inserirItemFila(fila, "monopolly")

console.log("Fila", fila);

//vai fazer com que dois itens sejam retirados da fila.
retirarItemFila(fila)
retirarItemFila(fila)


console.log("Fila", fila);



export function filaVazia (fila)

If (fila [0]  ==  undefined){
 Console.log (----)
 Return}

Index. 


 *feito depois*

 
filaVazia (fila)

--------------------------------------------
limparFila (fila){
 
Fila.forEach ( item => ( 
Item = undefined))

}
 index 

limpar Fila (fila)
-------------------------------------------------


verificarTamanhoFila (fila)
  Return fila.lenght 

}

Index 



verificarTamanhoFila (fila)

---------------------------------------------------

verificarPrimeiroElemento (fila){
          filaVazia (fila)

Return fila [0]

}

---------------------------------------------------

verificarElementoFila (fila, elemento){
       Return fila.includes (elemento)

}
-------------------------------------------------------
verificarPosiçãoFila (fila, elemento) {
      If (fila.indexOf (elemento) === -1){

Console.log ( "fila não possui esse elemento") 

Return ;
}
 
RETURN fila.indexOf (elemento)
}

-------------------------------------#-

verificarFilaCheia (fila) {
  If (fila [fila.lenght- 1] != undefined){
    console.log (" Fila cheia")

Return ;
}

}



