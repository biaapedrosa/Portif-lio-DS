# Registro de Resolução de Conflito

**O que causou o conflito (qual arquivo, qual trecho)**
O conflito aconteceu no arquivo `exercicios/ex03-conflito/arquivo.txt`, especificamente na linha 1. O erro rolou porque eu editei exatamente essa mesma linha em duas branches diferentes (`feat/alteracao-a` e `feat/alteracao-b`). Quando fiz o merge da branch A na main, deu tudo certo. Mas quando fui tentar dar o merge da branch B logo em seguida, o Git acusou conflito porque não sabia qual das duas versões ele deveria manter para aquele trecho.

**Como você decidiu qual versão manter**
Abri o arquivo no VS Code e vi aquelas marcações esquisitas do Git (`<<<<<<< HEAD`, `=======` e `>>>>>>>`). Decidi que não queria manter só o texto da branch A nem só o da B. Apaguei todas as setas e códigos gerados pelo Git e reescrevi a linha na mão com uma versão final unindo as duas ideias: "Linha 1 modificada - Conflito resolvido unindo as duas branches!".

**O comando ou ação usada para marcar o conflito como resolvido**
Depois de ajeitar o texto e salvar o arquivo no editor, voltei para o terminal e usei o comando `git add exercicios/ex03-conflito/arquivo.txt`. Isso serve para avisar ao Git que eu já resolvi a bagunça manualmente. Em seguida, finalizei a união rodando o comando `git commit -m "fix(ex03): resolve conflito de merge no arquivo.txt"`.