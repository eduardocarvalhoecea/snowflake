
# Definições de Competências

A seguir, a descrição de cada indicador para uso na avaliação (notas de 1 a 5).

---

## 1. Technical Skills

### 1.1 Code

#### 1.1.1 Implementation  
Entrega soluções técnicas corretas, eficientes e alinhadas aos padrões da empresa. Envolve escrever código ou esquemáticos, configurar periféricos, montar pipelines de automação e garantir que a solução funcione conforme requisitos.

Avalia a capacidade de entregar soluções técnicas corretas, eficientes e alinhadas aos padrões da empresa.

---

##### **1 – Fundamenta Competência**
**Descrição:** Entrega o mínimo funcional, seguindo instruções passo a passo e padrões estabelecidos.  

**Example behaviors:**  
- Segue estritamente um checklist sem antecipar problemas.  
- Depende de orientação para cada etapa e revisa o próprio trabalho apenas após feedback.  
- Não considera cenários de falha além do exemplo dado.  

**Example tasks:**  
- **HW/FW:** Configurar I²C para leitura de sensor conforme tutorial, sem tratar erros de bus.  
- **Software:** Criar um endpoint simples que retorna texto estático; sem validação ou testes.  
- **TI:** 
    - Instalar e configurar um servidor web seguindo documentação oficial, sem ajustes de segurança.
    - Registrar manualmente novo SIM card em planilha, anotando ICCID e plano, sem usar o sistema de gestão.  

---

##### **2 – Contribuidor Consistente**
**Descrição:** Trabalha de forma quase autônoma em tarefas rotineiras, mas ainda requer revisão em detalhes críticos.  

**Example behaviors:**  
- Lembra de adicionar logs básicos e verifica seu próprio código/esquemático.  
- Lida com erros conhecidos, mas esquece casos de borda.  
- Ajuda colegas em dúvidas, porém precisa de confirmação antes de finalizar.  

**Example tasks:**  
- **HW/FW:** Escrever driver UART com retry após timeout, mas sem relatório detalhado de falhas.  
- **Software:** Implementar CRUD simples em framework (Express/Django) com testes unitários básicos.  
- **TI:** 
    - Criar script de backup automático com retry e log, mas sem alertas em caso de falha persistente.  
    - Importar lote de SIM cards no sistema de gestão via CSV, mas sem validar atributos (data de expiração, status).

---

##### **3 – Desempenho Confiável**
**Descrição:** Entrega soluções estáveis, prevendo cenários de falha comuns e integrando testes automáticos.  

**Example behaviors:**  
- Antecipar e tratar timeouts, gargalos de recursos e condições de erro típicas.  
- Configurar e usar ferramentas de teste/monitoramento mínimo sem supervisão.  
- Compartilha aprendizados e atualiza documentação interna.  

**Example tasks:**  
- **HW/FW:** Desenvolver biblioteca modular de SPI com testes unitários em CI e documentação de API.  
- **Software:** Dockerizar microserviço, implementar testes de integração e rodar pipeline CI/CD completo.  
- **TI:** 
    - Provisionar servidores via Ansible com validação de linting e playbook idempotente. 
    - Desenvolver script Python que carrega automaticamente SIM cards ao sistema de gestão, atribuindo planos e status. 

---

##### **4 – Proativo na Otimização**
**Descrição:** Identifica e resolve gargalos, propõe refatorações e automações que beneficiam a equipe inteira.  

**Example behaviors:**  
- Sugere melhorias de arquitetura ou processos antes de serem solicitadas.  
- Conduz revisões de design para todo o time, mentorando na adoção de padrões.  
- Automatiza workflows repetitivos, liberando tempo dos colegas para tarefas críticas.  

**Example tasks:**  
- **HW/FW:** Refatorar bootloader para reduzir tempo de inicialização em 30% e automatizar deep-sleep.  
- **Software:** Quebrar monólito em serviços desacoplados, reduzindo latência de 200 ms para 50 ms.  
- **TI:** 
    - Implementar pipeline de patching seguro (scripts, agendamento, relatórios e alertas) para todos os servidores.  
    - Criar módulo Ansible para provisionar SIM cards em estoque, incluindo parametrização de fornecedor e data de validade. 

---

##### **5 – Inova e Eleva Padrões**
**Descrição:** Cria frameworks, templates e ferramentas que se tornam referência e elevam o nível de toda a organização.  

**Example behaviors:**  
- Lidera iniciativas estratégicas de melhoria contínua e set-up de práticas de excelência.  
- Publica guias internos e treina times em novas metodologias.  
- Atua como mentor sênior, influenciando roadmap técnico e cultural da empresa.  

**Example tasks:**  
- **HW/FW:** Desenvolver HAL unificado (ESP32, STM32, Arduino) com CLI para flashing e HIL automáticos.  
- **Software:** Criar framework interno de geração de APIs e SDKs, com documentação, testes de contrato e deploy automatizado.  
- **TI:** 
    - Projetar e implementar plataforma self-service de CI/CD para equipes de TI e DevOps, com dashboards de health-checks e compliance.  
    - Implementar framework interno CLI que gerencia todo o ciclo de vida do SIM card (estoque, ativação, expiração) integrando sistema de gestão, ERP e APIs de operadora.  

#### 1.1.2 Quality & Testing  
Garante robustez e confiabilidade por meio de testes (unitários, de integração, HIL), revisão de código/esquemáticos e uso de ferramentas de análise estática. Inclui automação de pipelines de teste e adoção de boas práticas de cobertura.

Avalia a capacidade de garantir robustez e confiabilidade por meio de testes, revisão e automação de qualidade. 

---

##### **1 – Fundamenta Competência**
**Descrição:** Executa testes mínimos seguindo scripts manuais; não cria novos casos de teste nem automatizações.  

**Example behaviors:**  
- Executa teste manual de funcionalidade única, sem registrar resultados detalhados.  
- Roda checklists fornecidos, sem adaptar a novos cenários de falha.  
- Depende de QA ou colegas para planejar casos de teste.  

**Example tasks:**  
- **HW/FW:** Conecta osciloscópio e verifica sinal de clock em um ponto específico, registrando “pass/fail” em planilha.  
- **Software:** Executa testes unitários existentes localmente, sem adicionar novos casos; copia comandos de README.  
- **TI:** 
    - Verifica manualmente se serviços estão ativos (systemctl status) e registra resultado em relatório diário.  
    - Testar manualmente ativação de um SIM card em um único modem e registrar “pass/fail” em planilha.  

---

##### **2 – Contribuidor Consistente**
**Descrição:** Cria casos de teste básicos e scripts de verificação, mas com cobertura limitada e pouca automação.  

**Example behaviors:**  
- Adiciona testes unitários para funções centrais, mas omite cenários de erro.  
- Usa ferramentas de linting/analysis, mas não configura integração no pipeline.  
- Documenta casos de falha conhecidos, mas sem evoluir o catálogo de testes.  

**Example tasks:**  
- **HW/FW:** Escreve teste JUnit-like para driver I²C em simulação, cobrindo leitura/escrita, mas não timeout nem NACK.  
- **Software:** Implementa testes unitários em Jest ou PyTest cobrindo 70% de uma camada de negócio, sem mocks de dependências externas.  
- **TI:** 
    - Cria script de health-check automático que testa portas de serviço, mas não envia alertas em falha.  
    - Criar checklist de ativação de SIM cards e seguir manualmente para lote de 5 unidades.  

---

##### **3 – Desempenho Confiável**
**Descrição:** Integra testes unitários e de integração ao CI, mede cobertura e captura regressões sem supervisão.  

**Example behaviors:**  
- Configura pipeline para falhar build em cobertura abaixo de meta.  
- Automatiza testes de hardware-in-the-loop para CEPAS de comunicação.  
- Analisa relatórios de cobertura e corrige gaps críticos.  

**Example tasks:**  
- **HW/FW:** Monta banco de testes HIL para comunicação SPI e executa em GitHub Actions, com geração automática de relatórios.  
- **Software:** Configura pipeline GitHub Actions que roda testes unitários, de integração e static analysis, bloqueando merges com erros.  
- **TI:** 
    - Implementa monitoramento com Nagios/Prometheus que testa serviços e dispara alertas via Telegram e email em cada falha.  
    - Escrever script PowerShell que ativa e desativa SIM cards em homologação, gera CSV com resultados.  

---

##### **4 – Proativo na Otimização**
**Descrição:** Amplia cobertura de testes, introduz frameworks e gera relatórios que guiam melhorias contínuas.  

**Example behaviors:**  
- Identifica áreas de risco em código/esquemáticos e prioriza criação de testes para elas.  
- Conduz workshops de melhores práticas de QA/Testes para toda a equipe.  
- Automatiza geração de métricas de qualidade (MTTR, flakiness).  

**Example tasks:**  
- **HW/FW:** Desenvolve framework de testes end-to-end para placas custom, incluindo scripts de setup e teardown automáticos.  
- **Software:** Introduz Pact ou Postman CI para contract testing entre microserviços, assegurando compatibilidade.  
- **TI:** 
    - Cria dashboards Grafana com métricas de disponibilidade, tempo médio de resposta e tempos de execução de scripts de manutenção.  
    - Desenvolver testes automatizados em Python que simulam ativação em modems celulares e satélite, validando respostas de API.  

---

##### **5 – Inova e Eleva Padrões**
**Descrição:** Define políticas, frameworks e ferramentas de QA que se tornam padrão corporativo; mentor de cultura de qualidade.  

**Example behaviors:**  
- Formula guidelines de TDD/BDD para desenvolvimento cross-team e treina times.  
- Pesquisa e adota novas ferramentas de fuzzing, coverage ou análise estática avançada.  
- Representa a empresa em conferências internas/externas sobre qualidade de software e sistemas embarcados.  

