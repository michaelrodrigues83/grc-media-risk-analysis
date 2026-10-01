# 📑 Relatório Técnico de GRC: Análise de Riscos e Conformidade em Mídia

**Autor:** Michael Hernandes Rodrigues  
**Contexto:** Projeto Prático de Desenvolvimento Profissional Contínuo  
**Escopo:** Avaliação de Vulnerabilidades Cibernéticas, Quebra de Diretrizes de GRC e Impacto Regulatório  
**Objetos de Análise:** *Privacidade Hackeada (2019)* e *O Dilema das Redes (2020)*  

---

## 🎯 Apresentação e Desenvolvimento Profissional

Este relatório reflete a aplicação prática dos conhecimentos técnicos que venho adquirindo ao longo da minha jornada acadêmica e trilha de especialização em Governança, Riscos e Conformidade (GRC). As análises críticas e diagnósticos de riscos aqui apresentados foram estruturados com base na correlação das seguintes formações:

* **Formação Acadêmica:** Cursando Segurança da Informação pela **FATEC**.
* **Lei Geral de Proteção de Dados (LGPD):** Curso EAD Essencial pela **Data Privacy Brasil**.
* **Segurança da Informação (ISO/IEC 27001):** Especialização em frameworks internacionais pela **Udemy**.
* **Google Cybersecurity Certificate:** Práticas de SOC, análise de logs e segurança defensiva pela **Google**.
* **Analista Júnior de Segurança Cibernética:** Fundamentos de redes, scripts e inteligência de ameaças pela **Cisco Networking Academy**.

---

## 🎬 Estudo de Caso 1: Privacidade Hackeada (2019)

### 1. Descrição do Incidente e Vetores de Ataque
O caso Cambridge Analytica expou um dos maiores escândalos de uso abusivo de dados da era moderna. Sob a ótica de segurança digital, o incidente **não decorreu da exploração de um malware sofisticado**, mas sim do abuso de privilégios em uma API do Facebook. Através de um aplicativo de teste acadêmico, coletou-se dados de usuários cadastrados e, de forma reflexiva, estendeu-se a coleta a toda a sua rede de contatos, impactando mais de 80 milhões de titulares.

### 2. Mapeamento de Não-Conformidades (ISO/IEC 27001:2022 / Udemy)
* **Controle A.8.2 (Privilégios de Acesso Mínimos):** Falha grave na concessão de permissões de API. O Facebook permitiu que uma aplicação de terceiros coletasse dados periféricos de usuários que sequer haviam interagido com o software.
* **Controle A.8.12 (Segurança em Interfaces de Programação de Aplicações - APIs):** Ausência de mecanismos de governança e *rate limiting* capazes de auditar, restringir e interromper a extração massiva de dados por terceiros.
* **Controle A.8.16 (Monitoramento e Análise de Logs):** Falha na implementação de ferramentas de monitoramento em tempo real. Como venho estudando na trilha da **Google**, a falta de correlação de eventos via ferramentas SIEM permitiu que a exfiltração massiva ocorresse sem o disparo de alertas automatizados.

### 3. Impacto Regulatório e Violações Legais (LGPD / Data Privacy Brasil)
O desfecho do incidente feriu o pilar da **Confidencialidade** da Tríade CID e serviu como catalisador para a promulgação do GDPR na Europa e, consequentemente, da LGPD no Brasil. Alinhado com a base teórica da **Data Privacy Brasil**, o caso configura infração direta aos seguintes pontos:
* **Art. 6º, I (Princípio da Finalidade):** Desvio massivo de finalidade. Dados coletados sob pretexto de pesquisa acadêmica foram convertidos em inteligência de manipulação psicológica em processos eleitorais.
* **Art. 6º, VII (Princípio da Segurança):** Ausência de medidas técnicas eficazes para salvaguardar os dados pessoais de acessos não autorizados.
* **Falta de Base Legal (Art. 7º):** Inexistência de consentimento legítimo ou legítimo interesse para o compartilhamento de dados de contatos terceiros da rede social.

---

## 🎬 Estudo de Caso 2: O Dilema das Redes (2020)

