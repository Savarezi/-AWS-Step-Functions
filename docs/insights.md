
---



```markdown
# 📘 Insights e Reflexões - AWS Step Functions

Este documento reúne minhas anotações e aprendizados práticos durante o desafio da DIO sobre **Workflows Automatizados com AWS Step Functions**.

---

## 🛠️ Primeiros Passos

- Iniciei utilizando o **AWS Free Tier**, garantindo que não houvesse custo na execução dos testes.  
- Criei a minha primeira **State Machine** a partir do exemplo **Hello World** disponibilizado pela AWS.  
- A partir daí, fui modificando para entender como funcionam os diferentes estados: `Task`, `Choice`, `Wait` e tratamento de erro com `Catch`.

---

## 🔄 Aprendizados sobre os Estados

- **Task** → É onde realmente algo acontece, como chamar uma função Lambda.  
- **Choice** → Permite tomar decisões condicionais dentro do fluxo.  
- **Wait** → Super útil para aguardar antes de seguir para o próximo passo, simulando processos assíncronos.  
- **Catch / Retry** → Mostram como lidar com falhas (transientes ou persistentes), reforçando a resiliência do fluxo.  

---

## 📊 Visualização

- Utilizei o **console da AWS** para validar a execução e observar a transição entre estados.  
- Criei diagramas no **Draw.io** para deixar mais claro o fluxo e facilitar futuras consultas.  
- Essa parte visual foi essencial para fixar a lógica e estruturar melhor a documentação no GitHub.

---

## 💡 Reflexões Pessoais

- O Step Functions me mostrou como **orquestrar serviços da AWS de forma declarativa**.  
- Achei muito interessante como ele permite montar um fluxo **sem escrever código complexo**, apenas configurando os estados.  
- Entendi que, no mundo real, isso pode ser usado para **processamento de pedidos, ETL, automação de pipelines de dados e até microservices**.  
- Documentar tudo no GitHub foi um exercício importante para consolidar o aprendizado e ainda criar um material de apoio para o futuro.

---

## 🚀 Próximos Passos

- Testar integrações mais avançadas com **SQS e SNS** dentro de um fluxo.  
- Explorar **Step Functions Express Workflows** (voltado para execuções de alta frequência e curta duração).  
- Automatizar deploy da definição com **CloudFormation ou Terraform**.  

---

✍️ **Autor:** Paty  
📌 *Parte do desafio "Workflows Automatizados com AWS Step Functions" - DIO.*
