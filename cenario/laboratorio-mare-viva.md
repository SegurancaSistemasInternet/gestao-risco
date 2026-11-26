# 🏥 Cenário: Laboratório Maré Viva Análises Clínicas

> ⚠️ **Empresa fictícia**, criada só para esta atividade. Nomes, números e sistemas são
> inventados; qualquer semelhança com organizações reais é coincidência. **Não teste nenhum
> sistema real**: todo o trabalho é de análise, feito na planilha.

[⬅️ Voltar ao roteiro](../README.md)

---

## 1. A empresa

O **Laboratório Maré Viva** faz exames de sangue, urina e outros materiais biológicos na Baixada
Santista.

| Item | Situação |
|---|---|
| Unidades | Sede em **Santos**, onde as amostras são processadas e ficam os servidores, e 3 postos de coleta |
| Pessoas | 120 funcionários; cerca de **210 mil pacientes** cadastrados, com seus **laudos** (documentos com o resultado dos exames) |
| Clientes importantes | **2 hospitais** que exigem o resultado de exames de urgência em até **2 horas**, 24 horas por dia; atraso gera multa |
| TI (tecnologia da informação) | **3 pessoas**, das 8h às 18h. Ninguém se dedica só à segurança |

Duas coisas tornam este cenário especial:

- **Dados de saúde** são **dados pessoais sensíveis** pela LGPD (Lei Geral de Proteção de Dados
  Pessoais). Um vazamento de laudos é grave.
- Um **laudo errado** pode levar o médico a uma decisão errada: aqui, uma falha de **integridade**
  pode afetar a saúde de alguém.

---

## 2. Termos técnicos usados no cenário

| Termo | O que significa |
|---|---|
| **SIL** | Sistema de Informação Laboratorial: o sistema central do laboratório. Cadastra pacientes, recebe os resultados dos equipamentos e gera os laudos. Sem ele, o laboratório para |
| **Analisador** | Equipamento que processa as amostras e envia os resultados ao SIL. Alguns são controlados por um computador acoplado |
| **Servidor** | Computador que fica ligado o tempo todo oferecendo um serviço (aqui, o SIL) |
| **Sistema sem suporte** | Software que o fabricante deixou de atualizar. Falhas descobertas depois disso **nunca** serão corrigidas |
| **Backup** | Cópia de segurança dos dados, para recuperá-los se o original for perdido |
| **NAS** | Caixa com discos ligada à rede, usada aqui para guardar o backup. Se o servidor enxerga o NAS como uma pasta, um vírus no servidor também consegue apagá-lo |
| **Criptografia** | Embaralhar os dados com uma chave, de modo que só quem tem a chave consiga lê-los |
| **Acesso remoto** | Programa que permite controlar um computador à distância, pela internet |
| **Segundo fator (MFA)** | Além da senha, o sistema pede outra prova de identidade, como um código no celular |
| **Nobreak** | Equipamento com bateria que mantém os computadores ligados por alguns minutos quando falta energia |
| **Phishing** | Golpe em que o criminoso se passa por alguém confiável (por e-mail, por exemplo) para roubar senhas |
| **Ransomware** | Programa malicioso que embaralha os dados com criptografia e cobra resgate para devolvê-los |
| **SMBv1 e MS17-010** | SMBv1 é uma versão antiga do protocolo que o Windows usa para compartilhar arquivos na rede. MS17-010 é o código de um **boletim de segurança** da Microsoft (aviso de falha com a correção) sobre falhas graves no SMBv1 |

---

## 3. Sistemas e recursos

| Sistema / recurso | Como funciona hoje |
|---|---|
| **SIL** | Roda num servidor na sede. Quem dá suporte é a empresa **Kintal Sistemas**, por acesso remoto |
| **Analisadores** | 14 equipamentos; 3 deles são controlados por computadores com **Windows 7**, um sistema sem suporte desde 2020 |
| **Portal de Resultados** | Site onde o paciente baixa seus laudos. Feito por um programador autônomo, cujo contrato acabou em 2024; ninguém mais mexe nele |
| **E-mail** | Serviço de e-mail na nuvem (internet) para todos os funcionários |
| **WhatsApp da recepção** | Um celular usado pelas atendentes para agendar exames |
| **Backup** | Cópia diária do SIL num NAS **na mesma sala** do servidor, e cópia mensal num HD externo (disco rígido portátil) |
| **Sala de servidores** | No térreo da sede, perto de um canal. Um ar-condicionado e um nobreak de 20 minutos; **sem gerador** |
| **Site institucional** | Só informativo: endereços e horários |

**Regra importante do negócio:** se o SIL parar, o laboratório trabalha no papel por até
**4 horas**. Depois disso, precisa suspender as coletas.

---

## 4. Evidências

Estas são as informações que vocês, como consultoria, reuniram no laboratório. **Use os códigos
(E1, E2…) na planilha** para mostrar de onde tirou cada risco e cada nota.

> 💡 As pessoas não falam em "ameaça" ou "vulnerabilidade": elas contam fatos. O trabalho de
> vocês é **traduzir** esses fatos para a linguagem de risco.

### Entrevista com a Dra. Helena Prado, diretora-geral

- **E1** — "Nosso maior medo é parar. Se o resultado de urgência dos hospitais atrasa, pagamos
  multa e podemos perder o contrato, que é um quarto do nosso faturamento."
- **E2** — "Quem libera os laudos na bancada usa o login genérico `bancada` no SIL. É mais rápido
  na troca de turno, mas não dá para saber quem liberou cada laudo."
