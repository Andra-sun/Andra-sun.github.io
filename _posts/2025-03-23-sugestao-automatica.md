---
title: Sugestão Automática.
description: Dia 15 do projeto 30 dias com js
tag: [js, programação, front-end, desafio]
category: [30days]
date: 2025-03-23 14:56:00 -03:00
image: "https://assets.dio.me/NE7uaL6XGP-9iGInOaN5IGlCkhpX-81xNRT38bh__J0/f:webp/q:80/L2FydGljbGVzL2NvdmVyL2E0YjUyMjFjLTVkMzgtNGY4Mi04MzBlLTc4YTY1NWI4N2RlNi5qcGc"
---

Chegamos à terceira semana do projeto!

O objetivo desta vez foi criar um **input com sugestões de texto em tempo real**. Para isso, existem várias abordagens possíveis, e eu escolhi utilizar um **JSON contendo uma lista de linguagens de programação**.

No **HTML**, criei um **input** e uma **div vazia**, que será usada para exibir as sugestões.

Já no **JavaScript**, desenvolvi a função `Sugestao`. Ela importa a lista do JSON e, conforme o usuário digita no input, faz uma busca por palavras que contenham as mesmas letras. Quando o usuário **clica em uma sugestão**, o campo de entrada é preenchido automaticamente com o texto selecionado, e a lista de sugestões é limpa.


```js
function Sugestao() {
    const listaDeSugestaoUrl = "/listaDeSugestao.json";
    const input = document.getElementById("pesquisa");
    const caixaDeSugestao = document.getElementById("sugestao");

    fetch(listaDeSugestaoUrl)
        .then((response) => response.json())
        .then((listaDeSugestao) => {
            input.addEventListener("input", () => {
                const query = input.value.toLowerCase();
                caixaDeSugestao.innerText = "";

                if (query) {
                    const addSugestao = listaDeSugestao.filter((item) =>
                        item.toLowerCase().includes(query)
                    );
                    addSugestao.forEach((sugestao) => {
                        const div = document.createElement("div");
                        div.textContent = sugestao;
                        div.addEventListener("click", () => {
                            input.value = sugestao;
                            caixaDeSugestao.innerHTML = "";
                        });
                        caixaDeSugestao.appendChild(div);
                    });
                }
            });
        })
        .catch((error) =>
            console.error("Erro ao carregar a lista de sugestões:", error)
        );

    document.addEventListener("click", (e) => {
        if (e.target !== input) {
            caixaDeSugestao.innerHTML = "";
        }
    });
}

Sugestao();

```
{: file="sugestao.js" }

---
O resultado final você pode conferir
[aqui](https://andra-sun.github.io/30DaysJs/Day15//)
<br/>
[link para o repositorio do projeto](https://github.com/Andra-sun/30DaysJs)

