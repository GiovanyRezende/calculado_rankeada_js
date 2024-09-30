# Cálculo de Rankeada
Esse é um projeto de JavaScript proposto pela [DIO](https://www.dio.me/). Se trata de um simples algoritmo para calcular o rendimento de um jogador em rankeadas. O objetivo é exerciar a lógica de programação.

## O que devia ser utilizado

- Variáveis;
- Operadores;
- Laços de repetição;
- Estruturas de decisões;
- Funções

# O código
```
let saldoVitorias = 0;
let victCount = 0;
let lossCount = 0;
let random = Math.floor(Math.random() * 2);
let nivel;
let i = 0;

function victCalc(vict,loss){
    return vict - loss
}

while(i !== 100){
    switch(random){
        case 0:
            lossCount++;
        case 1:
            victCount++;
    }
    random = Math.floor(Math.random() * 2);
    i++;
}

saldoVitorias = victCalc(victCount,lossCount);

if(saldoVitorias <= 10){
        nivel = "Ferro";
    }
    else if (saldoVitorias > 10 && saldoVitorias <= 20){
        nivel = "Bronze";
    }
    else if (saldoVitorias > 20 && saldoVitorias <= 50){
        nivel = "Prata";
    }
    else if (saldoVitorias > 50 && saldoVitorias <= 80){
        nivel = "Ouro";
    }
    else if (saldoVitorias > 80 && saldoVitorias <= 90){
        nivel = "Diamante";
    }
    else if (saldoVitorias > 90 && saldoVitorias <= 100){
        nivel = "Lendário";
    }
    else{
        nivel = "Imortal";
    }

console.log(`O Herói tem saldo de ${saldoVitorias} vitórias e está no nível de ${nivel}`);
  ```