**Example tasks:**  
- **HW/FW:** Publica e mantém biblioteca de testes parametrizáveis (pytest-like) para automação de validação de firmware em múltiplas plataformas.  
- **Software:** Constrói e documenta um framework interno de BDD (Cucumber, SpecFlow) integrado ao CI e pipelines de release.  
- **TI:** 
    - Projeta e implementa plataforma de “Quality as Code”, onde playbooks Ansible/Terraform são validados automaticamente antes de cada alteração de infraestrutura.  
    - Lançar suíte end-to-end em CI/CD que testa fluxo completo de aquisição, ativação e expiração de SIM cards, bloqueando merges em falhas.  


#### 1.1.3 Debugging & Monitoring  
Identifica, isola e corrige falhas em desenvolvimento e produção. Usa debuggers (JTAG, SWO), analisadores lógicos, logs e métricas (Grafana, UART prints), constrói alertas e dashboards para antecipar problemas.

Avalia a habilidade de identificar, isolar e resolver problemas em desenvolvimento e produção, bem como implementar e manter sistemas de monitoramento. 

---

##### **1 – Fundamenta Competência**
**Descrição:** Usa apenas métodos básicos de debugging e observações manuais; não configura alertas nem dashboards.  

**Example behaviors:**  
- Roda o sistema e observa diretamente o erro no terminal ou display.  
- Copia comandos de depuração de um tutorial sem entender o fluxo completo.  
- Verifica manualmente logs sem filtragem ou análise.  

**Example tasks:**  
- **HW/FW:** Conecta o osciloscópio em um ponto do circuito para confirmar pulso, sem registrar dados.  
- **Software:** Adiciona `console.log`/`print` em trechos de código para descobrir onde falha.  
- **TI:** 
    - Executa `top` ou `htop` manualmente em servidor e anota consumo de CPU em planilha.  
    - Usar `ping` manual em modem 4G para verificar conectividade de um SIM card.  

---

##### **2 – Contribuidor Consistente**
**Descrição:** Utiliza ferramentas de debugging e monitoração básicas; configura logs estruturados, mas sem alertas ou automação.  

**Example behaviors:**  
- Define breakpoints e step-through em IDE para investigar falhas conhecidas.  
- Centraliza logs em arquivo ou serviço simples (e.g., Logstash sem dashboards).  
- Examina métricas básicas periodicamente sem notificações ativas.  

**Example tasks:**  
- **HW/FW:** Usa JTAG para depurar ISR em ESP32, identifica causa de travamento em buffer DMA.  
- **Software:** Configura Winston/Log4j para logs JSON e filtra erros 500 em log file.  
- **TI:** 
    - Instala e configura Prometheus para coletar métricas de uso de CPU e memória, mas sem alertas.  
    - Configurar logs básicos do Snipe-IT para registrar erro de importação de SIM cards.  

---

##### **3 – Desempenho Confiável**
**Descrição:** Encadeia debugging e monitoring em pipelines de CI/CD, automatiza alertas básicos e investiga incidentes em produção de forma autônoma.  

**Example behaviors:**  
- Configura dashboards minimalistas (Grafana) e alerta por e-mail/Telegram em erros de severidade média.  
- Reproduz bugs em ambiente de staging usando snapshots de dados.  
- Documenta causas raízes e publica post-mortems simples.  

**Example tasks:**  
- **HW/FW:** Monta script no CI que executa captura de sinal via analisador lógico em cada build e compara com baseline.  
- **Software:** Implementa APM (New Relic, Datadog) para rastrear latência de endpoints, enviando alertas em SLA violado.  
- **TI:** 
    - Cria playbook Ansible que instala e configura node_exporter em hosts, populando Grafana com painel de latência de rede.  
    - Criar dashboard Grafana que monitora consumo de dados de cada SIM card via API da operadora, com alerta de 80% do limite.  

---

##### **4 – Proativo na Otimização**
**Descrição:** Identifica padrões de falha e pontos de monitoramento críticos, estende automação de alertas, reduz MTTR e orienta colegas.  

**Example behaviors:**  
- Introduz tracing distribuído para rastreamento de requests end-to-end.  
- Cria runbooks de investigação automática e executa drills de incidentes.  
- Revê e refina alerts, evitando falsos positivos e alert fatigue.  

**Example tasks:**  
- **HW/FW:** Desenha e implementa um sistema de registro circular de eventos críticos em memória flash externa, com exportação automatizada via USB para ferramenta de análise pós-campo.  
- **Software:** Implementa OpenTelemetry para rastrear transações entre microserviços, visualizando no Jaeger.  
- **TI:** 
    - Constrói playbook que simula falha de disco e verifica resposta automática de failover, gerando relatório de SLA.  
    - Automatizar coleta diária de métricas de consumo e status de SIM cards (uso, roaming) e gerar alerta via Slack em anomalias.  

---

##### **5 – Inova e Eleva Padrões**
**Descrição:** Define frameworks, ferramentas e processos de debugging e monitoring corporativos; é mentor e referência global na organização.  

**Example behaviors:**  
- Padrões de observabilidade “as code” são criados e evangelizados internamente.  
- Lidera comunidade técnica interna em práticas de SRE e resposta a incidentes.  
- Publica whitepapers e conduz treinamentos sobre monitoramento avançado e debugging de sistemas complexos.  

**Example tasks:**  
- **HW/FW:** Desenvolve framework de telemetria sobre LoRa e satélite, incluindo scripts de ingestão e visualização multi-regional.  
- **Software:** Cria plataforma interna baseada em Grafana Loki e Tempo, unificando logs e traces em um único painel.  
- **TI:** 
    - Projeta e implementa sistema de self-healing em Kubernetes, integrando Prometheus, Alertmanager e scripts de recuperação.  
    - Desenvolver sistema de telemetria centralizado que correlaciona logs de modems satélite e celulares, exibindo estatísticas em dashboard HMI e acionando failover automático.  


#### 1.1.4 Understanding Code  
Compreende rapidamente bases de código ou projetos existentes: navega em repositórios, interpreta fluxos de dados e controla efeitos colaterais antes de propor mudanças ou correções.

Avalia a capacidade de ler, compreender e navegar em bases de código ou projetos existentes antes de propor alterações. 

---

##### **1 – Familiaridade Básica**  
**Descrição:** Reconhece onde o código ou configuração está, mas depende de documentação externa e orientação para entender o fluxo.  

**Example behaviors:**  
- Segue links de comentários e README para localizar funções ou módulos.  
- Precisa que colegas expliquem parte do fluxo de execução.  
- Não consegue traçar dependências sem ajuda.  

**Example tasks:**  
- **HW/FW:** Localiza a inicialização I²C em um projeto ESP32 lendo README e linkando para o arquivo `i2c_driver.c`.  
- **Software:** Usa busca de IDE para encontrar onde um endpoint REST é definido, mas não entende totalmente middleware aplicado.  
- **TI:** 
    - Abre playbook Ansible e identifica tarefa de instalação de pacote, mas não descobre como roles se encaixam sem diagrama.  
    - Localizar playbook Ansible que importa SIM cards, mas não identificar todas as variáveis usadas.  

---

##### **2 – Navegador Competente**  
**Descrição:** Consegue navegar em múltiplos módulos de forma independente, mas ainda demora a conectar todos os pontos do fluxo.  

**Example behaviors:**  
- Explora imports/includes para seguir chamadas de função ou tarefas entre arquivos.  
- Usa breakpoints e logging para entender o comportamento.  
- Documenta descobertas em notas pessoais.  

**Example tasks:**  
- **HW/FW:** Mapeia sequência de inicialização de periféricos (SPI, DMA) navegando nos arquivos `init.c` e `driver_spi.c`.  
- **Software:** Percorre código JavaScript/TypeScript para rastrear fluxo de dados do front-end ao back-end, usando debugger do browser.  
- **TI:** 
    - Analisa playbook Terraform para entender como módulos são referenciados e combinados em um deploy.  
    - Navegar pelos scripts Python de provisão de modems e listar as chamadas à API da operadora.  

---

##### **3 – Compreensão Confiável**  
**Descrição:** Entende rapidamente o propósito e as interdependências do código, identificando pontos de extensão ou refatoração.  

**Example behaviors:**  
- Resume a arquitetura de alto nível e descreve pontos críticos de falha.  
- Identifica rapidamente funções-chave e seus contratos de entrada/saída.  
- Atualiza ou corrige documentação existente com base no entendimento.  

**Example tasks:**  
- **HW/FW:** Documenta o fluxo de dados de aquisição de sensor via I²C e identifica onde inserir tratamento de overflow.  
- **Software:** Gera diagrama UML simplificado para um microserviço, incluindo controllers, serviços e repositórios.  
- **TI:** 
    - Cria diagrama de dependências entre módulos Ansible e roles, destacando pontos de variáveis compartilhadas.  
    - Documentar fluxo completo de integração entre Snipe-IT, ERP e API de SIM cards, incluindo diagrama de chamadas REST.  

---

##### **4 – Insight em Arquitetura**  
**Descrição:** Analisa e refatora partes do sistema com conhecimento profundo, antecipando impactos e sugerindo melhorias.  

**Example behaviors:**  
- Propõe e justifica refatorações para desacoplar módulos complexos.  
- Antecipates efeitos colaterais de mudanças em baixo nível no sistema como um todo.  
- Mentora outros para entenderem o design existente.  

**Example tasks:**  
- **HW/FW:** Refatora driver DMA para um modelo baseado em callbacks, reduzindo acoplamento e facilitando testes.  
- **Software:** Extrai lógica de negócio de um controller monolítico, movendo para serviço dedicado e criando testes correspondentes.  
- **TI:** 
    - Reestrutura repositório de IaC, separando módulos de rede, compute e storage em workspaces distintos.  
    - Refatorar script de gestão de SIM cards em funções modulares e criar README detalhado de uso e dependências.  

---