### 1. Diagnóstico do Cenário: O Capitalismo de Vigilância
O documentário analisa o modelo de negócios das Big Techs estruturado sob o conceito de Capitalismo de Vigilância. Do ponto de vista de GRC, o risco transcende o mero armazenamento ou vazamento de dados; reside na **Engenharia de Atenção Agressiva**. A plataforma rastreia variáveis milimétricas (como tempo de tela e velocidade de rolagem) para retroalimentar algoritmos de aprendizado de máquina voltados à manipulação comportamental do usuário por meio do sistema de recompensa de dopamina.

### 2. Mapeamento de Vulnerabilidades e Incidentes de SOC
* **Quebra do Pilar da Integridade da Informação:** O uso de algoritmos de recomendação baseados exclusivamente em engajamento (*Black Box Algorithms*) prioriza a disseminação desenfreada de desinformação, teorias da conspiração e *bots*.
* **Classificação de Incidentes no SOC:** Sob a perspectiva do treinamento de **Analista Júnior de Segurança Cibernética da Cisco**, campanhas coordenadas de desinformação e proliferação de contas automatizadas falsas (*bots*) devem ser tratadas como **Incidentes de Segurança de Alta Gravidade**, pois violam as Políticas de Uso Aceitável (AUP) e atacam diretamente a estabilidade das operações e a governança social.
* **Engenharia Social Automatizada:** Os scripts defensivos convencionais abordados pela **Cisco** e pelo **Google** ensinam o usuário a mitigar engenharia social baseada em phishing humano. No entanto, o filme demonstra uma Engenharia Social executada por código ofensivo automatizado (Python), gerando um risco invisível à atenção do usuário.

### 3. Análise de Conformidade e Direitos do Titular (LGPD)
A exploração psicológica oculta entra em conflito direto com as garantias estabelecidas na regulação de privacidade brasileira:
* **Art. 6º, VI (Princípio da Transparência):** O usuário acredita usufruir de um serviço gratuito, mas carece de informações claras e precisas sobre o tratamento agressivo de suas pegadas digitais para fins de perfilamento comportamental (*profiling*).
* **Art. 20 (Direito à Revisão de Decisões Automatizadas):** A LGPD garante ao titular o direito de solicitar a revisão de decisões tomadas unicamente com base em tratamento automatizado de dados que afetem seus interesses, o que se choca diretamente com o modelo de opacidade dos algoritmos de recomendação citados.

---

## 📊 Matriz de Riscos de GRC Comparativa

| Variável Analisada | Privacidade Hackeada (Facebook / Cambridge Analytica) | O Dilema das Redes (Big Techs / Redes Sociais) |
| :--- | :--- | :--- |
| **Vetor Principal de Risco** | Abuso de Privilégios em APIs de Terceiros e Exfiltração de Dados. | Perfilamento Psicológico (*Profiling*) e Engenharia de Atenção. |
| **Pilar da Tríade CID Afetado** | **Confidencialidade** (Acesso e compartilhamento indevido). | **Integridade** (Disseminação de dados falsos e desinformação). |
| **Principal Falha ISO 27001** | Controle A.8.2 (Privilégios) e Controle A.8.16 (Logs/SIEM). | Controle A.5.10 (Uso aceitável de ativos e políticas de IA). |
| **Principal Infração LGPD** | Art. 6º, I (Desvio de Finalidade) e Ausência de Base Legal. | Art. 6º, VI (Falta de Transparência) e Falhas no Perfilamento Automatizado. |
| **Mitigação em GRC** | Auditoria de APIs, *Zero Trust* e Monitoramento Ativo via SOC. | Transparência Algorítmica, Avaliação de Impacto à Privacidade (DPIA). |

---

## 🧠 Conclusão Geral do Analista

Ambos os estudos de caso comprovam que a segurança da informação e a privacidade não se resumem a barreiras de perímetro contra agentes maliciosos externos (*hackers*). Os maiores riscos corporativos mapeados decorrem do **desenho deliberado de modelos de negócios que violam a governança de dados**. 

Como profissional em pleno desenvolvimento técnico, o aprendizado essencial que extraio dessa análise para minha bagagem de GRC é que a verdadeira conformidade exige a implementação de uma cultura de *Privacy by Design* e *Privacy by Default*, onde a ética, o cumprimento estrito das bases legais (LGPD) e o monitoramento contínuo de controles (ISO 27001) sirvam como pilares de sustentação de qualquer organização em uma economia movida a dados.

---
[⬅️ Voltar para a Abertura de Análises](../README.md)
