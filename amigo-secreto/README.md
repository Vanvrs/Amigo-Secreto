# Sorteio de Amigo Secreto Alura

Prática de Lógica de Programação com o desafio de um aplicativo de sorteio de amigo secreto

## Funcionalidades

- Sorteio de amigo secreto
- Função para garantir que a pessoa não retire seu próprio nome como amigo secreto
- Função para otimizar o embaralhamenti da lista de pessoas 

## Tecnologia aplicada

Javascript, HTML, CSS...

## Uso/Exemplos

#### Função de embaralhamento de array

```javascript
function embaralhaArray(arr) {
  for (let i = arr.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [arr[i], arr[j]] = [arr[j], arr[i]];
  }
}
```

#### Função de sorteio

```javascript
function sortear() {
  elemListaSorteio.innerHTML = "";

  embaralhaArray(amigos);
  for (i = 0; i < amigos.length; i++) {
    if (i == amigos.length - 1) {
      elemListaSorteio.innerHTML += `${amigos[i]} --> ${amigos[0]}<br>`;
    } else {
      elemListaSorteio.innerHTML += `${amigos[i]} --> ${amigos[i + 1]}<br>`;
    }
  }
}
```

## Autora

- (https://www.github.com/vanvrs)