##### **5 – Maestro de Código**  
**Descrição:** Atua como referência, documentando padrões de navegação e auxiliando o time a entender e evoluir sistemas complexos sem documentação prévia.  

**Example behaviors:**  
- Cria e mantém “caminhos de leitura” (guided tours) do código nos repositórios.  
- Lidera sessões de code walkthrough para esclarecer arquitetura e processos.  
- Publica guias de boas práticas para documentação de projetos legados.  

**Example tasks:**  
- **HW/FW:** Desenvolve ferramenta interna que gera documentação interativa (plantuml) a partir de comentários no código C/C++.  
- **Software:** Implementa e mantém portal de documentação automática (e.g., Swagger + diagramas UML) para todos os microserviços.  
- **TI:** 
    - Constrói site interno “mapa do repositório” para playbooks e módulos Ansible, com links navegáveis e exemplos de uso.  
    - Desenvolver ferramenta interna que gera automaticamente documentação interativa do fluxo de integração de SIM cards a partir do código-fonte.  


#### 1.1.5 System Design  
Projeta soluções de alto nível cobrindo arquitetura de software (APIs, microsserviços), firmware/hardware (RTOS, power-management, SI/PI) ou infraestrutura (topologias de rede, redundância, escalabilidade).

Avalia a capacidade de projetar soluções de alto nível, definindo estruturas modulares, interfaces e fluxos de dados adequados para escala e evolução.

---

##### **1 – Design Básico**  
**Descrição:** Segue modelos ou padrões existentes com mínima customização; define apenas o essencial.  

**Example behaviors:**  
- Replica um diagrama de referência sem questionar trade-offs.  
- Define interfaces sem especificar requisitos de performance ou falha.  
- Aceita configurações padrão sem avaliar implicações.  

**Example tasks:**  
- **HW/FW:** Copia esquema de referência de placa Arduino, sem ajustar roteamento ou decoupling.  
- **Software:** Cria estrutura de projeto Express/Maven usando o gerador padrão, sem modularizar pacotes.  
- **TI:** 
    - Adota topologia de rede simples (flat network) baseada em guia de instalação sem personalização de VLANs.  
    - Adotar topologia existente para armazenar dados de SIM cards em banco local, sem questionar performance.  

---

##### **2 – Design Consistente**  
**Descrição:** Conecta subsistemas de forma coerente, mas deixa lacunas em escalabilidade, tolerância a falhas ou performance.  

**Example behaviors:**  
- Define módulos com responsabilidades claras, mas não documenta limites de carga.  
- Seleciona tecnologias adequadas, mas subestima custos operacionais.  
- Entrega diagramas de sequência sem detalhes de retentativa ou timeout.  

**Example tasks:**  
- **HW/FW:** Desenha bloco de alimentação e lógica digital no esquemático, mas não calcula tolerâncias de EMI.  
- **Software:** Esboça diagrama de microserviços com APIs REST, mas não especifica SLA ou caching.  
- **TI:** 
    - Planeja rede com sub-redes separadas para DMZ e LAN, porém sem plano de failover para roteadores.  
    - Propor tabela de banco de dados para estoque de SIM cards, mas sem considerar crescimento anual.  

---

##### **3 – Design Robusto**  
**Descrição:** Projeta arquiteturas completas, prevendo requisitos de performance, falhas e escala; documenta trade-offs.  

**Example behaviors:**  
- Realiza análise de carga e define limites de rate-limiting.  
- Inclui planos de fallback e monitoração no design.  
- Produz documentação clara com diagramas C4 ou UML.  

**Example tasks:**  
- **HW/FW:** Arquitetura de placa com separação de domínio analógico/digital, roteamento de alta-velocidade e ESD protection.  
- **Software:** Desenha arquitetura de eventos com Kafka ou RabbitMQ, definindo particionamento e garantias de entrega.  
- **TI:** 
    - Elabora desenho de infraestrutura em múltiplas AZs, com load balancers, VPNs redundantes e health checks.  
    - Desenhar arquitetura que integra Snipe-IT, ERP e dashboard Grafana para gestão de SIM cards com failover manual.  

---

##### **4 – Proativo na Evolução**  
**Descrição:** Identifica pontos críticos de evolução e define padrões para modularidade, extensibilidade e segurança.  

**Example behaviors:**  
- Propõe padrões de API (versioning, HATEOAS) ou de firmware (HAL, drivers plugáveis).  
- Antecipates necessidades de integração futura e facilita onboarding de novos módulos.  
- Lidera revisões de arquitetura para garantir compliance e melhores práticas.  

**Example tasks:**  
- **HW/FW:** Define plataforma de hardware genérica com footprint configurável para múltiplos sensores e atuadores.  
- **Software:** Cria blueprint de arquitetura serverless para microserviços, incluindo pipelines CI/CD e IaC.  
- **TI:** 
    - Desenvolve framework Terraform/Ansible com módulos reutilizáveis para workloads variadas, incluindo políticas de segurança.  
    - Projetar solução de alta disponibilidade para API de gestão de SIM cards, com balanceador e replicação de dados.  

---

##### **5 – Visionário de Arquitetura**  
**Descrição:** Cria frameworks e diretrizes de arquitetura corporativa, alinhando tecnologia a objetivos de negócio e mercado.  

**Example behaviors:**  
- Define e evangeliza referência arquitetural (TOGAF, DDD) em toda a organização.  
- Conduz workshops interdisciplinares para alinhar hardware, software e operações.  
- Publica guias de governança e revisa roadmaps de produto/infraestrutura em nível executivo.  

**Example tasks:**  
- **HW/FW:** Lança plataforma de hardware modulável, com specification-driven design e pipelines de validação automatizada.  
- **Software:** Publica e mantém repositório de “architectural patterns” compartilhados (monolito modular, event-driven, CQRS).  
- **TI:** 
    - Implementa e promove malha de serviços (service mesh) com políticas de segurança e observabilidade unificadas.  
    - Definir plataforma corporativa de conectividade M2M, integrando SIM cards, modems satélite e celular, com orquestração de failover e billing consolidado.  


---

### 1.2 Delivery

#### 1.2.1 Project Management  
Planeja tarefas, define marcos e gerencia riscos. Utiliza metodologias (Ágil, Waterfall), mantém backlog atualizado, faz estimativas realistas e acompanha progresso até a entrega.

Avalia a capacidade de planejar, coordenar e executar projetos, garantindo alcance de marcos, gestão de riscos e comunicação clara.

---

##### **1 – Planejamento Básico**  
**Descrição:** Segue cronogramas predefinidos com pouca adaptação; não antecipa riscos ou dependências.  

**Example behaviors:**  
- Atualiza cronograma apenas reproduzindo datas passadas.  
- Expõe progresso somente quando solicitado.  
- Não documenta riscos nem planos de contingência.  

**Example tasks:**  
- **HW/FW:** Preenche planilha com datas de entrega de PCBs conforme cronograma inicial, sem revisar prazos de fabricação.  
- **Software:** Cria/Atualiza um board no Jira com tarefas e deadlines copiados de um template, sem estimar esforço real.  
- **TI:** 
    - Agenda manutenção de servidores em horário fixo, sem validar janela de downtime com stakeholders.  
    - Anotar prazos de entrega de SIM cards em planilha conforme instruções.  

---

##### **2 – Execução Confiável**  
**Descrição:** Estima prazos com base em experiência; revisa plano quando surgem imprevistos, mas requer supervisão.  

**Example behaviors:**  
- Reavalia estimativas após pequenos atrasos.  
- Comunica bloqueadores em reuniões diárias.  
- Registra riscos em documento, mas não os prioriza.  

**Example tasks:**  
- **HW/FW:** Ajusta datas de projeto de firmware após atraso na entrega de componentes, comunicando equipe e fornecedor.  
- **Software:** Reestima tarefas de sprint em planning ao detectar dependências ocultas em bibliotecas externas.  
- **TI:** 
    - Atualiza calendário de migração de rede quando descobre conflito com outro time, mas sem propor novo plano de backup.  
    - Criar board no Jira para rastrear pedidos de novos SIM cards, mas sem estimar tempo de aprovação.  

---

##### **3 – Gerenciamento Proativo**  
**Descrição:** Identifica riscos e dependências antecipadamente; mantém stakeholders informados e entrega dentro do prazo.  

**Example behaviors:**  
- Realiza reuniões de risco e mantém risk register atualizado.  
- Priorização clara dos entregáveis com base em valor de negócio.  
- Garante que toda a equipe tenha visibilidade de marcos e blockers.  

**Example tasks:**  
- **HW/FW:** Coordena fornecedores e equipe de montagem, mapeando lead times e mitigando risco de atraso de PCBs.  
- **Software:** Define milestones e checkpoints no GitLab, acionando demonstrações regulares para product owner.  
- **TI:** 
    - Cria runbook para migração de datacenter, incluindo fallback plan e comunicação prévia a todos os times.  
    - Planejar rollout de sistema de gestão de SIM cards, definindo milestones de inventário, integração e testes.  

---

##### **4 – Líder de Projetos Complexos**  
**Descrição:** Conduz projetos multifuncionais complexos, antecipando impactos e garantindo sinergia entre áreas.  

**Example behaviors:**  
- Facilita alinhamento entre hardware, firmware, software e operações.  
- Gerencia múltiplos streams de trabalho com OKRs claros.  
- Usa métricas de performance de projeto (burn-down, CPI, SPI) para ajustes dinâmicos.  

**Example tasks:**  
- **HW/FW:** Lidera desenvolvimento de plataforma IoT de ponta a ponta, integrando design de PCB, firmware e testes de campo em paralelo.  
- **Software:** Orquestra desenvolvimento de suíte de microserviços, coordenando dependências e versionamento de APIs.  
- **TI:** 
    - Gerencia rollout global de nova infraestrutura em nuvem, sincronizando equipes regionais e operações 24×7.  
    - Coordenar simultaneamente a implantação de playbooks Ansible, scripts Python e dashboards Grafana para SIM cards, monitorando riscos.  

