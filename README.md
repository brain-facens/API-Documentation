# Estrutura de API | BRAIN
#### Versão: 1.0.0
#### Autores:
- Matheus Oliveira de Souza *(matheus.souza@facens.br)*

---
# Sumário:
- *[Sobre](#sobre)*
- *[Rotas](#rotas)*
    - *[About](#about)*
    - *[Inference](#inference)*
    - *[Training](#training)*
    - *[Playground](#playground)*

---
### Sobre
Documento informativo para a equipe BRAIN sobre o uso de APIs e sua padronização de rotas. Esse esquema deverá ser seguido afim de organizar todo e qualquer serviço de IA desenvolvido pelo BRAIN.

### Rotas
Cada rota deverá iniciar com o próprio nome do serviço/projeto do qual ela pertence seguido de sua versão. Como mostra o exemplo abaixo:
```
/{nome-do-projeto}/{versão}
```
Em seguida, deverá seguir o esquema de rotas mostrado abaixo:

- #### About
Rota destinada a informações sobre o serviço.
```
/{nome-do-projeto}/{versão}/about
```
Preferencialmente, uma simples página HTML contendo a documentação online do serviço.

- #### Inference
Rota destinada a qualquer tipo de inferência realizada pelo modelo.
```
/{nome-do-projeto}/{versão}/inference
```
Sendo a raiz ("/") a rota principal para a inferência, as demais possíveis rotas relacionas a inferência do modelo deverão se originar apartir dela.

- #### Training
Rota destinada a transferência de aprendizado do modelo, com o objetivo de gerar modelos com a mesma arquitetura mas para problemas diferentes.
```
/{nome-do-projeto}/{versão}/training
```
**O serviço de transferência de aprendizado não se torna obrigatório dependendo da complexidade de realizá-lo.*

- #### Playground
Rota padrão para as rotas **/inference** e **/training**, se trata de uma página web juntamente com uma interface para utilizar o serviço.
```
/{nome-do-projeto}/{versão}/inference/playground
/{nome-do-projeto}/{versão}/training/playground
```
Aonde, **/inference/playground** servirá como um ambiente para demostrações do serviço, enquanto **/training/playground** servirá para a tranferência de aprendizado de maneira mais "amigável" ao invés de se utilizar o **CLI** *(Command Line Interface)*.
