# Aula 13 - Introdução a SOA

## 1. O que é SOA?

**Definição:**  
Service-Oriented Architecture organiza aplicações como um conjunto de serviços interoperáveis, independentes de plataforma, com contratos bem definidos para integração.

**Exemplo didático:** Uma loja virtual pode usar SOA para integrar o sistema de estoque, pagamentos e logística, mesmo que cada um seja feito em tecnologias diferentes.

---

## 2. Princípios e fundamentos

- **Serviços como blocos de construção:** Função de negócio exposta via interface padronizada.
- **Interoperabilidade:** Comunicação entre sistemas heterogêneos (ex: Java, .NET, PHP).
- **Reusabilidade:** Serviços podem ser reaproveitados em múltiplos processos e aplicações.
- **Contratos claros (WSDL, OpenAPI):** Define como os serviços se comunicam.
- **Acoplamento fraco:** Alterações em um serviço não devem impactar outros.

---

## 3. Componentes principais

- **Serviço:** Unidade funcional (ex: pagamento, cadastro, autenticação).
- **Contrato de serviço:** Documentação formal do serviço (ex: SOAP/WSDL, REST/OpenAPI).
- **Barramento de Serviços (ESB):** Middleware que gerencia roteamento, transformação e orquestração de mensagens.
- **Registro de serviços (UDDI):** Catálogo para descoberta e reutilização de serviços.

---

## 4. Tecnologias e padrões

- **SOAP:** Protocolo XML para mensagens estruturadas.
- **REST:** Evolução para comunicação mais simples (HTTP/JSON).
- **WSDL:** Descreve interfaces SOAP.
- **UDDI:** Registro de serviços SOAP.
- **BPMN e BPEL:** Para orquestração de processos de negócio.

---

## 5. Benefícios (para iniciantes e avançados)

- **Integração de sistemas legados e modernos.**
- **Governança e padronização de APIs.**
- **Centralização de lógica de negócio.**
- **Facilita terceirização e integração com parceiros.**

---

## 6. Desafios práticos

- **Complexidade do ESB:** Pode virar gargalo ou ponto único de falha.
- **Sobrecarga de XML/SOAP:** Pode impactar desempenho em sistemas de alta demanda.
- **Governança:** Demanda processos rígidos para versionamento, segurança e monitoramento.

---

## 7. SOA vs. Microsserviços

| SOA                       | Microsserviços                 |
|---------------------------|-------------------------------|
| Serviços grandes          | Serviços pequenos e focados   |
| ESB central               | Orquestração distribuída      |
| SOAP/XML                  | REST/JSON, gRPC, eventos      |
| Mais comum em corporações | Cloud-native, startups, SaaS  |

---

## 8. Boas práticas e padrões

- **Design first:** Especifique contratos antes de implementar.
- **Versão de contratos:** Planeje evolução e compatibilidade.
- **Segurança:** Autenticação, autorização e criptografia de mensagens.
- **Monitoramento e logging:** Centralize logs e métricas.

---

## 9. Exemplos práticos

- **Governo eletrônico:** Integração entre sistemas de Receita Federal, bancos e cartórios.
- **Bancos tradicionais:** Integração entre sistemas legados, internet banking e parceiros.

---

## 10. Para arquitetos

- Avalie se SOA realmente é necessário (custo, benefícios, contexto).
- Combine SOA com API Management moderno.
- Planeje migração gradual para microsserviços onde fizer sentido.

---

## 11. Perguntas-chave e Respostas

**Quando SOA é melhor que microsserviços?**  
- SOA é melhor em cenários de integração de sistemas legados, com alta necessidade de padronização, governança centralizada, e quando existe uma grande variedade de tecnologias e protocolos distintos a serem integrados.

**Como evitar “ESB antipadrão” (bottleneck central)?**  
- Use ESB apenas para orquestração e integração. Não coloque lógica de negócio no ESB, distribua funções entre serviços, e adote arquitetura distribuída sempre que possível para evitar ponto único de falha.

**Como promover reuso sem criar dependência excessiva?**  
- Defina contratos claros, use versionamento bem planejado, documente interfaces e mantenha acoplamento fraco entre serviços, incentivando a reutilização sem dependências rígidas.

---

## 12. Referências

- SOA Patterns (Thomas Erl)
- Enterprise Integration Patterns (Gregor Hohpe, Bobby Woolf)
- Documentação oficial dos provedores de ESB

---