---

##### **5 – Executivo de Programas**  
**Descrição:** Define a estratégia de portfólio de projetos; estabelece processos corporativos e mentora gerentes de projeto.  

**Example behaviors:**  
- Cria e evangeliza metodologia de entrega (ex.: SAFE, Prince2 adaptado).  
- Monitora KPIs de portfólio (ROI, NPV, RONA) para decisões de continuidade ou pivot.  
- Mentora colegas em gestão de programas e governança.  

**Example tasks:**  
- **HW/FW:** Implanta governance board para pipeline de hardware, padronizando processos de aprovação e QA.  
- **Software:** Define framework de gestão de produtos e programas, alinhado ao roadmap estratégico da empresa.  
- **TI:** 
    - Estabelece PMO para iniciativas de infraestrutura, consolidando relatórios e benchmarks de desempenho.  
    - Liderar programa de transformação de gestão de conectividade, alinhando cronograma, orçamento e metas de redução de custos globais.  

#### 1.2.2 Prioritisation & Dependencies  
Avalia impacto de requisitos e dependências técnicas/negócio. Organiza backlog de forma que itens críticos sejam endereçados primeiro e gargalos sejam eliminados.

Avalia a habilidade de organizar o backlog e gerenciar dependências técnicas e de negócio para maximizar valor e minimizar bloqueios. 

---

##### **1 – Segue Ordens**  
**Descrição:** Executa tarefas na ordem que chegam, sem avaliar prioridade ou dependências.  

**Example behaviors:**  
- Pega a próxima tarefa sem verificar se outras atividades bloqueiam seu progresso.  
- Não considera impacto de atrasos em componentes externos ou APIs.  
- Nunca revisa ou ajusta o backlog.  

**Example tasks:**  
- **HW/FW:** Inicia desenvolvimento de driver antes de receber o esquemático final da placa.  
- **Software:** Começa a codificar um novo endpoint sem checar se o banco de dados está migrado.  
- **TI:** 
    - Aplica patch em servidor sem verificar se há dependências de serviço de rede pendentes.  
    - Atender primeiros pedidos de SIM cards sem verificar dependências de estoque ou faturamento.  

---

##### **2 – Contribuidor Consciente**  
**Descrição:** Reconhece algumas dependências, mas requer confirmação para priorizar adequadamente.  

**Example behaviors:**  
- Pergunta ao Product Owner se a tarefa X deve preceder a Y, mas não investiga por conta própria.  
- Atualiza o backlog quando orientado, mas não faz análise de impacto detalhada.  
- Resolve bloqueios conhecidos, mas perde novas dependências que surgem.  

**Example tasks:**  
- **HW/FW:** Aguarda entrega de componentes antes de começar layout, mas esquece que firmware precisa de biblioteca compatível.  
- **Software:** Solicita configuração de feature flag antes de desenvolver, mas ignora dependências de serviço externo.  
- **TI:** 
    - Verifica ordem de execução de playbooks, mas não ajusta a sequência quando um role falha.  
    - Perguntar ao gestor qual pedido de SIM card atender antes, mas sem mapear dependências.  

---

##### **3 – Gerenciamento Confiável**  
**Descrição:** Mapeia e prioriza dependências de forma autônoma, garantindo que entregas fluam sem bloqueios.  

**Example behaviors:**  
- Cria diagrama ou lista de dependências antes de estimar esforço.  
- Reprioriza backlog quando uma dependência crítica atrasa.  
- Comunica stakeholders sobre mudanças de prioridade.  

**Example tasks:**  
- **HW/FW:** Documenta e sequencia tarefas de design de PCB e desenvolvimento de firmware, ajustando cronograma conforme lead times.  
- **Software:** Define ordering de microserviços e migrations, criando tickets que refletem dependências de banco de dados.  
- **TI:** 
    - Planeja rollout de patches respeitando dependências de rede, armazenamento e serviços adjacentes.  
    - Mapear dependências entre modems em uso, estoque de SIM cards e faturas pendentes, sequenciando pedidos de reabastecimento.  

---

##### **4 – Proativo na Otimização**  
**Descrição:** Identifica dependências ocultas, reordenando iniciativas para reduzir riscos e maximizar throughput.  

**Example behaviors:**  
- Antecipates cross-team blockers e ajeita prioridades antes que afetem sprint.  
- Automatiza verificação de dependências (scripts, ferramentas) para detectar conflitos.  
- Trabalha com PM e Tech Leads para ajustar roadmap com base em dependências técnicas.  

**Example tasks:**  
- **HW/FW:** Cria script que valida versão de bootloader e hardware antes de cada build de firmware.  
- **Software:** Implementa ferramenta de análise de dependências de pacotes (npm, pip) e bloqueia versões inseguras.  
- **TI:** 
    - Desenvolve dashboard de dependências de rede e servidores, exibindo nós críticos e sugerindo ordem de manutenção.  
    - Automatizar verificação de compatibilidade de plano de SIM card e versão de firmware do modem antes de aprovar ordens.  

---

##### **5 – Estrategista de Priorização**  
**Descrição:** Define frameworks e políticas de priorização para toda a organização, alinhando dependências a objetivos de negócio.  

**Example behaviors:**  
- Constrói matriz de valor vs. esforço que embasa decisões de roadmap.  
- Treina equipes para identificar e documentar dependências de forma sistemática.  
- Ajusta processos de governança para incorporar análise de dependências em todas as fases.  

**Example tasks:**  
- **HW/FW:** Padrão de pipeline onde cada PR de firmware valida automaticamente se os arquivos de layout de PCB correspondem à versão esperada.  
- **Software:** Desenvolve e dissemina guideline de versionamento semântico e monorepo tooling, prevenindo conflitos de dependência.  
- **TI:** 
    - Define política corporativa de change management que exige matriz de dependências antes de qualquer deploy em produção.  
    - Definir política corporativa de priorização de pedidos de SIM cards baseada em métricas de uso, SLA e custo-benefício.  

#### 1.2.3 Adaptability & Change  
Reage bem a mudanças de escopo, requisitos ambíguos ou novas prioridades. Replaneja rapidamente, incorpora feedback e mantém a equipe alinhada em ambientes de incerteza.

Avalia a capacidade de reagir a mudanças de requisitos, escopo e ambiente, mantendo produtividade e alinhamento. 

---

##### **1 – Resistente a Mudanças**  
**Descrição:** Demonstra dificuldade em aceitar novas diretrizes; precisa de muita orientação para ajustar prioridades.  

**Example behaviors:**  
- Insiste em seguir o plano original mesmo diante de evidências de mudança.  
- Solicita instruções detalhadas para alterar scripts ou código.  
- Evita tecnologias ou processos novos.  

**Example tasks:**  
- **HW/FW:** Mantém firmware antigo sem adaptar drivers para novo sensor entregue.  
- **Software:** Recusa-se a migrar de framework legado, atrasando integrações.  
- **TI:** 
    - Continua usando playbooks antigos após atualização de infraestrutura, gerando falhas.  
    - Relutar em adotar novo layout de campo de formulário de pedido de SIM card.  

---

##### **2 – Contribuidor Flexível**  
**Descrição:** Ajusta-se a mudanças conhecidas, mas requer confirmação e direção para lidar com imprevistos.  

**Example behaviors:**  
- Replaneja tarefas quando comandado, mas sem antecipar impactos colaterais.  
- Adota novas ferramentas apenas após tutorial ou exemplo pronto.  
- Precisa de revisão ao alterar processos.  

**Example tasks:**  
- **HW/FW:** Atualiza build system para novo compilador sob supervisão, mas esquece flags de otimização.  
- **Software:** Refatora um endpoint para nova versão de API externa seguindo guia de migração.  
- **TI:** 
    - Adapta playbook Ansible para novo container runtime, mas ignora configuração de network namespace.  
    - Ajustar planilha de inventário conforme novo requisito, mas sem revisar consistência dos dados.  

---

##### **3 – Adaptável Confiável**  
**Descrição:** Lida bem com escopo dinâmico; reorganiza prioridades e aprende novas ferramentas conforme necessário.  

**Example behaviors:**  
- Avalia impacto de mudanças e comunica plano de ação rapidamente.  
- Testa novas bibliotecas ou processos em sandbox antes de aplicar em produção.  
- Mantém equipe informada sobre ajustes de rota.  

**Example tasks:**  
- **HW/FW:** Migra firmware de Arduino para ESP32, validando funcionalidades e ajustando configurações de pinout.  
- **Software:** Converte projeto de build Make para CMake, garantindo compatibilidade de múltiplas plataformas.  
- **TI:** 
    - Atualiza playbooks para suportar Kubernetes 1.24 e testa rollback automático em ambientes de staging.  
    - Migrar playbook Ansible de importação de SIM cards para nova versão de API de operadora sem interromper produção.  

---

##### **4 – Proativo na Transformação**  
**Descrição:** Antecipates mudanças de tecnologia e processos, propondo e liderando migrações ou evoluções antes de se tornarem urgentes.  

**Example behaviors:**  
- Monitora tendências e recomenda adoção de novas arquiteturas ou padrões.  
- Conduz PoCs para avaliar viabilidade de ferramentas emergentes.  
- Treina colegas nos novos métodos de trabalho.  

**Example tasks:**  
- **HW/FW:** Projeta e implementa PoC de firmware em Zephyr RTOS para substituir FreeRTOS, apresentando resultados de performance.  
- **Software:** Conduz migração de monolito para arquitetura de micro front-ends com module federation.  
- **TI:** 
    - Planeja e executa rollout de GitOps para gerenciar infraestrutura em múltiplos clusters Kubernetes.  
    - Conduzir PoC de integração com novo fornecedor de SIM cards em paralelo ao sistema existente, validando em staging.  

