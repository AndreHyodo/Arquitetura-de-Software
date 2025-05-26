# Aula 10 - Cloud Computing

## 1. Introdução e Conceitos Básicos

**O que é computação em nuvem?**  
É um modelo que oferece recursos computacionais (servidores, armazenamento, banco de dados, redes, software) via internet, sob demanda, com escalabilidade automática e cobrança baseada no consumo.  
**Exemplo para iniciantes:** Usar o Google Drive para armazenar arquivos é computação em nuvem.

### **Evolução Histórica**
- Antes: Computação centralizada (mainframes), depois client-server, virtualização, até chegar à nuvem.
- Hoje: Nuvem é padrão para empresas de todos os portes.

---

## 2. Modelos de Serviço

### **IaaS (Infraestrutura como Serviço)**
- **Para quem:** Equipes de TI que querem controle sobre servidores e redes.
- **Responsabilidade:** Cliente gerencia SO, aplicações e dados.
- **Exemplo:** Amazon EC2 permite criar e gerenciar máquinas virtuais.
- **Dica avançada:** Ideal para arquiteturas que exigem flexibilidade máxima ou integração com sistemas legados.

### **PaaS (Plataforma como Serviço)**
- **Para quem:** Desenvolvedores que querem agilidade sem gerenciar infraestrutura.
- **Responsabilidade:** Cliente foca no código, provedor cuida do resto.
- **Exemplo:** Heroku, Google App Engine.
- **Tópico avançado:** Serverless é uma evolução do PaaS.

### **SaaS (Software como Serviço)**
- **Para quem:** Usuários finais e empresas que querem soluções completas.
- **Responsabilidade:** Cliente só gerencia usuários e dados.
- **Exemplo:** Salesforce, Office365, Gmail.
- **Para arquitetos:** Avalie integração via APIs e extensibilidade.

---

## 3. Tipos de Nuvem

- **Pública:** Recursos compartilhados entre múltiplos clientes. Barata, escalável, mas menos controle.
- **Privada:** Infraestrutura exclusiva de uma organização, maior controle e segurança.
- **Híbrida:** Combinação das anteriores, aproveitando o melhor de cada modelo.
- **Multicloud:** Uso de múltiplos provedores para evitar dependência (“vendor lock-in”).

---

## 4. Vantagens e Benefícios

- **Escalabilidade e Elasticidade:** Aumenta ou reduz recursos conforme a demanda.
- **Custo sob demanda:** Paga apenas pelo que usa.
- **Alta disponibilidade e redundância:** Provedores oferecem SLAs robustos e replicação geográfica.
- **Redução de complexidade:** Menos preocupação com hardware físico.
- **Automação:** Provisionamento e monitoramento automáticos.

**Para arquitetos:**  
- Facilita DevOps, CI/CD, infraestrutura como código e microserviços.

---

## 5. Desafios e Riscos

- **Segurança:** Dados em servidores de terceiros exigem cuidados extras.
- **Latência:** Distância entre usuário e servidor pode causar lentidão.
- **Dependência de fornecedor (vendor lock-in):** Dificuldade em migrar para outro provedor.
- **Regulamentação:** Atenção às leis de proteção de dados (ex: LGPD).
- **Custos ocultos:** Tráfego de dados, licenças, recursos não provisionados corretamente.

---

## 6. Tendências Atuais

- **Serverless (FaaS):** Executa funções sem gerenciar servidores (ex: AWS Lambda, Azure Functions).
- **Containers e Orquestração:** Docker, Kubernetes, OpenShift.
- **Edge Computing:** Processamento de dados próximo ao usuário, reduzindo latência.
- **Inteligência Artificial e Machine Learning como serviço.**

---

## 7. Boas Práticas

- **Escolha a nuvem e modelo de serviço adequado ao seu caso de uso.**
- **Automatize o provisionamento:** Use ferramentas como Terraform, Ansible, CloudFormation.
- **Implemente observabilidade:** Monitoramento, logs centralizados, alertas.
- **Planeje a segurança desde o design.**

---

## 8. Perguntas para Reflexão e Respostas

**Quando migrar para a nuvem faz sentido?**  
- A migração faz sentido quando a organização precisa de escalabilidade, elasticidade, quer pagar apenas pelo que usa, necessita de alta disponibilidade, deseja acelerar a inovação ou não quer investir em infraestrutura própria. Também é recomendada quando a manutenção de data centers locais se torna cara e operacionalmente complexa.

**Como garantir portabilidade entre diferentes provedores?**  
- Utilize containers (ex: Docker), orquestradores portáveis (Kubernetes), padrões abertos, evite serviços proprietários exclusivos, automatize infraestrutura com ferramentas como Terraform e armazene dados em formatos padrão. Automatize deploys e utilize APIs e tecnologias que funcionem em múltiplos ambientes (multicloud).

**Quais workloads devem permanecer on-premises?**  
- Workloads que exigem latência muito baixa, requisitos de compliance/regulação rígidas, dependência de hardware específico, integração profunda com sistemas locais, dados altamente sensíveis ou quando o custo da nuvem não compensa para cargas estáveis e previsíveis.

---

## 9. Para quem quer se aprofundar

- **Arquiteturas cloud-native:** 12-factor apps, microserviços, APIs.
- **Design para resiliência:** Chaos Engineering, circuit breaker, fallback.
- **Compliance:** Certificações e regulamentações para ambientes cloud.

---

## 10. Referências e Ferramentas

- AWS Well-Architected Framework
- Google Cloud Architecture Center
- Azure Architecture Center
- Ferramentas: Terraform, Kubernetes, Prometheus, Grafana

---