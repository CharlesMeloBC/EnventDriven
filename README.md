# Arquitetura Orientada a Eventos e Bounded Context

## Introdução

A **Arquitetura Orientada a Eventos (Event-Driven Architecture - EDA)** é um modelo arquitetural baseado na produção, detecção, consumo e reação a eventos. Quando aplicada dentro do **Domain-Driven Design (DDD)**, a EDA se alinha com o conceito de **Bounded Context**, garantindo que diferentes domínios da aplicação possam se comunicar por meio de eventos.

---

## Conceitos Fundamentais

### **Bounded Context**

O **Bounded Context** define limites claros dentro de um domínio, onde um modelo específico é aplicado com uma linguagem e regras bem definidas. Esses contextos podem se comunicar por meio de eventos.

![alt text](https://martinfowler.com/bliki/images/boundedContext/sketch.png)

### **Microsserviços e Eventos**

A arquitetura de **microsserviços** se beneficia da EDA, pois cada serviço pode operar de forma independente, reagindo a eventos relevantes sem dependências rígidas.

**Espaço para imagem: Exemplo de comunicação entre microsserviços usando eventos.**

### **Pub-Sub (Publicar-Subscribir)**

O modelo **pub-sub** desacopla produtores e consumidores, permitindo que eventos sejam distribuídos para vários assinantes.

**Vantagens:**
- Escalabilidade;
- Desacoplamento entre serviços;
- Flexibilidade na comunicação.

**Espaço para imagem: Exemplo de arquitetura pub-sub.**

### **Streaming de Eventos**

O **event streaming** permite processar eventos em tempo real, utilizando tecnologias como **Apache Kafka** e **AWS Kinesis**.

**Benefícios:**
- Processamento contínuo de eventos;
- Persistência para reprocessamento;
- Análises em tempo real.

**Espaço para imagem: Fluxo de eventos com streaming.**

---

## Padrões Avançados

### **Conformist Model**

No **Conformist Model**, um contexto consumidor adota diretamente o modelo de eventos definido pelo produtor, reduzindo a necessidade de transformações.

**Vantagens:**
- Simplicidade na implementação;
- Redução da complexidade de integração.

**Desafios:**
- Dependência direta do produtor.

**Espaço para imagem: Exemplo de Conformist Model.**

### **Anticorruption Layer (ACL)**

O **Anticorruption Layer** protege um contexto contra mudanças indesejadas de outro contexto, evitando dependências diretas.

**Benefícios:**
- Isolamento entre domínios;
- Maior estabilidade do sistema.

**Espaço para imagem: Exemplo de Anticorruption Layer entre dois contextos.**

### **Open Host Service (OHS) & Published Language**

- **Open Host Service (OHS):** Expõe um serviço bem definido para permitir interações externas sem acoplamento direto.
- **Published Language:** Define uma linguagem comum para facilitar a comunicação entre contextos.

**Espaço para imagem: Exemplo de OHS e Published Language.**

---

## Gerenciamento de Transações

### **Choreography-Based SAGA**

No modelo **Choreography-Based SAGA**, os microsserviços reagem a eventos e coordenam transações distribuídas sem um orquestrador central.

**Vantagens:**
- Descentralização do fluxo de processos;
- Maior escalabilidade.

**Espaço para imagem: Exemplo de Choreography-Based SAGA.**

### **Orchestration-Based SAGA**

No modelo **Orchestration-Based SAGA**, um serviço centralizado gerencia a execução das etapas da transação distribuída.

**Vantagens:**
- Controle mais rígido do fluxo de eventos;
- Facilidade na implementação de rollback.

**Espaço para imagem: Exemplo de Orchestration-Based SAGA.**

---

## Conclusão

A **Arquitetura Orientada a Eventos**, combinada com **Bounded Contexts**, oferece um modelo altamente escalável e flexível para aplicações distribuídas. Com padrões como **Pub-Sub, Streaming, Anticorruption Layer, Open Host Service, SAGA e Conformist Model**, é possível criar sistemas resilientes e desacoplados.

Se precisar de mais detalhes ou exemplos práticos, basta preencher os espaços com imagens e diagramas para ilustrar os conceitos!