---

##### **5 – Campeão da Mudança**  
**Descrição:** Define frameworks de gestão de mudanças e lidera iniciativas de transformação cultural e tecnológica em toda a organização.  

**Example behaviors:**  
- Estabelece processos de change management integrados ao ciclo de vida de desenvolvimento.  
- Evangeliza cultura de experimentação e iteratividade.  
- Mentora líderes para gerir mudanças em larga escala.  

**Example tasks:**  
- **HW/FW:** Cria governance board para validação de novas plataformas hardware, definindo critérios de adoção e planos de capacitação.  
- **Software:** Implementa e documenta processo de Feature Toggles e Canary Releases em todos os serviços críticos.  
- **TI:** 
    - Desenvolve e treina equipes no framework ITIL 4 adaptado à realidade DevOps da empresa, coordenando mudanças em datacenters e nuvem.  
    - Liderar mudança de plataforma de gestão de conectividade (SaaS para on-premise), gerenciando stakeholders e mitigando riscos.  

#### 1.2.4 Reliability & Accountability  
Entrega com consistência, cumpre prazos e assume responsabilidade pelos resultados. Comunica riscos antecipadamente e implementa planos de contingência quando necessário.

Avalia a consistência e responsabilidade na entrega de resultados, comunicação de riscos e cumprimento de compromissos.

---

##### **1 – Cumprimento Básico**  
**Descrição:** Entrega apenas o que foi solicitado, frequentemente atrasado, e raramente assume responsabilidade por falhas.  

**Example behaviors:**  
- Atrasos não são comunicados até o prazo já ter expirado.  
- Rejeita a ideia de assumir correções pós-entrega.  
- Evita reportar problemas, esperando que outros percebam.  

**Example tasks:**  
- **HW/FW:** Entrega firmware de leitura de sensor fora do prazo acordado sem aviso prévio.  
- **Software:** Finaliza feature no repositório sem executar testes finais e ignora falhas de build.  
- **TI:** 
    - Executa manutenção de servidor sem comunicar janela de downtime e falha em restaurar serviço rapidamente.  
    - Executar inventário de SIM cards uma vez por mês manualmente, sem checar discrepâncias.  

---

##### **2 – Contribuidor Responsável**  
**Descrição:** Cumpre a maior parte das tarefas dentro do prazo, mas requer lembretes; assume responsabilidade apenas quando solicitado.  

**Example behaviors:**  
- Notifica atrasos somente após ser questionado.  
- Assume correções quando apontado, mas não se antecipa.  
- Documenta incidentes apenas para fechar tickets.  

**Example tasks:**  
- **HW/FW:** Ajusta cronograma de testes de bancada após ser notificado de conflito de agenda.  
- **Software:** Corrige bug em produção depois de alerta de monitoramento, mas não implementa rollback automático.  
- **TI:** 
    - Restaura host com backup após incidente, mas não analisa causa raiz nem previne recorrências.  
    - Notificar divergências de estoque apenas após auditoria anual.  

---

##### **3 – Confiável e Responsável**  
**Descrição:** Entrega consistentemente dentro do prazo, comunica riscos e assume a resolução de problemas proativamente.  

**Example behaviors:**  
- Informa stakeholders sobre possíveis atrasos com antecedência.  
- Monitora health checks e reage a alertas automaticamente.  
- Documenta causas raízes e compartilha lições aprendidas.  

**Example tasks:**  
- **HW/FW:** Agenda testes de campo com margem para retrabalho e informa equipe quando ocorrem desvios.  
- **Software:** Configura pipeline para reverter automaticamente deploy com falha e envia relatório ao time.  
- **TI:** 
    - Recebe alerta de disco cheio, adiciona espaço e notifica o time antes que impacte serviços.  
    - Implementar script de auditoria semanal que compara estoque físico x sistema e gera tickets em Jira.  

---

##### **4 – Proativo na Confiabilidade**  
**Descrição:** Implementa melhorias de processo e automações que elevam o nível de confiabilidade além do esperado.  

**Example behaviors:**  
- Identifica potenciais pontos de falha e propõe alertas ou redundâncias.  
- Define SLAs e SLOs claros para componentes críticos.  
- Orienta colegas a seguir padrões de confiabilidade.  

**Example tasks:**  
- **HW/FW:** Automatiza testes de regressão de firmware e valida bootloader em cada commit, reduzindo falhas em campo.  
- **Software:** Implementa circuit breaker e retry com backoff em chamadas externas, monitorando métricas de sucesso.  
- **TI:** 
    - Cria processo automatizado de failover de banco de dados e testa a recuperação sem intervenção manual.  
    - Automatizar reconciliação diária de consumo de dados e inventário de SIM cards, abrindo chamados junto ao fornecedor em caso de anomalias.  

---

##### **5 – Defensor da Excelência**  
**Descrição:** Estabelece políticas de confiabilidade corporativa e é referência em accountability, elevando padrões organizacionais.  

**Example behaviors:**  
- Cria e evangeliza cultura de blameless post-mortems e melhoria contínua.  
- Define métricas de confiabilidade corporativas (e.g., uptime, MTTR) e conduz acompanhamento executivo.  
- Mentora outras equipes na implementação de práticas de responsabilidade.  

**Example tasks:**  
- **HW/FW:** Lança programa de certificação interna de qualidade de firmware, incluindo auditorias periódicas.  
- **Software:** Publica guideline de SRE com regras de escalabilidade, monitoramento e runbooks de incidentes.  
- **TI:** 
    - Estabelece processo de change review board, garantindo que todas as mudanças passem por análise de risco e rollback plan.  
    - Definir e implantar política corporativa de auditoria contínua de ativos móveis, com dashboards de compliance e relatórios executivos.  

---

## 2. Soft Skills

### 2.1 Collaboration

#### 2.1.1 Communication & Sharing  
Comunica ideias de forma clara (oral, escrita, apresentações) e compartilha conhecimento: documenta processos, conduz workshops e faz pair-programming.

Avalia clareza, eficácia e frequência com que o profissional comunica informações e compartilha conhecimento com a equipe.

---

##### **1 – Comunicação Pontual e Básica**  
**Descrição:** Comunica apenas o mínimo necessário; raramente documenta ou compartilha aprendizados.  

**Example behaviors:**  
- Responde mensagens apenas quando diretamente solicitado.  
- Usa linguagem técnica sem adaptar ao público.  
- Não registra decisões ou passos importantes.  

**Example tasks:**  
- **HW/FW:** Envia e-mail informando “sensor calibrado” sem detalhar parâmetros usados.  
- **Software:** Adiciona um comentário genérico no código (“TODO: handle error”) sem contexto.  
- **TI:** 
    -Executa alteração em servidor e não atualiza o ticket com detalhes da mudança.  
    - Informar via e-mail genérico “Novo SIM adicionado” ao time.  

---

##### **2 – Comunicação Consistente**  
**Descrição:** Fornece atualizações de status regulares, mas faltam detalhes ou formatação clara.  

**Example behaviors:**  
- Participa de reuniões diárias, mas não documenta decisões.  
- Compartilha snippets de código ou diagramas sem explicação completa.  
- Envia links sem sumário do conteúdo.  

**Example tasks:**  
- **HW/FW:** Publica no canal Teams “firmware build concluído” anexando binário, mas sem log de testes.  
- **Software:** Comenta PR com “funciona aqui” sem detalhar o cenário testado.  
- **TI:** 
    -Atualiza ticket dizendo “servidor rebootado”, mas sem registrar motivo ou resultado de health-check.  
    - Publicar no Confluence procedimento de pedido de SIM cards sem exemplos visuais.  

---

##### **3 – Comunicação Clara e Colaborativa**  
**Descrição:** Comunica-se de forma clara, documenta decisões e compartilha conhecimento relevante.  

**Example behaviors:**  
- Escreve resumos de reunião com ações e responsáveis.  
- Produz README ou wiki com instruções de uso.  
- Faz pair-programming e revisões de código abertos.  

**Example tasks:**  
- **HW/FW:** Documenta o fluxo de calibração I²C, com fotos de sinal e parâmetros.  
- **Software:** Cria guia de estilo Markdown para o repositório, incluindo exemplos de chamadas de API.  
- **TI:** 
    -Publica playbook Ansible com comentários explicando cada etapa do provisionamento.  
    - Criar guia ilustrado no Confluence com fluxo de aprovação, screenshots e link para formulário de requisição.  

---

##### **4 – Facilitador de Conhecimento**  
**Descrição:** Proativamente compartilha insights, cria templates e conduz treinamentos internos.  

**Example behaviors:**  
- Organiza workshop “Como usar o analisador lógico” para colegas de hardware.  
- Escreve blog interno explicando pattern arquitetural adotado.  
- Ajuda novos membros a se situarem no código e no processo.  

**Example tasks:**  
- **HW/FW:** Desenvolve template de relatório de testes HIL e treina a equipe em como preenchê-lo.  
- **Software:** Cria gerador de documentação automática (Swagger) e treina devs no uso.  
- **TI:** 
    -Constrói repositório de scripts reutilizáveis para manutenção e faz live-coding para o time.  
    - Conduzir webinar interno sobre o processo de gestão de SIM cards, gravando vídeo e Q&A.  

---

##### **5 – Influenciador de Comunicação**  
**Descrição:** Define políticas e padrões de comunicação corporativa; inspira a cultura de compartilhamento e transparência.  

**Example behaviors:**  
- Padrões de documentação “as code” são implementados em todos os projetos.  
- Lidera série de Tech Talks ou “lunch & learn” regulares.  
- Mentora outros na arte da comunicação técnica.  

