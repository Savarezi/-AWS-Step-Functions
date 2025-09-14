# -AWS-Step-Functions
 Aplicando na prática a criação de uma State Machine e documentando os resultados.

##

# 🚀 Desafio AWS Step Functions - DIO

Este repositório contém minha prática do desafio **Workflows Automatizados com AWS Step Functions**, parte da formação na [DIO](https://www.dio.me/).

O objetivo foi consolidar conceitos aprendidos durante as aulas, aplicando na prática a criação de uma **State Machine** e documentando os resultados.

---


---

## 🛠️ Tecnologias e Serviços Utilizados

- **AWS Step Functions**
- **AWS Lambda (integração simples)**
- **Amazon CloudWatch (monitoramento básico)**
- **Draw.io** para o fluxograma
- **GitHub** para versionamento e documentação

---

## 🔄 Fluxo da State Machine

### Diagrama Visual
.<img width="863" height="453" alt="Step Functions" src="https://github.com/user-attachments/assets/d3cfb538-4dda-458f-a4fa-b141f7801748" />

]

---

## 📂 Definição JSON

O código completo da máquina de estados está disponível em [`/state-machine/hello-world.json`](./state-machine/hello-world.json).

Trecho ilustrativo:

```json
{
  "Comment": "Exemplo Hello World com AWS Step Functions",
  "StartAt": "TaskInicial",
  "States": {
    "TaskInicial": {
      "Type": "Task",
      "Resource": "arn:aws:lambda:REGION:ACCOUNT_ID:function:hello-world",
      "Next": "VerificacaoResultado"
    },
    "VerificacaoResultado": {
      "Type": "Choice",
      "Choices": [
        {
          "Variable": "$.status",
          "StringEquals": "sucesso",
          "Next": "TaskFinal"
        },
        {
          "Variable": "$.status",
          "StringEquals": "pendente",
          "Next": "Aguardar"
        }
      ],
      "Default": "TratarErro"
    }
  }

```
##
💡 Insights e Aprendizados

A importância de definir bem os estados para prever cenários de erro.

Como o Choice State facilita a tomada de decisão dentro do fluxo.

O uso de Wait State para processos assíncronos.

Integração do CloudWatch para logs e monitoramento.

Boa prática: sempre estruturar o repositório com README, código e imagens organizados.

👉 Para mais detalhes pessoais sobre meu aprendizado, consulte o arquivo completo:  
[📘 insights.md](./docs/insights.md)