- **E3** — "O site institucional é só vitrine. Se sair do ar um dia, ninguém morre."

### Entrevista com Rafael Lima, coordenador de TI

- **E4** — "Os técnicos da Kintal entram no servidor do SIL por acesso remoto. A senha é a mesma
  para todos eles desde 2019. Nem sei quem lá conhece essa senha."
- **E5** — "O backup vai todo dia para o NAS, que fica na mesma sala do servidor e aparece no
  servidor como uma pasta. Restaurar tudo? Nunca testamos."
- **E6** — "Uma vez por mês copio o backup num HD externo e levo para casa. O HD não tem
  criptografia."
- **E7** — "Os 3 computadores com Windows 7 dos analisadores não podem ser atualizados, porque o
  fabricante não deixa. Eles estão na mesma rede que todos os outros computadores."
- **E8** — "Só as 5 contas de e-mail da diretoria têm segundo fator. Para os outros, o pessoal
  reclamou e a gente desligou."
- **E9** — "Quando alguém sai da empresa, o RH (recursos humanos) deveria me avisar para eu
  bloquear as contas. Às vezes avisa."
- **E10** — "Na sala de servidores, o nobreak segura uns 20 minutos. Gerador, não temos."

### Entrevista com Juliana Costa, supervisora de atendimento

- **E11** — "O celular do WhatsApp fica sem senha de bloqueio e é usado por 6 atendentes. Quando o
  paciente não consegue entrar no portal, mandamos o laudo em PDF pelo WhatsApp."
- **E12** — "Para entrar no portal, o paciente só digita CPF e data de nascimento. E treinamento
  de segurança, nunca tivemos."

### Registro de ocorrências dos últimos 12 meses

| Código | Data | O que aconteceu |
|---|---|---|
| **E13** | 22/01/2026 | Faltou energia por **3 horas** depois de uma chuva forte. O nobreak acabou em 20 minutos, o SIL parou e **dois exames de urgência atrasaram**: multa de R$ 6 mil |
| **E14** | 17/04/2026 | Um golpista roubou a senha do e-mail do gerente financeiro (conta **sem segundo fator**) e mandou a um fornecedor um boleto falso, que foi pago: prejuízo de **R$ 38 mil** |
| **E15** | 09/06/2026 | Uma atendente mandou pelo WhatsApp o laudo de um paciente para **outro paciente**. Houve reclamação formal |
| **E16** | 30/07/2026 | Uma ex-funcionária, desligada em maio, entrou no sistema financeiro (contas a pagar e boletos) com a conta dela, que **continuava ativa** |
| **E17** | 02/09/2026 | Uma paciente avisou que, ao **trocar um número no endereço** do link do seu laudo, apareceu o **exame de outra pessoa**. Até hoje o portal continua igual |

### Varredura de vulnerabilidades

*Teste automático feito por uma empresa contratada, em setembro de 2026.*

- **E18** — Os 3 computadores dos analisadores usam **Windows 7 com SMBv1 ativado** e estão
  vulneráveis às falhas descritas no boletim **MS17-010** da Microsoft. Severidade: crítica.

---

## 5. Critérios de risco do laboratório

Use **exatamente** estes critérios. Eles permitem comparar grupos diferentes: a justificativa de
cada nota deve dizer qual descrição foi usada.

### 5.1 Probabilidade (P)

| P | Nível | Use quando… |
|:-:|---|---|
| **1** | Rara | Exige condições raras ou acesso de administrador, e nunca aconteceu no laboratório |
| **2** | Possível | Exige algo a mais: uma senha, o erro de alguém, estar dentro da rede do laboratório, ou um evento comum (furto, perda, pane de equipamento ou de serviço) |
| **3** | Provável | **Já aconteceu** no laboratório nos últimos 12 meses **ou** está exposto na internet e pode ser explorado sem nenhuma barreira |

### 5.2 Impacto (I)

Veja as colunas e **use a mais alta**.

| I | Nível | Parada | Dinheiro | Dados pessoais | Pacientes |
|:-:|---|---|---|---|---|
| **1** | Baixo | Menos de 1 h | Menos de R$ 10 mil | Nenhum dado pessoal exposto | Sem efeito |
| **2** | Moderado | De 1 h a 4 h, sem atrasar urgências | De R$ 10 mil a R$ 100 mil | Dados de até 10 pacientes | Reclamação formal |
| **3** | Alto | Mais de 4 h **ou** atraso de urgência | Mais de R$ 100 mil | Dados de mais de 10 pacientes | Risco à saúde (laudo errado ou alterado) |

### 5.3 Nível, classificação e o que fazer

**Nível = P × I.**

| P \ I | **1** Baixo | **2** Moderado | **3** Alto |
|:-:|:-:|:-:|:-:|
| **3** Provável | 3 🟨 Médio | 6 🟥 Alto | 9 🟥 Alto |
| **2** Possível | 2 🟩 Baixo | 4 🟨 Médio | 6 🟥 Alto |
| **1** Rara | 1 🟩 Baixo | 2 🟩 Baixo | 3 🟨 Médio |

| Classificação | Nível | Regra do laboratório |
|---|:-:|---|
| 🟩 **Baixo** | 1–2 | Pode ser aceito |
| 🟨 **Médio** | 3–4 | Tratar **ou** aceitar com justificativa |
| 🟥 **Alto** | 6–9 | **Não pode ser aceito**: precisa de tratamento |

**Meta:** depois do tratamento, o risco residual deve ficar com **nível 4 ou menos**.

[⬅️ Voltar ao roteiro](../README.md)