**Example tasks:**  
- **HW/FW:** Publica guia de “best practices” para documentação de hardware e firmware, integrado ao pipeline CI para validar templates.  
- **Software:** Implanta portal interno de conhecimento com auto-deploy de docs e versionamento.  
- **TI:** 
    -Estabelece política de “Docs as Code” para playbooks e scripts, integrando revisão por pares antes de qualquer merge.  
    - Desenvolver portal self-service com vídeos, FAQs e chatbot para solicitação e dúvidas sobre SIM cards e infraestrutura.  

#### 2.1.2 Teamwork & Relationships  
Constrói confiança e boas relações no time: colabora em tarefas conjuntas, apoia colegas e mantém um ambiente de trabalho respeitoso e colaborativo.

Avalia a capacidade de colaborar efetivamente, construir confiança e manter relacionamentos saudáveis dentro da equipe e com stakeholders.

---

##### **1 – Participação Mínima**  
**Descrição:** Interage apenas quando solicitado; mantém fronteiras claras, porém sem engajamento ativo.  

**Example behaviors:**  
- Responde a convites de reunião mas não contribui com ideias.  
- Evita discussões de grupo e trabalha isoladamente.  
- Não procura entender ou apoiar desafios dos colegas.  

**Example tasks:**  
- **HW/FW:** Completa sua parte de design de PCB, mas não participa da revisão de esquemáticos dos colegas.  
- **Software:** Abre PR apenas quando concluído, sem comentar ou revisar PRs dos demais.  
- **TI:** 
    - Executa ticket de suporte individualmente, sem oferecer ajuda ou transferência de conhecimento ao próximo turno.  
    - Responder isoladamente tickets de SIM cards sem envolver outras áreas.  

---

##### **2 – Colaboração Ocasional**  
**Descrição:** Contribui de forma pontual em tarefas de equipe, mas não assume responsabilidades de facilitador.  

**Example behaviors:**  
- Oferece ajuda quando diretamente solicitado.  
- Compartilha recursos ou links úteis, mas não coordena esforços.  
- Participa de discussões, mas sem assumir papéis de liderança.  

**Example tasks:**  
- **HW/FW:** Ajuda colega a configurar ferramenta de depuração quando perguntado, mas não documenta o processo.  
- **Software:** Comenta em um PR de outro desenvolvedor, apontando um bug simples, mas não propõe solução.  
- **TI:** 
    - Dá suporte em reunião de shift handover, mas não identifica melhorias no processo de passagem de bastão.  
    - Ajudar colega em chamado de modem satélite quando perguntado.  

---

##### **3 – Colaborador Confiável**  
**Descrição:** Engaja-se proativamente em atividades de equipe, divide responsabilidades e fortalece a confiança mútua.  

**Example behaviors:**  
- Oferece revisão de código/esquemático voluntariamente e cumpre prazos combinados.  
- Solicita feedback sobre seu trabalho e implementa as sugestões.  
- Auxilia novos membros a se integrarem ao time.  

**Example tasks:**  
- **HW/FW:** Coordena sessões de debugging em dupla para resolver issue de comunicação I²C em bancada.  
- **Software:** Atua como revisor principal em pull requests de colegas, garantindo qualidade e consistência no código.  
- **TI:** 
    - Documenta e treina equipe de plantão em novos procedimentos de recovery após incidente de rede.  
    - Organizar reunião semanal com compras, financeiro e suporte de campo para alinhamento de estoque e consumos.  

---

##### **4 – Facilitador de Equipe**  
**Descrição:** Promove a colaboração contínua, resolve conflitos e conecta pessoas e áreas para entregar resultados integrados.  

**Example behaviors:**  
- Media discussões técnicas em reuniões e garante voz para todos os participantes.  
- Identifica e resolve impedimentos interdependentes de forma rápida.  
- Fomenta um ambiente de confiança e inclusão.  

**Example tasks:**  
- **HW/FW:** Organiza e modera workshop de integração hardware-firmware para alinhar especificações de interface.  
- **Software:** Conduz daily stand-ups e retrospectives, introduzindo práticas que aumentam a produtividade do squad.  
- **TI:** 
    - Facilita reunião cross-funcional entre TI, segurança e desenvolvimento para planejar rollout de novas políticas.  
    - Facilitar grupo de trabalho interdepartamental para otimizar fluxos de ativação e faturamento de SIM cards.  

---

##### **5 – Construtor de Comunidade**  
**Descrição:** Cria e mantém redes colaborativas além do próprio time, influenciando positivamente a cultura organizacional.  

**Example behaviors:**  
- Inicia programas de mentoria cruzada entre áreas (ex.: pairing de Software e TI).  
- Representa o time em comitês ou grupos de afinidade, trazendo melhorias para toda a empresa.  
- Inspira outros a colaborarem, criando grupos de prática ou comunidades internas.  

**Example tasks:**  
- **HW/FW:** Lança comunidade técnica interna de IoT, organizando meetups mensais com temas de hardware e firmware.  
- **Software:** Cria e mantém hackathon semestral de inovação de software, integrando times de frontend, backend e DevOps.  
- **TI:** 
    - Estabelece canal interno de “Office Hours” de TI, onde membros de qualquer time podem buscar consultoria e compartilhar soluções.  
    - Criar comunidade interna de “Connectivity Champions” que reúne representantes de todas as áreas para compartilhar práticas e inovações.  

---

### 2.2 Feedback

#### 2.2.1 Feedback Delivery  
Oferece críticas construtivas de maneira respeitosa e orientada a soluções. Sabe apontar pontos de melhoria sem desmotivar, focando em comportamentos e resultados.

Avalia a habilidade de fornecer feedback construtivo, claro e oportuno, com foco em melhoria contínua.

---

##### **1 – Feedback Esparso e Vago**  
**Descrição:** Raramente fornece feedback; quando o faz, é genérico e pouco útil.  

**Example behaviors:**  
- “Está bom” ou “Precisa melhorar” sem detalhar o que ou como.  
- Evita dar retorno em PRs ou design reviews.  
- Foca em falhas pessoais em vez de comportamentos ou resultados.  

**Example tasks:**  
- **HW/FW:** Comenta em um pull request apenas “Verifique isso” sem indicar o que revisar.  
- **Software:** Responde “Parece ok” em PRs sem sugerir melhorias de código ou testes.  
- **TI:** 
    - Informa “Serviço ok” após revisão de playbook, sem indicar configurações específicas.  
    - “Ok” em revisão de processo de pedido de SIM card, sem sugestões.  

---

##### **2 – Feedback Pontual, mas Superficial**  
**Descrição:** Fornece feedback quando solicitado, mas não aprofunda análise ou sugere soluções.  

**Example behaviors:**  
- Aponta problemas (“bug aqui”), mas não sugere correções.  
- Usa linguagem que pode soar crítica, sem orientar próximo passo.  
- Raramente elogia boas práticas observadas.  

**Example tasks:**  
- **HW/FW:** Comenta “Seu driver I²C falha neste caso” sem explicar como tratar o NACK.  
- **Software:** Indica “Sua função está grande demais” sem sugerir refatoração em módulos.  
- **TI:** 
    - Diz “Este playbook não funciona em RHEL 8” sem listar mudanças necessárias.  
    - Apontar falha de validação de IMEI sem sugerir como resolver.  

---

##### **3 – Feedback Claro e Orientado**  
**Descrição:** Entrega feedback específico, com exemplos e sugestões de melhoria, balanceando pontos positivos.  

**Example behaviors:**  
- Aponta melhorias de forma construtiva.  
- Usa exemplos concretos (“na linha 45, faça X em vez de Y”).  
- Propõe referências ou padrões a serem seguidos.  

**Example tasks:**  
- **HW/FW:** “Ótimo uso de RTOS. Na função de ISR, inclua checagem de overflow no buffer para evitar corromper dados.”  
- **Software:** “O endpoint funciona, mas adicione um teste de integração para o caso de timeouts usando Jest.”  
- **TI:** 
    - “A playbook está eficiente. Inclua verificação de idempotência e reporte de status usando Ansible callbacks.”  
    - Fornecer feedback sobre melhoria de formulário de solicitação, indicando campos obrigatórios e lógica de validação.  

---

##### **4 – Feedback Proativo e Colaborativo**  
**Descrição:** Busca oportunidades para fornecer feedback, conduz revisões em grupo e ajuda colegas a implementar mudanças.  

**Example behaviors:**  
- Inicia reuniões de design review sem ser solicitado.  
- Acompanha a aplicação do feedback, oferecendo ajuda prática.  
- Elogia publicamente melhorias e compartilha aprendizados.  

**Example tasks:**  
- **HW/FW:** Organiza sessão de pair-debug para revisar e melhorar juntos o driver SPI.  
- **Software:** Conduz code review workshop mostrando padrões de arquitetura e refatoração em tempo real.  
- **TI:** 
    - Facilita café-da-manhã de feedback sobre playbooks, compartilhando boas práticas de YML e idempotência.  
    - Conduzir sessão de feedback cross-team após go-live de novo sistema, propondo ajustes em tempo real.  

---

##### **5 – Mentor de Feedback e Cultura de Crescimento**  
**Descrição:** Institucionaliza processos de feedback, treina o time em técnicas de comunicação e cria ambientes seguros para troca contínua.  

**Example behaviors:**  
- Desenvolve guia interno de como dar e receber feedback, promovendo cultura de “growth mindset”.  
- Treina líderes e pares em técnicas de feedback situacional e escalonado.  
- Realiza follow-ups para medir impacto do feedback e ajustar abordagens.  

**Example tasks:**  
- **HW/FW:** Publica e mantém “Playbook de Feedback” para revisões de design e PRs, com templates e exemplos.  
- **Software:** Implementa programa de “Feedback Fridays” integrando retrospectives e sessões individuais de mentoria.  
- **TI:** 
    - Cria workshop “Feedback 360°” para equipes de operações, incluindo role-playing e estudos de caso.  
    - Instituir programa trimestral de feedback de processo de gestão de SIM cards, gerando relatório de melhorias e métricas de satisfação.  

