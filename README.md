# Introdução

Esses recursos de estado entraram na biblioteca a partir da versão 16.8 e estão ligados ao gancho de estado, normalmente importado assim:

```
import React, { useState } from 'react';
```


---

Atenção: o import vem da biblioteca base, não da camada móvel.

Existe também o gancho de efeito colateral.

E o código desses ganchos é idêntico entre a versão web e a móvel.

O gancho sempre devolve uma função e uma variável.

A analogia usada em aula:

![analoy](images/analogia.png)

E a explicação:

![explanation](images/explicacao.png)

O exemplo mostrado era um contador que soma e subtrai; segundo a aula, o estado ali funciona de forma parecida com sessão em outra linguagem de servidor.

Criei um aplicativo de teste na pasta de testes.

Comando usado para criar:

```
npx create-expo-app basic-hooks -t
```

Já dentro da pasta criada, rodei:

```
npm run android
```

Repare que é preciso chamar uma função de tratamento, e é ela que aciona a função declarada na linha do gancho de estado.

![useState - example 01](images/exemplo-de-estado.png)


# Aplicativo de teste

Vale olhar o aplicativo que fiz, reparando em:

- o uso do gancho de estado;
- a função indicada no gancho não sendo declarada antes.


# Gancho de efeito

O gancho de efeito serve para lidar com efeitos colaterais.

Exemplo de uso:

![example of useEffect use](images/exemplo-de-efeito.png)

Também foi mostrado que não é preciso monitorar variável nenhuma.

![useEffect - we do not have to monitor a variable](images/efeito-sem-monitorar-variavel.png)

OBS: repare que a imagem usa os dois ganchos, o de efeito e o de estado.


# Redutor de estado

Como importar:

```
import {useReducer} from 'react'
```

Declarando para uso:

![useReducer - declaring the use](images/declarando-o-redutor.png)

A documentação oficial é uma ótima referência para estudar esses ganchos.

Agora veja o uso do redutor:

![example with 2 hooks -- useReducer](images/exemplo-com-dois-ganchos.png)

Explicando:

1. você indica a função despachante na linha em que declara o redutor;
2. na última linha da imagem essa função despachante aparece sendo chamada;
3. na mesma linha é possível ver que a função ouvinte está ligada ao redutor;
4. a função ouvinte recebe um parâmetro só, mas o redutor repassa a ela esse parâmetro e mais outro, na frente;
5. a função ouvinte recebe um objeto com duas chaves e valores;
6. no exemplo, o estado entregue automaticamente pelo redutor é usado dentro da função ouvinte;

Gravando as tarefas na tela:

![example with 2 hooks -- writing the tasks in the screen](images/gravando-tarefas-na-tela.png)

Comentário: o uso do redutor não parecia necessário ali; serviu só para exemplificar dois ganchos juntos.


# Repositório das aulas

O código usado está num repositório público da trilha.