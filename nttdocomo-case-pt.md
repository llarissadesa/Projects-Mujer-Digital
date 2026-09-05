# Caso: Invasão e vazamento de dados na NTT DOCOMO


## Tipo de incidente:
Roubo e fuga de dados (data breach) viabilizado por ataque à cadeia de suprimentos (supply chain attack) e compromentimento de credenciais corporativas.


## Sobre a empresa:
A NTT DOCOMO é a maior operadora de telecomunicações móveis do Japão, pertencente ao grupo NTT (Nippon Telegraph and Telephone). Ela processa e armazena dados de dezenas de milhões de cidadãos japoneses, incluindo informações pessoais sensíveis e dados financeiros para faturamento.


## O que aconteceu:
Houve um ataque de phishing - criminosos se passam por outra pessoa ou empresa confiável para enganar e roubar dados sensíveis -, onde os atacantes não invadiram os servidores centrais da empresa diretamente, em vez disso, eles comprometeram as credenciais de acesso de um funcionário de uma empresa parceira de TI que possuía acesso privilegiado aos sistemas de manutenção da operadora. Sem autenticação multifator (MFA) rigorosa no ambiente parceiro, os atacantes usaram esses acessos legítimos para extrair dados do banco de dados de clientes sem levantar alertas imediatos.
[imagem]


## Impacto:
**- Operacional e financeiro:** Necessidade de notificação massiva a clientes, custos com perícia forense, auditoria externa e reestruturação da infraestrutura de TI terceirizada.
**- Reputacional:** Exposição de milhões de registros de clientes e dados de contas, gerando perda de confiança pública na maior operadora do país.
**- Regulatório:** Investigação e sanções severas impostas pelo Ministérios dos Assuntos Internos e Comunicações (MIC) do Japão por falha na supervisão de subcontratados.


## Conceitos identificados:
**- Engenharia social/phishing:** Manipulação de pessoas para entregar dados confidenciais ou credenciais de acesso.
**- Princípio do menor privilégio (least privilege):** Prática de conceder a um usuário ou sistema apenas as permissões estritamente necessárias para realizar suas tarefas diárias.
**- Exfiltração de dados:** Transferência ou cópia não autorizada de informações confidenciais de dentro da rede corporativa para um ambiente externo controlado pelo invasor.
**- Zero trust:** Modelo de segurança baseado na premissa de sempre exigir autenticação e validação contínuas para qualquer usuário ou dispositivo.

## Profissionais da cibersegurança envolvidos:
**- Analistas SOC (Centro de Operações de Segurança):** Identificaram o volume anômalo de dados sendo transferidos fora de horário comercial.
**- Peritos Forense Computacional:** Rastrearam a origem dos acessos até as credenciais do funcionário terceirizado e analisaram logs para determinar a extensão do vazamento.
**- Equipe de engenharia de redes:** Revogaram imediatamente os acessos comprometidos, redefiniram segredos e isolaram os segmentos de rede afetados.
**- Encarregado de Proteção de Dados e relações públicas:** Comunicação oficial com os clientes afetados e reporte às autoridades reguladoras japonesas.


## Processo de resposta a incidentes:
**- Preparação:** Estabelecer políticas rigídas de acesso para terceiras e implementar MFA obrigatório em todas as conexões remotas.
**- Identificação:** Monitorar logs de autenticação e usar ferramentas de detecção de comportamentos anômalos.
**- Contenção:** Bloquear a conta do prestador, cortar a conexão VPN do parceiro e isolar os servidores de banco de dados afetados.
**- Erradicação:** Remover qualquer backdoor que possa ter sido instalado e redefinir todas as credenciais do ambiente de TI.
**- Recuperação:** Restabelecer a operação com rotinas adicionais de monitoramento e auditoria em tempo real sobre acessos privilegiados.
**- Lições aprendidas:** Revisar contratos de segurança com parceiros e realizar novas auditorias de compliance.


## Ferramentas usadas:
**- Gerenciamento de Informações e Eventos de Segurança:** Coleta e análise de logs para correlação dos eventos do ataque.
**- Gestão de acessos privilegiados:** Gestão e auditoria de acessos de contas com privilégios elevados.
**- Detecção e Resposta Gerenciadas/Detecção e Resposta em Endpoints:** Monitoramento contínuo de endpoints e servidores para identificar movimentação lateral.
**- Prevenção contra perda de dados:** Ferramentas para prevenir o envio de arquivos confidenciais para fora da rede.