#### 2.2.2 Feedback Receptiveness  
Busca e recebe feedback de forma aberta, sem defensividade. Reflete sobre as sugestões, ajusta seu comportamento e demonstra evolução contínua.

Avalia a abertura para receber, refletir e agir sobre o feedback recebido, demonstrando crescimento contínuo.

---

##### **1 – Fechado a Feedback**  
**Descrição:** Reage defensivamente ou ignora o feedback; sem demonstrar vontade de mudança.  

**Example behaviors:**  
- Desvaloriza feedback (“isso não faz sentido”).  
- Justifica erros em vez de buscar entendimento.  
- Não implementa alterações sugeridas.  

**Example tasks:**  
- **HW/FW:** Recebe comentário sobre falha em ISR e mantém o código inalterado.  
- **Software:** Ignora sugestão de testes adicionais e fecha o PR sem ajustes.  
- **TI:** 
    - Desconsidera comentário sobre melhorias no playbook e reverte a mudança de documentação.  
    - Ignorar comentários sobre melhoria de formulário de requisição.  

---

##### **2 – Receptivo, mas Reativo**  
**Descrição:** Aceita o feedback, porém coloca em prática apenas quando lembrado ou solicitado.  

**Example behaviors:**  
- Agradece pelo feedback, mas demora a implementar.  
- Precisa de lembretes para revisar o próprio trabalho.  
- Executa mudanças de forma mecânica, sem compreender o propósito.  

**Example tasks:**  
- **HW/FW:** Adiciona checagem de overflow após duas solicitações de revisão.  
- **Software:** Inclui teste sugerido em Jest somente após ser cobrado nas reuniões diárias.  
- **TI:** 
    - Atualiza playbook para usar variáveis criptografadas só depois de follow-up do time de segurança.  
    - Implementar sugestão de campo obrigatório apenas após lembrete.  

---

##### **3 – Aplicação Confiável**  
**Descrição:** Recebe e integra feedback de forma autônoma, demonstrando entendimento e melhoria efetiva.  

**Example behaviors:**  
- Reflete sobre o feedback e propõe mudanças adicionais.  
- Compartilha no time como aplicou o feedback e os resultados.  
- Ajusta processos para evitar erros semelhantes no futuro.  

**Example tasks:**  
- **HW/FW:** Após revisão, refatora driver I²C e documenta como o tratamento de NACK melhorou a confiabilidade.  
- **Software:** Implementa sugestão de cobertura de testes e registra no changelog melhorias de qualidade.  
- **TI:** 
    - Modifica playbook para incluir verificação de idempotência e explica aos colegas o motivo da mudança.  
    - Revisar e aprimorar script de importação de SIM cards com base em feedback recebido, comunicando mudanças ao time.  

---

##### **4 – Proativo no Desenvolvimento**  
**Descrição:** Busca feedback ativamente, testa diferentes abordagens e compartilha aprendizados, inspirando o time.  

**Example behaviors:**  
- Solicita feedback antes de finalizar grandes mudanças.  
- Realiza experimentos baseados em sugestões e mede resultados.  
- Reconhece e elogia contribuições de quem ofereceu o feedback.  

**Example tasks:**  
- **HW/FW:** Organiza revisão de design pré-código e convida colegas de layout e firmware para sugerir melhorias.  
- **Software:** Envia draft de arquitetura em RFC e ajusta conforme comentários, compartilhando a versão finalizada.  
- **TI:** 
    - Planeja sessão de feedback sobre playbooks, coleta sugestões e integra melhorias antes do próximo ciclo.  
    - Solicitar proativamente feedback de usuários de campo sobre o novo dashboard de consumo e ajustar thresholds.  

---

##### **5 – Champion do Crescimento**  
**Descrição:** Estabelece práticas e ferramentas para feedback contínuo, liderando programas de desenvolvimento pessoal e de equipe.  

**Example behaviors:**  
- Cria canais regulares (por exemplo, “feedback circles”) para troca de feedback estruturado.  
- Mentora colegas em como receber e utilizar feedback para progresso de carreira.  
- Monitora métricas de melhoria pós-feedback e ajusta processos de acordo.  

**Example tasks:**  
- **HW/FW:** Desenvolve programa de “Code Clinics” onde a equipe revisa e reflete sobre código em grupo, incorporando feedback estruturado.  
- **Software:** Lança ferramenta de peer review anônima e treina a equipe no uso para elevar a qualidade dos PRs.  
- **TI:** 
    - Implant “Feedback Bot” no chat para coletar e categorizar feedback de playbooks e responder com insights semanais.  
    - Conduzir ciclos formativos de feedback em cada sprint de melhoria de infraestrutura, medindo impacto e refinando processos.  

---

### 2.3 Leadership

#### 2.3.1 Strategic Alignment  
Toma decisões técnicas e de produto alinhadas aos objetivos da empresa. Consegue balancear trade-offs de curto e longo prazo, engajando stakeholders nas prioridades corretas.

Avalia a capacidade de tomar decisões técnicas e de produto alinhadas aos objetivos estratégicos da empresa e de engajar stakeholders nesse processo.

---

##### **1 – Visão Tática**  
**Descrição:** Foca em entregar atividades imediatas sem considerar contexto ou metas maiores.  

**Example behaviors:**  
- Executa requisitos pontuais do documento de especificação sem questionar prioridades.  
- Não demonstra compreensão dos objetivos de negócio por trás das tarefas.  
- Comunica progresso somente em termos técnicos, sem conectar ao impacto estratégico.  

**Example tasks:**  
- **HW/FW:** Implementa leitura de sensor conforme pedido, sem avaliar se a frequência de amostragem atende ao SLA do produto.  
- **Software:** Desenvolve endpoint conforme spec, sem verificar se atende às metas de latência definidas pelo negócio.  
- **TI:** 
    - Configura servidor para novas aplicações, sem validar requisitos de disponibilidade ou compliance da empresa.  
    - Atender pedidos de SIM cards sem considerar orçamento ou metas de custo.  

---

##### **2 – Conexão Básica**  
**Descrição:** Entende as metas de curto prazo, mas ainda não as traduz em decisões técnicas de forma autônoma.  

**Example behaviors:**  
- Consulta roadmap ou manager antes de tomar decisões que impactam outras áreas.  
- Alinha-se a prioridades definidas, mas não propõe ajustes quando surgem conflitos.  
- Comunica-se com stakeholders somente quando solicitado.  

**Example tasks:**  
- **HW/FW:** Confirma com o product owner a taxa de transmissão antes de otimizar o módulo LoRa.  
- **Software:** Verifica com o PO os SLAs de API antes de ajustar timeouts no cliente HTTP.  
- **TI:** 
    - Consulta equipe de segurança antes de aprovar mudanças de firewall, mas não questiona regras existentes.  
    - Confirmar prioridade de reposição de estoque com gestor antes de agir.  

---

##### **3 – Implementador Estratégico**  
**Descrição:** Toma decisões informadas, equilibrando trade-offs técnicos e metas de negócio; comunica rationale aos stakeholders.  

**Example behaviors:**  
- Avalia custo vs. benefício antes de escolher tecnologias ou arquiteturas.  
- Documenta decisões estratégicas e compartilha as razões com o time.  
- Propõe ajustes de prioridade quando o impacto no negócio é significativo.  

**Example tasks:**  
- **HW/FW:** Seleciona entre uso de modem celular ou LoRa baseado em análise de custo de conectividade vs. cobertura regional.  
- **Software:** Escolhe banco de dados SQL ou NoSQL considerando volume de leitura/escrita e requisitos de consistência.  
- **TI:** 
    - Decide migrar workloads para nuvem pública vs. on-prem considerando SLAs, compliance e custos operacionais.  
    - Analisar custo-benefício de planos de dados e propor troca de plano para reduzir despesas em 10 %.  

---

##### **4 – Alinhador Proativo**  
**Descrição:** Antecipates mudanças na estratégia de produto/negócio e realinha o roadmap técnico antes que os impactos aconteçam.  

**Example behaviors:**  
- Inicia discussões com PM e executivos para ajustar prioridades de arquitetura.  
- Fornece dashboards e indicadores que orientam a tomada de decisão executiva.  
- Facilita workshops de alinhamento entre áreas técnicas e de produto.  

**Example tasks:**  
- **HW/FW:** Propõe plano de atualização OTA para atender nova regulamentação de IoT, coordenando times de hardware, firmware e campo.  
- **Software:** Cria painel de métricas de negócio (ex.: conversão, latência) ligado ao status dos microserviços, influenciando roadmap.  
- **TI:** 
    - Desenvolve relatório de custos de cloud vs. on-prem com projeções de uso, ajudando a definir orçamento anual.  
    - Apresentar à diretoria análise de uso de SIM cards por projeto, recomendando realocação para otimizar orçamento.  

---

##### **5 – Visionário Estratégico**  
**Descrição:** Define e evangeliza a visão técnica que orienta toda a organização, alinhando tecnologia, produto e negócio em nível executivo.  

**Example behaviors:**  
- Co-cria a estratégia tecnológica da empresa com o C-level e traduz em planos de ação claros.  
- Mentora líderes de área para cultivar visão holística e direcionamento estratégico.  
- Representa a empresa em fóruns externos como autoridade técnica.  

**Example tasks:**  
- **HW/FW:** Lança iniciativa de plataforma IoT corporativa, definindo padrões de hardware, firmware e conectividade que suportam a estratégia de expansão global.  
- **Software:** Desenvolve e apresenta o “tech vision deck” para stakeholders, definindo roadmap de novas arquiteturas (event-driven, edge computing) para os próximos 5 anos.  
- **TI:** 
    - Elabora política corporativa de multicloud que equilibra agilidade, segurança e custo, e forma comitê executivo para governança contínua.  
    - Definir estratégia corporativa de “Connectivity as a Service”, alinhando planos de SIM, modems e contratos com metas de crescimento e ROI.  

