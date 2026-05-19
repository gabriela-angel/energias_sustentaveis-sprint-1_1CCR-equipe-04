# GoodWe Challenge Sprint 1 - 1CCR Equipe 04

## EQUIPE
- Gabriela Angel Silva — RM: 570808
- Izabelly Menezes — RM: 570673
- Marcos Paulo Sampaio — RM: 573987
- Otávio Santos — RM: 570225
- Tiago Muhlmann — RM: 569569
- Wesley Marques — RM: 573915

## ÍNDICE
- [INTRODUÇÃO](#introdução)
  - [Contexto e Motivação](#contexto-e-motivação)
  - [Problema Central](#problema-central)
  - [Objetivo do Projeto](#objetivo-do-projeto)
- [CONTEXTUALIZAÇÃO DO DESAFIO](#contextualização-do-desafio)
  - [Sobre a GoodWe](#sobre-a-goodwe)
  - [ChargeGrid Intelligence](#chargegrid-intelligence)
  - [Transição: Residencial vs Comercial](#transição-residencial-vs-comercial)
  - [Os Quatro Pilares do ChargeGrid](#os-quatro-pilares-do-chargegrid)
    - [Controle de Demanda](#controle-de-demanda)
    - [Protocolos Abertos](#protocolos-abertos)
    - [Tarifação e Pagamento](#tarifação-e-pagamento)
    - [Inteligência Artificial](#inteligência-artificial)
- [ANÁLISE DE PROBLEMAS](#análise-de-problemas)
  - [Sobrecarga em Horários de Pico](#sobrecarga-em-horários-de-pico)
  - [Falta de Padronização](#falta-de-padronização)
  - [Complexidade de Cobrança](#complexidade-de-cobrança)
  - [Experiência do Usuário](#experiência-do-usuário)
  - [Ineficiência Energética](#ineficiência-energética)
- [SOLUÇÃO PROPOSTA](#solução-proposta)
  - [Descrição](#descrição)
  - [Como Funciona](#como-funciona)
  - [Impacto Esperado](#impacto-esperado)
  - [Tecnologias Utilizadas](#tecnologias-utilizadas)
  - [Princípios de Energias Renováveis e Sustentabilidade Utilizados](#princípios-de-energias-renováveis-e-sustentabilidade-utilizados)
- [REFERÊNCIAS](#referências)

## INTRODUÇÃO

### Contexto e Motivação
O Brasil vive um momento de inflexão histórica no setor de mobilidade. Em 2025, o mercado de veículos elétricos e híbridos plug-in registrou 223.912 unidades vendidas, crescimento de 26% em  relação  ao  ano  anterior,  e  os  dois  primeiros  meses  de  2026  já  somaram  48.591 emplacamentos — 90% a mais que no mesmo bimestre de 2025. O país acumula mais de 350 mil  veículos  plug-in  em  circulação  e  conta  com  16.880  eletropostos  públicos  e  semipúblicos, uma expansão de aproximadamente 290% desde 2023.

Esse  crescimento  acelerado  coloca  em  evidência  um  gargalo  estrutural:  a  infraestrutura  de recarga comercial — em shoppings, supermercados, postos de combustível e estacionamentos —  carece  de  inteligência  operacional.  Enquanto  o  hardware  dos  carregadores  evoluiu rapidamente, os sistemas de gestão de potência, faturamento, monitoramento em tempo real e interoperabilidade entre fabricantes ainda apresentam lacunas críticas. A sessão de recarga se tornou  um  evento  rico  em  dados,  mas  esses  dados  raramente  são  capturados,  analisados  e transformados em valor operacional ou comercial.

Nesse  cenário,  a  parceria  entre  a  FIAP  e  a  GoodWe  materializou  o  EV  Challenge  2026,  um desafio acadêmico baseado em problemas reais que propõe aos estudantes do 1º ano do curso presencial  o desenvolvimento de soluções concretas para a gestão inteligente de eletropostos comerciais.  A  motivação  central  é  clara:  transformar  cada  sessão  de  recarga  em  dados estruturados e inteligência acionável.

### Problema Central
O problema central identificado no desafio ChargeGrid Intelligence é a ausência de mecanismos integrados em eletropostos comerciais capazes de orquestrar potência, registrar ciclos de recarga, realizar faturamento automático e comunicar-se com sistemas de gestão externos.
 
Na prática, isso se traduz em quatro disfunções operacionais que coexistem no ecossistema atual:
 
- Opacidade energética: operadores de eletropostos não têm visibilidade em tempo real do consumo por ponto de carga, o que impede decisões de gestão de demanda e aumenta o risco de ultrapassagem de demanda contratada.
- Fragmentação de hardware: eletropostos de fabricantes diferentes utilizam protocolos proprietários, tornando impraticável a gestão centralizada de redes heterogêneas.
- Ausência de faturamento automatizado: a cobrança por sessão de recarga ainda depende de sistemas manuais ou soluções proprietárias desconexas da operação financeira do estabelecimento.
- Desperdício de capacidade instalada: sem previsão de demanda, os eletropostos operam de forma reativa, incapazes de distribuir carga de forma eficiente entre os pontos disponíveis.
 
### Objetivo do Projeto
O ChargeGrid Intelligence tem como objetivo projetar e prototipar um sistema de orquestração para redes de eletropostos comerciais que seja capaz de:
 
- Controlar dinamicamente a potência entregue a cada ponto de carga em tempo real, respeitando os limites da demanda contratada pelo estabelecimento;
- Integrar-se a equipamentos de diferentes fabricantes por meio dos protocolos abertos OCPP e MODBUS, eliminando dependência de soluções proprietárias;
- Automatizar o faturamento das sessões de recarga por meio de APIs de pagamento, habilitando modelos de negócio sustentáveis para o operador comercial;
- Aplicar inteligência artificial para prever picos de consumo, analisar padrões de uso e otimizar a alocação de potência na rede de carregadores.
 
O projeto é avaliado não apenas pela qualidade do código produzido, mas principalmente pelo raciocínio arquitetônico, pela visão de produto e pela capacidade de endereçar problemas regulatórios e operacionais reais do mercado brasileiro de mobilidade elétrica.

## CONTEXTUALIZAÇÃO DO DESAFIO

### Sobre a GoodWe
A GoodWe Technologies Co., Ltd. é uma das principais fabricantes globais de inversores solares e soluções de energia inteligente. Fundada em 2010 na China, a empresa atingiu a marca de 100 GW de capacidade instalada acumulada globalmente até 2025 — um crescimento que a colocou consistentemente no topo dos rankings mundiais de fabricantes de inversores.
 
A empresa tem subsidiárias em múltiplas regiões, incluindo sede europeia na Alemanha, e opera em mercados como Austrália, Europa, América Latina e Ásia.
 
No campo da mobilidade elétrica, a GoodWe lançou em 2022 a linha HCA Series de carregadores AC para uso residencial, compatível com todos os modelos de veículos elétricos e com os inversores e sistemas de armazenamento da própria marca. Em 2024, foi lançada a versão HCA G2, com a funcionalidade de balanceamento dinâmico de carga — ausente na geração anterior. A empresa integra seus carregadores à plataforma de monitoramento SEMS (Smart Energy Management System), permitindo gestão unificada de geração fotovoltaica, armazenamento e recarga de veículos.
 
O ecossistema GoodWe — composto pelos carregadores EV, pelos inversores e pelo sistema SEMS — é o substrato tecnológico sobre o qual o EV Challenge 2026 foi construído. 

### ChargeGrid Intelligence
O ChargeGrid Intelligence é a trilha do EV Challenge 2026 destinada à turma do 1º ano presencial da FIAP. Enquanto a trilha EV ChargeOps (turma online) foca em gestão compartilhada de eletropostos em condomínios e ambientes corporativos, o ChargeGrid Intelligence direciona sua atenção ao setor comercial e de varejo — eletropostos em estacionamentos de shoppings, supermercados, hotéis e postos de combustível.
 
A proposta do ChargeGrid Intelligence é desenvolver uma plataforma de Gestão Comercial, Controle de Demanda e Operação em Tempo Real, estruturada sobre quatro pilares: Controle de Demanda, Protocolos Abertos, Tarifação e Pagamento, e Inteligência Artificial Aplicada. A arquitetura proposta é híbrida, com três camadas interdependentes:
 
- Camada Física: o hardware de carregamento — EV Charger FIAP, medidores MODBUS e controladores OCPP — que coleta dados brutos de energia e eventos de sessão.
- Camada de Conectividade: a rede/internet que transporta os dados entre o hardware e os sistemas de processamento.
- Camada Digital: onde residem as Regras de Controle, o Módulo Analítico (IA) e as APIs de Pagamento — a inteligência que transforma dados em decisões operacionais.
 
A orquestração exige sincronia perfeita entre os limites elétricos do hardware e a flexibilidade lógica do software. Essa é exatamente a complexidade que o desafio propõe resolver.

### Transição: Residencial vs Comercial
Compreender a diferença entre soluções de recarga residencial e comercial é essencial para dimensionar adequadamente a proposta do ChargeGrid Intelligence. As duas categorias compartilham o hardware básico de carregamento, mas divergem profundamente em requisitos operacionais, regulatórios e de negócio.
 
No ambiente residencial, o carregador é instalado em uma única unidade habitacional, atende um único usuário ou família, opera sob uma única fatura de energia elétrica e não precisa gerenciar múltiplos pontos simultâneos. A GoodWe HCA Series, por exemplo, foi projetada para esse contexto: integra-se ao sistema fotovoltaico doméstico e permite que o excedente solar carregue o veículo de forma gratuita. O gerenciamento é simples e realizado por um único aplicativo (SEMS). A gestão de demanda é de baixa complexidade, pois o consumo total do domicílio é relativamente previsível.
 
No ambiente comercial, o cenário muda radicalmente. Um shopping center, por exemplo, pode operar dezenas de eletropostos simultaneamente, cada um com usuários distintos, pagamentos independentes e necessidade de controle granular de potência para não ultrapassar a demanda contratada com a distribuidora — o que geraria multas e custos elevados. O operador precisa de dashboards em tempo real, relatórios de faturamento por sessão, integração com gateways de pagamento, alertas de falha e capacidade de ajuste remoto de potência por ponto de carga.
  
Essa transição de escala e complexidade justifica toda a arquitetura proposta pelo ChargeGrid Intelligence e explica por que soluções residenciais, mesmo as mais sofisticadas, não podem ser simplesmente transplantadas para o ambiente comercial.

### Os Quatro Pilares do ChargeGrid
O ChargeGrid Intelligence organiza sua proposta em torno de quatro pilares fundamentais. Cada pilar representa uma dimensão crítica do problema e propõe uma abordagem específica para resolvê-la.

#### Controle de Demanda
O Controle de Demanda é o pilar responsável pelo gerenciamento da potência entregue aos eletropostos em tempo real. Em ambientes comerciais, a distribuidora de energia cobra não apenas pelo consumo em kWh, mas também pela demanda de ponta em kW — e ultrapassagens da demanda contratada geram tarifas adicionais severas. Um estabelecimento que opera 20 carregadores de 22 kW cada pode, no pior cenário, demandar 440 kW simultaneamente, o que pode exceder em muito a demanda contratada.
 
A solução proposta pelo ChargeGrid é o gerenciamento inteligente dessa potência: o sistema monitora o consumo total em tempo real e, quando necessário, reduz dinamicamente a potência entregue a carregadores individuais para manter o consumo total dentro dos limites contratados. Esse processo, conhecido na literatura técnica como load balancing ou demand management, permite que o operador maximize o número de veículos atendidos sem incorrer em custos adicionais.
 
Conceito técnico: o sistema define um limite de potência global (ex: 100 kW) e distribui essa carga entre os carregadores ativos. Quando um novo veículo se conecta, o algoritmo redistribui a alocação disponível. Quando um veículo desconecta, a potência liberada é redistribuída para os demais.
 
Desafios e limitações: a principal limitação é a latência de comunicação. Em redes com muitos carregadores, o tempo de resposta entre a detecção de um evento (conexão de veículo) e o ajuste efetivo de potência pode criar janelas de instabilidade. Além disso, a granularidade do controle depende das capacidades do hardware — nem todos os carregadores suportam ajuste dinâmico de potência via OCPP com a mesma precisão.
 
Riscos: um sistema de controle de demanda mal calibrado pode degradar a experiência do usuário ao reduzir excessivamente a velocidade de carregamento. Há também o risco de falhas de comunicação entre o backend e o carregador resultarem em consumo descontrolado.

#### Protocolos Abertos
O pilar de Protocolos Abertos endereça o problema da fragmentação de hardware: cada fabricante de eletropostos tende a desenvolver protocolos proprietários, criando silos de dados e impossibilitando a gestão centralizada de redes com equipamentos de múltiplas origens. O ChargeGrid propõe a integração via OCPP (Open Charge Point Protocol) e MODBUS — os dois protocolos mais relevantes no ecossistema de carregamento EV.
 
OCPP (Open Charge Point Protocol): é o protocolo de comunicação padrão entre estações de carregamento e sistemas de gerenciamento (CSMS — Charging Station Management Systems). Desenvolvido em 2009 e mantido pela Open Charge Alliance (OCA), o OCPP define como o carregador reporta status, consumo de energia, eventos de sessão e códigos de erro, e como o sistema central envia comandos de início/parada de sessão, atualizações de firmware e perfis de carregamento. Em 2024, a versão OCPP 2.0.1 foi aprovada como padrão IEC (IEC63584), e a versão OCPP 2.1 — com suporte a V2G (vehicle-to-grid) — foi lançada em 2025.
 
MODBUS: é um protocolo industrial amplamente utilizado para comunicação com medidores de energia, CLPs (Controladores Lógicos Programáveis) e outros equipamentos físicos. No contexto do ChargeGrid, o MODBUS é utilizado para leitura de medidores de energia instalados nos quadros elétricos, permitindo correlacionar o consumo total do estabelecimento com o consumo específico dos eletropostos.
 
Impacto da interoperabilidade: pesquisas da OCA indicam que o mercado de plataformas OCPP atingiu US$ 1,47 bilhão em 2024 e cresce a 22,8% ao ano. Operadores que adotam sistemas proprietários enfrentam custos de migração três a cinco vezes maiores ao tentar trocar de plataforma. A interoperabilidade via OCPP é, portanto, não apenas uma escolha técnica, mas um requisito estratégico para o mercado.
 
Desafios e limitações: a principal dificuldade é que, embora o OCPP defina uma linguagem comum, implementações de diferentes fabricantes apresentam variações e extensões proprietárias que comprometem a compatibilidade. A certificação pela OCA ajuda, mas não é universalmente adotada. A coexistência de versões (OCPP 1.6, 2.0.1 e 2.1) também cria complexidade: nem todos os carregadores suportam as versões mais recentes, e as versões 1.6 e 2.0.1 não são diretamente compatíveis entre si.
 
Riscos: vulnerabilidades de segurança cibernética em implementações OCPP já foram documentadas, incluindo riscos de sequestro de sessão, spoofing de dispositivos e ataques de negação de serviço. A adoção da arquitetura OCPP no ChargeGrid exige atenção à camada de segurança da comunicação.

#### Tarifação e Pagamento
O pilar de Tarifação e Pagamento é o que habilita o modelo de negócio sustentável para o operador comercial de eletropostos. O ChargeGrid propõe uma cobrança dinâmica acionada por APIs de pagamento — um sistema capaz de ajustar o preço da recarga em função de variáveis como horário, demanda da rede, disponibilidade de carregadores e preço da energia.
 
Do ponto de vista regulatório, a Resolução Normativa ANEEL nº 1.000/2021 consolidou as regras para o serviço público de distribuição de energia elétrica e incorporou, entre seus dispositivos, a regulamentação da recarga de veículos elétricos. O marco regulatório brasileiro permite que a recarga pública e comercial opere com preços livremente negociados, sem necessidade de autorização específica da ANEEL — o que torna não apenas legal, mas obrigatório o desenvolvimento de plataformas de tarifação dinâmica para viabilizar modelos de negócio competitivos.
 
A tarifação dinâmica endereça múltiplos objetivos simultaneamente: maximiza a receita do operador, distribui a carga ao longo do dia reduzindo picos, e oferece ao usuário incentivos para carregar em horários de menor demanda. Estudos demonstram que preços menores em determinadas estações atraem mais usuários, aliviando congestionamentos em estações de maior preço.
 
Desafios e limitações: a complexidade de gerenciar múltiplas estruturas de precificação (por kWh, por minuto, taxa fixa) simultâneas com tarifas dinâmicas é significativa. Há também o desafio regulatório de garantir transparência ao usuário — pesquisas indicam que a confusão sobre preços de recarga é um desafio significativo, com quase metade dos usuários relatando dificuldade para encontrar informações sobre custos antes de iniciar uma sessão.
 
Riscos: a opacidade de preços pode gerar desconfiança e afastar usuários. Cobranças surpresa são um problema documentado no mercado norte-americano e europeu, e podem se reproduzir no Brasil à medida que o mercado amadurece. Além disso, a dependência de conectividade de rede para processar pagamentos significa que falhas de internet podem interromper completamente a capacidade de monetização do operador.

#### Inteligência Artificial
O pilar de Inteligência Artificial é o "motor invisível" — a camada que dá sentido aos dados brutos gerados pela rede de eletropostos. A IA no ChargeGrid não é uma funcionalidade decorativa, mas o núcleo lógico que integra e potencializa os três pilares anteriores.
 
As aplicações de IA propostas pelo ChargeGrid Intelligence organizam-se em três funções:
 
- Interpretação: decodificação de eventos de sessão via protocolos industriais em tempo real. O sistema traduz streams de dados OCPP e MODBUS em eventos semânticos (início de sessão, anomalia de consumo, falha de hardware) que podem ser processados e apresentados ao operador.
- Preditividade: previsão de necessidades de expansão de infraestrutura antes da sobrecarga. Modelos de machine learning analisam padrões históricos de uso para antecipar momentos de alta demanda e sugerir ajustes preventivos — como rebalancear a alocação de potência antes do horário de pico.
- Conversão: uso de NLP (Processamento de Linguagem Natural) para traduzir terabytes de dados brutos em orientações diretas para usuários finais e operadores. Um dashboard que exibe não apenas gráficos, mas insights em linguagem natural (ex: "A demanda de carregamento deve aumentar 40% nas próximas 2 horas — recomenda-se reduzir a potência dos pontos 3, 7 e 12") representa um salto qualitativo na usabilidade.
 
Do ponto de vista técnico, os modelos mais eficazes para previsão de demanda em estações de carregamento incluem redes neurais LSTM (Long Short-Term Memory), modelos transformer e algoritmos como XGBoost, dependendo do horizonte de previsão (minutos, horas ou dias) e da escala espacial (estação individual, região ou cidade). Pesquisas recentes indicam que fatores externos como condições climáticas, preços da energia, tráfego e eventos locais influenciam significativamente a demanda de carregamento e precisam ser incorporados aos modelos.
 
Desafios e limitações: modelos de IA treinados em dados de uma única localidade ou rede tendem a não generalizar bem para outros ambientes. A escassez de dados históricos — especialmente em redes novas — é um gargalo para o treinamento de modelos precisos. Além disso, inconsistências nos dados de entrada (leituras de medidores ausentes, sessões incompletas) impactam diretamente a acurácia das previsões.
 
Riscos: modelos de previsão de demanda com baixa acurácia podem levar a decisões equivocadas de controle de potência, gerando tanto subaproveitamento da capacidade instalada quanto ultrapassagem de demanda contratada. Há também o risco de viés em algoritmos de precificação dinâmica, que podem penalizar desproporcionalmente usuários em horários de necessidade real.

## ANÁLISE DE PROBLEMAS
Esta seção analisa os principais problemas identificados no contexto do ChargeGrid Intelligence, conectando cada um deles aos pilares do desafio e propondo caminhos de solução fundamentados na literatura técnica e nas práticas de mercado.

### Sobrecarga em Horários de Pico
A concentração de demanda de carregamento em períodos específicos do dia é um dos desafios mais documentados na literatura de infraestrutura EV. Estudos mostram que usuários de veículos elétricos tendem a carregar predominantemente no final da tarde e à noite — exatamente quando a demanda residencial e comercial já é naturalmente elevada. Em estacionamentos de shoppings e supermercados, há um padrão adicional de concentração nos horários de pico de visitação (fins de semana e feriados).
 
Essa sobreposição de picos cria dois problemas simultâneos: do lado do operador, o risco de ultrapassagem de demanda contratada com a distribuidora; do lado do usuário, tempos de espera elevados e redução na velocidade de carregamento quando o sistema limita a potência disponível.
 
Conexão com os pilares: este problema conecta diretamente o Pilar de Controle de Demanda (que precisa gerenciar ativamente a potência em tempo real) e o Pilar de Inteligência Artificial (que pode prever os picos e ajustar proativamente a distribuição de potência antes que a sobrecarga ocorra). O Pilar de Tarifação também é acionado, pois preços dinâmicos mais elevados em horários de pico são um mecanismo comprovado para redistribuir a demanda ao longo do dia.

### Falta de Padronização
A coexistência de carregadores de múltiplos fabricantes em uma mesma rede — cada um com seu protocolo de comunicação, formato de dados e API proprietária — cria um ambiente de gestão extremamente fragmentado. Operadores de redes maiores reportam que a integração manual de dados de diferentes fabricantes é um dos principais gargalos operacionais, consumindo tempo e recursos que deveriam estar focados na expansão da infraestrutura.
 
O problema se agrava quando o operador tenta escalar: adicionar um novo fabricante ao ecossistema significa, na prática, desenvolver uma nova integração do zero. Estima-se que operadores de sistemas proprietários enfrentam custos de migração três a cinco vezes maiores quando decidem trocar de plataforma de gestão.
 
Conexão com os pilares: este problema é o núcleo do Pilar de Protocolos Abertos. A adoção do OCPP como padrão de comunicação universal é a resposta direta à fragmentação. Ao impor OCPP como requisito da arquitetura, o ChargeGrid garante que qualquer carregador certificado possa ser integrado à plataforma sem desenvolvimento adicional. O Pilar de Controle de Demanda também depende diretamente da padronização: sem uma interface de comunicação uniforme, é impossível enviar comandos de ajuste de potência de forma consistente a carregadores de fabricantes distintos.

### Complexidade de Cobrança
O faturamento de sessões de recarga comercial é intrinsecamente mais complexo do que a simples leitura de um medidor de energia, e a tarifação dinâmica adiciona outra camada de complexidade: o preço pode variar ao longo da sessão conforme as condições da rede mudam.
 
Do lado do pagamento, a integração com múltiplos métodos (cartão de crédito/débito, carteiras digitais, RFID, QR Code via Pix) exige conformidade com padrões de segurança rigorosos (PCI DSS) e integração com múltiplos gateways de pagamento. A reconciliação financeira — garantir que cada kWh faturado corresponda a um pagamento efetivo — é outro desafio operacional significativo.

Conexão com os pilares: este problema é o domínio central do Pilar de Tarifação e Pagamento, mas também impacta o Pilar de IA (que define os parâmetros de precificação dinâmica) e o Pilar de Protocolos Abertos (pois o OCPP 2.0.1 inclui funcionalidades nativas de faturamento e controle de sessão que simplificam a integração).

### Experiência do Usuário
A experiência do usuário em eletropostos comerciais é frequentemente subestimada como problema técnico, mas tem impacto direto na adoção de veículos elétricos. Pesquisas realizadas em mercados maduros (EUA, Europa) indicam que a confiabilidade dos carregadores é um dos principais fatores de satisfação — e que carregadores públicos ainda apresentam índices de confiabilidade inferiores aos postos de gasolina convencionais, com dados insuficientes sendo o principal problema identificado.
 
No contexto brasileiro, problemas adicionais incluem: falta de informação antecipada sobre disponibilidade e preço dos carregadores, necessidade de múltiplos aplicativos para diferentes redes, e ausência de feedback em tempo real sobre o progresso da recarga. Quase 40% dos usuários em mercados estudados relataram ter pago valores significativamente diferentes do esperado.
 
Conexão com os pilares: todos os quatro pilares do ChargeGrid contribuem para a experiência do usuário. O Controle de Demanda garante velocidade de carregamento consistente. Os Protocolos Abertos permitem que diferentes redes sejam acessadas por uma única plataforma. A Tarifação transparente elimina surpresas de preço. A IA pode informar proativamente o usuário sobre o tempo estimado de conclusão da recarga, sugerir horários alternativos e notificar sobre disponibilidade de carregadores próximos.

### Ineficiência Energética
A ineficiência energética em redes de eletropostos comerciais manifesta-se em duas formas complementares: subutilização de capacidade instalada e desperdício por operação não otimizada. Carregadores ociosos em horários de baixa demanda representam capital imobilizado sem retorno. Carregadores operando sem gestão de demanda podem causar picos desnecessários que encarecem a tarifa de toda a unidade consumidora.
  
Conexão com os pilares: o Pilar de Inteligência Artificial é o principal endereçador deste problema, por meio de modelos de previsão de demanda que permitem planejar a operação da rede com antecedência. O Pilar de Controle de Demanda atua na correção em tempo real. O Pilar de Tarifação pode ser usado para incentivar carregamento nos horários de menor custo de energia (off-peak).

## SOLUÇÃO PROPOSTA

### Descrição
A solução desenvolvida pelo grupo é uma plataforma unificada de gestão comercial de eletropostos, composta por um dashboard web para operadores e uma camada de API que intermedia a comunicação entre os carregadores físicos e a inteligência da plataforma. O produto atua como o "cérebro" da rede de recarga: recebe dados brutos dos equipamentos, processa esses dados com regras de negócio e modelos preditivos, e devolve decisões operacionais (como ajustes de potência, geração de cobranças e alertas) em tempo real.

A plataforma não substitui o hardware existente, mas o potencializa. Ao se posicionar como um CSMS (Charging Station Management System) independente de fabricante, ela resolve simultaneamente os quatro problemas centrais identificados neste documento: sobrecarga em horários de pico, fragmentação de hardware, complexidade de cobrança e ineficiência energética; por meio de quatro módulos integrados: Controle Dinâmico de Potência, Predição de Demanda por Inteligência Artificial, Integração por Protocolos Abertos e Faturamento Automatizado.

### Como Funciona
**Controle Dinâmico de Potência**
A plataforma mantém um orçamento de potência configurável para cada site (por exemplo, 100 kW totais para um estacionamento). A cada evento de conexão ou desconexão de veículo, o backend recalcula em tempo real a alocação disponível e envia limites de potência atualizados a cada carregador individualmente, via comandos OCPP. Dessa forma, o consumo total da rede nunca ultrapassa o limite contratado com a distribuidora, independentemente do número de veículos conectados simultaneamente. Quando um veículo é desconectado, a potência liberada é redistribuída automaticamente entre os carregadores ativos, maximizando a eficiência da capacidade instalada.

**Predição de Demanda por Inteligência Artificial**
A plataforma coleta e armazena dados de cada sessão de recarga — horário de início, duração, energia consumida, dia da semana e condições externas relevantes. Sobre esses dados, é treinado um modelo preditivo que estima a demanda futura com antecedência. A saída do modelo é diretamente consumida pela camada de controle de potência: se o sistema prevê um pico de demanda nas próximas horas, ele sugere um ajuste do orçamento de potência antes que a sobrecarga ocorra, em vez de reagir somente quando o limite já foi atingido. A precisão do modelo melhora continuamente à medida que mais dados históricos são acumulados.

**Integração por Protocolos Abertos (OCPP e MODBUS)**
A plataforma implementa um servidor OCPP próprio, ao qual qualquer carregador compatível com o protocolo pode se conectar, independentemente do fabricante. Uma camada de abstração de protocolos traduz mensagens de diferentes versões do OCPP e leituras MODBUS dos medidores de energia para um formato interno unificado. A camada de negócio — controle de demanda, tarifação, IA — opera exclusivamente sobre esse formato interno, sem conhecimento das particularidades de cada equipamento. Isso torna a plataforma escalável: adicionar um novo fabricante à rede não exige desenvolvimento adicional na lógica de negócio.

**Faturamento Automatizado**
Cada sessão de recarga gera automaticamente um registro de cobrança contendo horário de início e término, energia consumida em kWh e tarifa aplicada. Ao final da sessão, o módulo de faturamento aplica as regras de precificação vigentes e aciona a integração com um gateway de pagamento para processar a cobrança. O módulo de faturamento é desacoplado da lógica de controle de carregamento, o que permite que as regras de precificação sejam ajustadas de forma independente do hardware. A transparência de preços é garantida pela exibição do custo estimado ao usuário antes e durante a sessão.

### Impacto Esperado
Do ponto de vista operacional, espera-se que a plataforma elimine o risco de ultrapassagem de demanda contratada, que representa um dos principais custos imprevistos para operadores comerciais de eletropostos. A gestão ativa de potência permite atender um número maior de veículos simultaneamente sem ampliar a infraestrutura elétrica contratada, aumentando a rentabilidade do operador com o capital já investido.

A predição de demanda por IA introduz uma mudança de paradigma na operação: de reativa para proativa. Em vez de responder a sobrecargas quando elas já ocorreram, o sistema as antecipa e distribui a carga de forma preventiva, reduzindo tanto o custo energético quanto a degradação da experiência do usuário em horários de pico.

A padronização via OCPP reduz drasticamente os custos de integração e manutenção ao longo do ciclo de vida da rede. Operadores que hoje dependem de plataformas proprietárias enfrentam custos de migração de três a cinco vezes maiores — a adoção de protocolos abertos elimina essa dependência e preserva a liberdade de escolha de equipamentos futuros.

O faturamento automatizado transforma a sessão de recarga em uma transação comercial rastreável e auditável, habilitando modelos de negócio sustentáveis para o operador e eliminando a dependência de processos manuais. A transparência de preços, por sua vez, reduz a fricção na adoção por parte dos usuários finais.

### Tecnologias Utilizadas
A plataforma é construída sobre um conjunto de tecnologias cujas escolhas refletem não apenas critérios técnicos de viabilidade, mas também princípios de sustentabilidade, eficiência energética e responsabilidade ambiental.

Python como linguagem principal do backend foi escolhido por sua maturidade no ecossistema de ciência de dados e aprendizado de máquina, pela disponibilidade de bibliotecas especializadas para OCPP e por sua ampla adoção em sistemas de monitoramento energético. A escolha de uma linguagem interpretada de alto nível reduz o tempo de desenvolvimento e facilita a manutenção — o que, em um contexto de inovação em energia limpa, significa que a equipe pode iterar mais rapidamente sobre as regras de eficiência energética sem custo de complexidade tecnológica.

Biblioteca OCPP para Python viabiliza a implementação do servidor CSMS com aderência ao padrão aberto da Open Charge Alliance, sem dependência de SDKs proprietários. A escolha pelo padrão aberto é, em si, uma decisão de sustentabilidade sistêmica: ela garante que a plataforma possa integrar equipamentos de qualquer fabricante, prolongando a vida útil dos ativos já instalados e reduzindo o desperdício gerado pela obsolescência prematura de hardware funcional.

Modelos de Machine Learning (regressão e redes LSTM) são utilizados para predição de demanda. A justificativa sustentável é direta: um modelo preditivo que antecipa picos de consumo permite que a energia disponível seja distribuída de forma mais eficiente, reduzindo desperdícios operacionais e evitando a necessidade de ampliar a capacidade instalada de forma preventiva e excessiva. A eficiência na alocação de recursos energéticos é, por definição, um princípio de sustentabilidade aplicada.

Banco de dados relacional para armazenamento de sessões, eventos e histórico de consumo. A persistência estruturada dos dados energéticos é condição necessária tanto para o treinamento dos modelos de IA quanto para a geração de relatórios de consumo que podem subsidiar decisões de expansão de infraestrutura com base em evidência, e não em estimativas — o que reduz o risco de superdimensionamento ou subdimensionamento da rede.

Dashboard web responsivo como interface do operador. A escolha por uma solução web — em vez de aplicativo nativo — reduz a barreira de adoção, não exige instalação em dispositivos específicos e pode ser acessada de qualquer terminal, o que diminui indiretamente a necessidade de hardware dedicado para monitoramento.

APIs de pagamento com suporte a meios de pagamento digitais nativos do mercado brasileiro. A digitalização completa do ciclo de cobrança elimina processos físicos, reduz o uso de papel e permite a rastreabilidade financeira das transações energéticas — alinhando a operação comercial aos padrões ESG crescentemente exigidos por investidores e reguladores.

### Princípios de Energias Renováveis e Sustentabilidade Utilizados
O primeiro fundamento é a eficiência no uso de energia já disponível. Um dos princípios centrais da transição energética é que a energia mais sustentável é aquela que não precisa ser gerada — ou seja, a eficiência é prioritária sobre a expansão de capacidade. O módulo de controle dinâmico de potência opera exatamente sobre esse princípio: em vez de simplesmente disponibilizar mais energia para atender picos, ele redistribui a energia existente de forma mais inteligente, adiando ou evitando a necessidade de ampliar a infraestrutura contratada.

O segundo fundamento é a integração com fontes renováveis. A arquitetura da plataforma — especialmente sua compatibilidade com o ecossistema GoodWe de inversores fotovoltaicos e armazenamento — permite que energia solar gerada no próprio estabelecimento seja prioritariamente direcionada para os eletropostos. Isso reduz a dependência da rede elétrica convencional e potencializa o uso de energia limpa gerada localmente, alinhando a operação dos eletropostos com os objetivos da matriz energética renovável brasileira.

O terceiro fundamento é a redução de desperdício por previsão e planejamento. Modelos de demanda energética baseados em IA permitem que o operador planeje a operação da rede com antecedência, evitando tanto o superdimensionamento quanto o subaproveitamento da capacidade instalada. O desperdício de capital em infraestrutura ociosa é também um desperdício de recursos materiais e energéticos que foram empregados na fabricação e instalação desses equipamentos — a otimização pelo uso de dados é, portanto, uma forma de sustentabilidade do ciclo de vida do ativo.

O quarto fundamento é a tarifação como instrumento de gestão da demanda energética. A tarifação dinâmica não é apenas um mecanismo de receita: é uma ferramenta de incentivo comportamental alinhada aos princípios de resposta à demanda (demand response) amplamente adotados em redes elétricas inteligentes. Ao praticar preços menores nos horários de menor demanda — geralmente coincidentes com maior geração solar —, a plataforma incentiva os usuários a carregar seus veículos quando a energia é mais abundante e limpa, contribuindo para o equilíbrio da rede elétrica como um todo.

Por fim, o quinto fundamento é a longevidade tecnológica como sustentabilidade sistêmica. A adoção de protocolos abertos (OCPP e MODBUS) garante que os equipamentos físicos instalados hoje possam continuar sendo gerenciados pela plataforma mesmo após atualizações de software ou mudanças de fornecedor. Isso evita o descarte prematuro de hardware funcional — uma das formas menos visíveis, mas mais impactantes, de desperdício tecnológico no setor de energia.

## REFERÊNCIAS
[1] ABVE — Associação Brasileira de Veículos Elétricos. Dados de mercado 2025. Disponível em: https://abve.org.br/abve-data/
[2] AutoIndústria. A nova geografia da recarga elétrica no Brasil. Fevereiro de 2026. Disponível em: https://www.autoindustria.com.br/2026/02/24/a-nova-geografia-da-recarga-eletrica-no-brasil/
[3] Cenário Energia. Infraestrutura de recarga rápida para veículos elétricos cresce 59% em seis meses no Brasil. Setembro de 2025. Disponível em: https://cenarioenergia.com.br/2025/09/12/infraestrutura-de-recarga-rapida-para-veiculos-eletricos-cresce-59-em-seis-meses-no-brasil/
[4] GoodWe Technologies. HCA Series EV Charger. Disponível em: https://en.goodwe.com/hca-series
[5] GoodWe Technologies. GoodWe is Accelerating the Global Transition Toward a New Power System. Novembro de 2025. Disponível em: https://en.goodwe.com/goodwe-is-accelerating-the-global-transition-toward-a-new-power-system
[6] Open Charge Alliance (OCA). Open Charge Point Protocol — OCPP. Disponível em: https://openchargealliance.org/protocols/open-charge-point-protocol/
[7] Wikipedia. Open Charge Point Protocol. Disponível em: https://en.wikipedia.org/wiki/Open_Charge_Point_Protocol
[8] Monta. Open charge point protocol (OCPP): Definition, versions, benefits, and software. 2026. Disponível em: https://monta.com/en/blog/ocpp/
[9] EVBoosters. OCPP explained. Agosto de 2024. Disponível em: https://evboosters.com/ev-charging-academy/articles-blogs/ocpp-explained/
[10] Amina Charging. A Complete Guide to OCPP for EV Charging. Dezembro de 2025. Disponível em: https://aminacharging.com/articles/complete-guide-ocpp-ev-charging/
[11] Uland Power. What is OCPP? The Complete Guide to Open Charge Point Protocol for EV Charging. 2026. Disponível em: https://www.ulandpower.com/blog/what-is-ocpp-ev-charging-guide/
[12] Driivz. How AI is Transforming EV Charging Networks Globally. Dezembro de 2024. Disponível em: https://driivz.com/blog/ai-transformative-role-in-ev-charging-networks/
[13] Kyriakopoulos, I.; Theodoridis, Y. Electric Vehicle Charging Load Forecasting: An Experimental Comparison of Machine Learning Methods. ArXiv, Abril de 2026. Disponível em: https://arxiv.org/pdf/2512.17257
[14] MDPI Electronics. Artificial Intelligence-Driven Optimal Charging Strategy for Electric Vehicles and Impacts on Electric Power Grid. Abril de 2025. Disponível em: https://www.mdpi.com/2079-9292/14/7/1471
[15] MDPI Energies. Machine Learning-Based Electric Vehicle Charging Demand Forecasting: A Systematized Literature Review. Setembro de 2025. Disponível em: https://www.mdpi.com/1996-1073/18/17/4779
[16] MDPI Engineering Proceedings. Dynamic Pricing for Load Balancing in Electric Vehicle Charging Stations: An Integration with Open Charge Point Protocol. Outubro de 2025. Disponível em: https://www.mdpi.com/2673-4591/112/1/11
[17] Transport Topics. EV Charging Rates Go Dynamic. Maio de 2025. Disponível em: https://www.ttnews.com/articles/ev-charging-rates-go-dynamic
[18] Driivz. Payment Terminals for EV Charging. Fevereiro de 2026. Disponível em: https://driivz.com/glossary/payment-terminals/
[19] ANEEL. Resolução Normativa nº 1.000, de 7 de dezembro de 2021. Disponível em: https://www2.aneel.gov.br/cedoc/ren20211000.html
[20] Voltbras. Legislação Brasileira sobre eletropostos: o que saber antes de investir. Fevereiro de 2026. Disponível em: https://voltbras.com/normas-tecnicas-e-legislacao/legislacao-brasileira-sobre-eletropostos-o-que-saber-antes-de-investir/
[21] Gazeta do Povo. Rede de recarga cresce para acompanhar alta dos carros elétricos. Março de 2026. Disponível em: https://www.gazetadopovo.com.br/energia/carros-eletricos-rede-recarga-avanca-brasil-acompanhar-alta/
[22] SolarQuotes. 15 Years Of GoodWe Solar Gear. Novembro de 2025. Disponível em: https://www.solarquotes.com.au/blog/goodwe-solar-anniversary-mb3313/
[23] OpenOCPP — Open-source embedded software for EV chargers. Disponível em: https://openocpp.com/
[24] NCBi/PMC. Optimizing EV charging stations and power trading with deep learning and path optimization. 2025. Disponível em: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12250350/
