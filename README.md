# Docs-escopo-1-AE1
Projeto integracionista
# Operação Carga Rápida
## Agendamento Inteligente e Desmaterialização Logística

## Sobre o Projeto

O projeto **Operação Carga Rápida** foi desenvolvido como uma proposta de transformação digital para terminais de carga, visando reduzir filas, eliminar processos manuais e aumentar a eficiência operacional.

A solução utiliza um sistema de agendamento inteligente para retirada de cargas, assinatura eletrônica de documentos e envio automático de notificações, permitindo maior previsibilidade e agilidade no atendimento.

Além disso, o projeto incorpora conceitos de análise de dados, qualidade da informação, LGPD e sustentabilidade através da redução do uso de papel.

# Problema de Negócio

Atualmente os terminais de carga enfrentam diversos desafios operacionais:

- Longas filas para retirada de cargas;
- Tempo elevado de espera dos clientes;
- Uso excessivo de documentos impressos;
- Falta de atualização em tempo real das informações;
- Baixa previsibilidade da demanda operacional;
- Sobrecarga em horários de pico.

Esses fatores impactam diretamente a experiência do cliente, os custos operacionais e a produtividade do terminal.

# Objetivo Geral

Desenvolver um sistema digital de agendamento e assinatura eletrônica para otimizar o processo de retirada de cargas em terminais logísticos conectado ao sistema que a empresa já utiliza

# Objetivos Específicos

- Implementar uma plataforma de agendamento online.
- Disponibilizar assinatura eletrônica para retirada de cargas.
- Automatizar o envio de notificações aos clientes.
- Atualizar informações operacionais em tempo real.
- Reduzir o uso de papel nos processos logísticos.
- Melhorar o controle das filas de atendimento.

# Público-Alvo

## Beneficiários Diretos

- Clientes B2B
- Clientes B2C
- Transportadoras
- Empresas aéreas de carga
- Operadores logísticos

## Beneficiários Indiretos

- Equipes operacionais
- Supervisores de terminal
- Gestores logísticos

# Escopo do Projeto

## Inclusões

✔ Desenvolvimento da página de agendamento

✔ Assinatura eletrônica em dispositivos móveis

✔ Sistema de notificações automáticas

✔ Atualização online dos dados operacionais

✔ Dashboard de indicadores

✔ Controle digital de retiradas

## Exclusões

✖ Compra de equipamentos para o terminal

✖ Entrega física das mercadorias ao cliente final

✖ Gestão de transporte rodoviário

✖ Controle de armazenagem


# Perguntas Analíticas

1. Qual é o tempo médio atual de espera para retirada de cargas?

2. Quantas folhas de papel são utilizadas mensalmente?

3. Qual o percentual de atrasos nos horários de pico?

4. Como os clientes avaliam o processo atual?

5. Qual o ganho financeiro obtido com a digitalização?


# Indicadores de Desempenho (KPIs)

| Indicador | Objetivo |
|------------|------------|
| Tempo Médio de Atendimento (TMA) | Reduzir filas |
| Economia de Papel | Sustentabilidade |
| Tempo de Entrega do Alerta | Melhorar comunicação |
| Taxa de Comparecimento | Eficiência operacional |
| Percentual de Assinaturas Digitais | Digitalização |
| Ocupação dos Slots | Balanceamento da demanda |


# Critérios de Sucesso

O projeto será considerado bem-sucedido caso alcance:

- Redução de 50% no Tempo Médio de Atendimento;
- Redução de 90% do consumo de papel;
- Entrega de notificações em até 3 segundos;
- Aumento da satisfação dos usuários;
- Redução das filas nos terminais.

# Arquitetura da Solução

## Backend

- Python
- FastAPI

## Banco de Dados

- PostgreSQL

## Segurança

- Criptografia AES/Fernet
- HTTPS
- Controle de acesso

## Analytics

- Python
- Pandas
- Power BI

# Funcionalidades Implementadas

## Agendamento de Retirada

Permite que clientes realizem o agendamento prévio da retirada da carga.

## Sugestão Inteligente de Horários

O sistema distribui automaticamente os agendamentos ao longo do dia para evitar congestionamentos.

## Assinatura Eletrônica

Elimina formulários físicos e reduz o consumo de papel.

## Notificações Automáticas

Envio automático de confirmação e lembretes de agendamento.

## Dashboard Operacional

Visualização de indicadores operacionais em tempo real.

# Segurança e LGPD

O projeto segue as diretrizes da Lei Geral de Proteção de Dados (LGPD).

## Dados Protegidos

- CNPJ dos clientes
- CNPJ das transportadoras
- Assinaturas digitais

## Medidas Implementadas

- Criptografia de CNPJ utilizando Fernet
- Controle de acesso aos dados
- Registro de auditoria
- Comunicação segura

# Estrutura do Repositório

Docs-escopo-1-AE1/

│
├── README.md
│
├── app.py
│
├── requirements.txt
│
├── docs/
│   ├── Termo_Abertura.pdf
│   ├── Plano_Projeto.pdf
│   ├── Dicionario_Dados.xlsx
│   ├── Modelo_Logico.drawio
│   ├── Plano_Qualidade_Dados.md
│   └── Plano_EDA.md
│
├── database/
│   └── create_tables.sql
│
└── data/
    └── agendamentos.csv

# Modelo de Dados

## Principais Entidades

### Agendamento

- ID
- AWB
- CNPJ Cliente
- CNPJ Transportadora
- Data Agendamento
- Status

### Notificação

- ID
- Agendamento
- Data Envio
- Status

### Evento Gate

- Entrada
- Início Atendimento
- Fim Atendimento
- Saída

# Qualidade dos Dados

As seguintes validações foram definidas:

- Não permitir AWB duplicado.
- Não permitir campos obrigatórios nulos.
- Validar formato de placa Mercosul.
- Validar CNPJ.
- Garantir integridade referencial.
- Validar consistência temporal.
- Garantir armazenamento criptografado dos CNPJs.

# Plano de Análise (EDA)

## Análises Descritivas

- Volume de retiradas por dia
- Volume de retiradas por hora
- Tempo médio de atendimento
- Utilização dos slots

## Análises Diagnósticas

- Horários críticos
- Gargalos operacionais
- Cancelamentos

## Análises Preditivas

- Previsão de demanda
- Previsão de ocupação
- Identificação de picos

# Produto Final

O produto final será composto por:

- Portal de Agendamento
- API de Atendimento
- Sistema de Assinatura Digital
- Dashboard Operacional
- Sistema de Notificações
- Base Analítica para Tomada de Decisão

# Matriz de Riscos

| Risco | Mitigação |
|---------|---------|
| Queda da internet | Operação offline |
| Recusa ao aplicativo | Totens de apoio |
| Vazamento de dados | Criptografia |
| Sobrecarga do sistema | Escalabilidade |
| Falha no SMS | Canal alternativo |
| Falha de sincronização | Rotinas automáticas |


```bash
git clone https://github.com/sabrynasantossrs-tech/Docs-escopo-1-AE1.git
```

```bash
pip install -r requirements.txt
```

```bash
uvicorn app:app --reload
```

# Documentação da API

Após iniciar o sistema:

```text
http://localhost:8000/docs
```


# Tecnologias Utilizadas

- Python
- FastAPI
- PostgreSQL
- Cryptography
- Pandas
- Power BI