#### 2.3.2 Mentorship  
Mentora colegas compartilhando experiências, orientando no desenvolvimento de habilidades e apoiando o crescimento individual. Facilita o aprendizado em pares e revisões de trabalho.

Avalia a habilidade de orientar e desenvolver colegas, compartilhando conhecimento e criando oportunidades de crescimento. 

---

##### **1 – Mentoria Pontual**  
**Descrição:** Oferece ajuda apenas quando solicitado, de forma reativa e limitada.  

**Example behaviors:**  
- Responde a dúvidas técnicas básicas no canal, mas não aprofunda explicações.  
- Indica referências genéricas sem guiar o aprendiz em como usar.  
- Não verifica se o colega entendeu ou aplicou o conselho.  

**Example tasks:**  
- **HW/FW:** Explica rapidamente como configurar o osciloscópio para um novo colega, sem demonstrar exemplos práticos.  
- **Software:** Envia link para documentação do framework, sem mostrar código de exemplo ou contexto.  
- **TI:** 
    - Orienta acesso ao inventário de ativos, mas não mostra como criar relatórios a partir dele.  
    - Responder dúvidas sobre SIM cards quando solicitado, mas sem aprofundar.  

---

##### **2 – Mentoria Estruturada**  
**Descrição:** Planeja breves sessões de orientação, mas sem acompanhamento contínuo.  

**Example behaviors:**  
- Agenda 1:1 pontual para revisar código ou configuração.  
- Fornece exemplos simples e sugere exercícios práticos.  
- Registra dicas em documento interno, mas não revisita os resultados.  

**Example tasks:**  
- **HW/FW:** Conduz mini-workshop sobre debouncing em GPIO e compartilha slides ou script de teste.  
- **Software:** Realiza código walkthrough de um módulo React, apontando padrões e antipadrões.  
- **TI:** 
    - Demonstra como criar playbook básico no Ansible e compartilha snippet anotado.  
    - Agendar 1:1 para explicar uso básico do Snipe-IT, mas sem acompanhar implementação.  

---

##### **3 – Mentor Confiável**  
**Descrição:** Acompanha o desenvolvimento de colegas, dando feedback regular e monitorando progresso.  

**Example behaviors:**  
- Realiza sessões de mentoria periódicas com agenda clara e metas de aprendizado.  
- Revisita tópicos anteriores para garantir absorção do conhecimento.  
- Incentiva colegas a praticar em projetos reais e acompanha resultados.  

**Example tasks:**  
- **HW/FW:** Guia junior na implementação de testes HIL completos, revisando resultados e sugerindo melhorias.  
- **Software:** Cria trilha de aprendizado (tutorial + projeto) para novos devs em microserviços, revisando código entregue.  
- **TI:** 
    - Prepara plano de desenvolvimento para analista júnior em automação de infraestrutura e revisa scripts entregues.  
    - Orientar analista júnior na automação de importação de SIM cards, revisando scripts entregues.  

---

##### **4 – Líder de Mentoria**  
**Descrição:** Estrutura programas de mentoria que impactam múltiplas pessoas e times, criando materiais e processos.  

**Example behaviors:**  
- Desenvolve currículo de treinamento e capacita outros mentores.  
- Avalia métricas de sucesso (ex.: tempo de ramp-up, feedback dos mentorados).  
- Ajusta programa com base em resultados e feedback.  

**Example tasks:**  
- **HW/FW:** Lança programa “Bootcamp de Firmware” com módulos teóricos e práticos, medindo evolução em radar de competências.  
- **Software:** Cria catálogo de projetos de exemplo e exercícios, conduz “office hours” semanais para todo o time.  
- **TI:** 
    - Desenvolve academias internas de Ansible e Kubernetes, com certificação prática e dashboards de progresso.  
    - Estruturar programa de treinamento em gestão de SIM cards e modems, com exercícios e avaliações práticas.  

---

##### **5 – Campeão de Desenvolvimento**  
**Descrição:** Define a cultura de mentoria na empresa, influenciando políticas de desenvolvimento de carreira e promovendo aprendizado contínuo.  

**Example behaviors:**  
- Institui processos formais de mentoria, capacitando líderes e mensurando impacto no engajamento.  
- Representa a empresa em conferências e comunidades para compartilhar práticas de mentoria.  
- Mentora outros mentores, criando uma rede de desenvolvimento interno.  

**Example tasks:**  
- **HW/FW:** Publica e mantém portal de mentoria em IoT, incluindo vídeos, guias interativos e sessões AMA (Ask Me Anything).  
- **Software:** Cria e gerencia programa de “Tech Fellowship”, selecionando e orientando mentores seniores.  
- **TI:** 
    - Define política de desenvolvimento de talentos em TI, com ciclos de mentoria 1:1, workshops trimestrais e métricas de retenção.  
    - Lançar “TI Academy” sobre conectividade móvel, ministrando treinamentos e certificando participantes.  

#### 2.3.3 Vision  
Enxerga o impacto da tecnologia no negócio e no usuário final. Antecipada tendências, propõe inovações e orienta roadmaps de produto para atender metas de mercado e clientes.

Avalia a capacidade de antecipar tendências, conectar tecnologia a objetivos de negócio e inspirar direção de produto.

---

##### **1 – Foco Tático**  
**Descrição:** Trabalha nas tarefas atribuídas sem considerar o impacto de longo prazo ou o contexto de produto.  

**Example behaviors:**  
- Concentra-se apenas na entrega técnica imediata.  
- Não demonstra interesse pela estratégia de produto ou mercado.  
- Não questiona requisitos além do escopo definido.  

**Example tasks:**  
- **HW/FW:** Implementa leitura de sensor conforme requisito, sem avaliar uso futuro dos dados.  
- **Software:** Adiciona logging básico a um microserviço sem conectar isso a métricas de negócio.  
- **TI:** 
    - Configura novo servidor de backup sem considerar crescimento previsto de dados.  
    - Executar atividades de gestão de SIM cards sem considerar tendências tecnológicas.  

---

##### **2 – Consciência Situacional**  
**Descrição:** Reconhece objetivos de médio prazo, mas não integra visão de produto ao propor soluções técnicas.  

**Example behaviors:**  
- Menciona metas de projeto em discussões, mas não as traduz em requisitos técnicos.  
- Busca entender roadmap, mas ainda não age proativamente para suportá-lo.  
- Comunica restrições de tecnologia sem propor alternativas.  

**Example tasks:**  
- **HW/FW:** Ajusta frequência de amostragem do sensor para atender SLA de coleta diário, mas sem otimizar consumo de energia.  
- **Software:** Escolhe biblioteca de análise de dados mencionada no roadmap, mas não valida escalabilidade.  
- **TI:** 
    - Planeja capacidade de armazenamento para três meses, sem alinhar com projeções de crescimento de usuários.  
    - Compartilhar roadmap de planos de dados com o time, mas sem propor inovação.  

---

##### **3 – Visão Integrada**  
**Descrição:** Conecta requisitos de produto, usuário e tecnologia para propor soluções coesas de médio e longo prazo.  

**Example behaviors:**  
- Propõe design de sistema considerando jornada do usuário e restrições técnicas.  
- Documenta impacto de decisões tecnológicas no roadmap de produto.  
- Compartilha insights de mercado/competição com a equipe.  

**Example tasks:**  
- **HW/FW:** Desenha fluxo de dados end-to-end para sensor IoT, incluindo gateway LoRa e integração com dashboard de cliente.  
- **Software:** Arquitetura de front-to-back que alinha UX com performance de API, garantindo SLAs de resposta.  
- **TI:** 
    - Elabora plano de adoção de cloud híbrida que equilibra custo, performance e requisitos regulatórios.  
    - Propor integração de SIM cards com IoT interno para coleta de métricas de energia predial.  

---

##### **4 – Proativo na Inovação**  
**Descrição:** Antecipates tendências tecnológicas e de mercado, liderando PoCs que validam novas oportunidades de produto.  

**Example behaviors:**  
- Identifica e avalia novas tecnologias (ex.: ML embarcado, edge computing, 5G) para casos de uso da empresa.  
- Aplica resultados de pesquisa em propostas de roadmap e MVPs.  
- Engaja stakeholders em discussões visionárias e demonstra valor da inovação.  

**Example tasks:**  
- **HW/FW:** Coordena PoC de ML embarcado em ESP32 para detecção de anomalias, medindo impacto em consumo de energia.  
- **Software:** Implementa PoC de processamento de vídeo em edge com WebAssembly, comparando performance em campo.  
- **TI:** 
    - Conduz teste de conectividade 5G e satellite failover para garantir cobertura total em unidades remotas.  
    - Conduzir PoC de conectividade redundante (4G + satélite) para sites remotos, medindo latência e confiabilidade.  

---

##### **5 – Arquiteto de Futuro**  
**Descrição:** Define e evangeliza a visão tecnológica da empresa, influenciando produto, operações e estratégia de mercado.  

**Example behaviors:**  
- Co-cria roadmaps de longo prazo com C-level e alinha investimentos em P&D.  
- Lidera comunidades e eventos focados em tendências tecnológicas para toda a organização.  
- Avalia e seleciona parcerias tecnológicas estratégicas e define padrões corporativos.  

**Example tasks:**  
- **HW/FW:** Publica e patrocina plataforma modular de IoT que serve como base para todos os futuros produtos, com diretrizes de expansão.  
- **Software:** Desenvolve “Tech Vision Deck” multianual que orienta arquiteturas de microserviços, segurança e dados para os próximos 5 anos.  
- **TI:** 
    - Define estratégia de multicloud e edge que reduz custos em 30% e melhora SLAs globais, coordenando com fornecedores e stakeholders.  
    - Definir visão de “Edge Connectivity Platform” que consolida todas as dimensões de conectividade da empresa em serviço gerenciado, integrando SIM cards, satélite e rede interna.  
