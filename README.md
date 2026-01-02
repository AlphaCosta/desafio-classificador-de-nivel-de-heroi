
# Classificador de Nível de Herói 🛡️⚔️

Um projeto simples em **JavaScript** que classifica o nível de um herói com base na sua quantidade de **XP (Experiência)**. Este desafio é parte do treinamento da **DIO** e utiliza **variáveis, operadores, laços de repetição e estruturas de decisão**.

> **Saída esperada:**  
> `O Herói de nome {nome} está no nível de {nivel}`

---

## 🧠 Regras de Classificação

De acordo com o desafio, os níveis são determinados assim:

- **Ferro**: XP menor do que **1.000**  
- **Bronze**: XP entre **1.001** e **2.000**  
- **Prata**: XP entre **2.001** e **5.000**  
- **Ouro**: XP entre **5.001** e **7.000**  
- **Platina**: XP entre **7.001** e **8.000**  
- **Ascendente**: XP entre **8.001** e **9.000**  
- **Imortal**: XP entre **9.001** e **10.000**  
- **Radiante**: XP **maior ou igual a 10.001**

> **Observação:** Para evitar sobreposição de intervalos, foi adotado o seguinte padrão:
> - `0–1000` → Ferro  
> - `1001–2000` → Bronze  
> - `2001–5000` → Prata  
> - `5001–7000` → Ouro  
> - `7001–8000` → Platina  
> - `8001–9000` → Ascendente  
> - `9001–10000` → Imortal  
> - `>= 10001` → Radiante

---

## 📂 Estrutura do Projeto

```
.
├── README.md
└── index.js
```

---

## ▶️ Como executar

1. Garanta que você tem o **Node.js** instalado.
2. Salve o código em um arquivo, por exemplo `index.js`.
3. No terminal, execute:
   ```bash
   node index.js
   ```

---

## 🧪 Código (versão simples)

```javascript
// Desafio: Classificador de nível de Herói

let nome = "Master Sauro";
let xp = 7001;
let nivel = "";

if (xp <= 1000) {
  nivel = "Ferro";
} else if (xp >= 1001 && xp <= 2000) {
  nivel = "Bronze";
} else if (xp >= 2001 && xp <= 5000) {
  nivel = "Prata";
} else if (xp >= 5001 && xp <= 7000) {
  nivel = "Ouro";
} else if (xp >= 7001 && xp <= 8000) {
  nivel = "Platina";
} else if (xp >= 8001 && xp <= 9000) {
  nivel = "Ascendente";
} else if (xp >= 9001 && xp <= 10000) {
  nivel = "Imortal";
} else {
  nivel = "Radiante";
}

console.log(`O Herói de nome ${nome} está no nível de ${nivel}`);
```

---

## 🧩 Versão com função reutilizável (opcional)

```javascript
function classificarHeroi(nome, xp) {
  let nivel = "";

  if (xp <= 1000) {
    nivel = "Ferro";
  } else if (xp >= 1001 && xp <= 2000) {
    nivel = "Bronze";
  } else if (xp >= 2001 && xp <= 5000) {
    nivel = "Prata";
  } else if (xp >= 5001 && xp <= 7000) {
    nivel = "Ouro";
  } else if (xp >= 7001 && xp <= 8000) {
    nivel = "Platina";
  } else if (xp >= 8001 && xp <= 9000) {
    nivel = "Ascendente";
  } else if (xp >= 9001 && xp <= 10000) {
    nivel = "Imortal";
  } else {
    nivel = "Radiante";
  }

  return `O Herói de nome ${nome} está no nível de ${nivel}`;
}

// Exemplo de uso:
console.log(classificarHeroi("Master Sauro", 7001));
```

---

## 🔍 Exemplos de teste

```javascript
console.log(classificarHeroi("Aeryn", 999));    // Ferro
console.log(classificarHeroi("Boromir", 1500)); // Bronze
console.log(classificarHeroi("Ceres", 4500));   // Prata
console.log(classificarHeroi("Doran", 6500));   // Ouro
console.log(classificarHeroi("Elyra", 7200));   // Platina
console.log(classificarHeroi("Falk", 8500));    // Ascendente
console.log(classificarHeroi("Gwen", 9500));    // Imortal
console.log(classificarHeroi("Hector", 14500)); // Radiante
```

---

## 🧭 Fluxo de decisão (resumo)

```text
XP <= 1000        -> Ferro
1001–2000         -> Bronze
2001–5000         -> Prata
5001–7000         -> Ouro
7001–8000         -> Platina
8001–9000         -> Ascendente
9001–10000        -> Imortal
>= 10001          -> Radiante
```

---

## 👤 Autor

**Alex Costa**

---

## 📝 Licença

Sinta-se livre para usar e adaptar.
