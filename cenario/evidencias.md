# 🗂️ Evidências: Laboratório Maré Viva

> ⚠️ Material **fictício**. Leia primeiro o [cenário](laboratorio-mare-viva.md), que explica
> os termos técnicos usados aqui.

[⬅️ Voltar ao roteiro](../README.md) · [⬅️ Voltar ao cenário](laboratorio-mare-viva.md)

---

Estas são as **evidências** que a equipe de consultoria (vocês!) reuniu no laboratório em
setembro de 2026, incluindo documentos que o laboratório entregou. Cada trecho tem um código (por exemplo, **E2.4**). **Use esses códigos na
planilha** para mostrar de onde veio cada ativo, cada risco e cada nota de probabilidade e
impacto.

> 💡 **Como ler:** as pessoas não falam em "ameaça" e "vulnerabilidade". Elas contam fatos,
> reclamam, dão opiniões. O trabalho de vocês é **traduzir** esses fatos para a linguagem de
> risco. Uma frase pode revelar um ativo, uma vulnerabilidade, um controle que já existe
> (ou que só parece existir) e até um impacto.

| Código | Documento |
|---|---|
| [E1](#e1--entrevista-com-a-dra-helena-prado-diretora-geral) | Entrevista com a diretora-geral |
| [E2](#e2--entrevista-com-rafael-lima-coordenador-de-ti) | Entrevista com o coordenador de TI |
| [E3](#e3--entrevista-com-juliana-costa-supervisora-de-atendimento) | Entrevista com a supervisora de atendimento |
| [E4](#e4--resumo-da-varredura-de-vulnerabilidades) | Resumo da varredura de vulnerabilidades |
| [E5](#e5--registro-de-ocorrências-dos-últimos-12-meses) | Registro de ocorrências dos últimos 12 meses |
| [E6](#e6--mensagens-recebidas) | Mensagens recebidas pelo laboratório |

---

## E1 — Entrevista com a Dra. Helena Prado, diretora-geral

*Realizada em 10/09/2026.*

- **E1.1** — "Nosso maior medo é parar. Os dois hospitais parceiros exigem o resultado dos
  exames de urgência em até duas horas. Se atrasar, pagamos multa e podemos perder o contrato,
  que é um quarto do nosso faturamento."
- **E1.2** — "Conseguimos trabalhar no papel por umas quatro horas. Depois disso, a fila trava:
  temos que suspender as coletas e remarcar os pacientes."
- **E1.3** — "Um laudo com resultado errado é a pior coisa que pode nos acontecer, porque o
  médico pode tomar uma decisão errada sobre o paciente. Hoje, quem libera laudo na bancada usa
  o login genérico `bancada` no SIL, porque assim é mais rápido trocar de turno."
- **E1.4** — "Aprovamos R$ 150 mil para segurança no próximo ano. Não dá para fazer tudo; quero
  saber onde colocar esse dinheiro primeiro."
- **E1.5** — "O site institucional é só vitrine: endereços, horários e o 'Trabalhe conosco'. Se
  sair do ar um dia, ninguém morre."
- **E1.6** — "Já ouvi falar em seguro contra ataques cibernéticos. Será que vale a pena para nós?"
- **E1.7** — "Não quero ver a Maré Viva no jornal por vazamento de exames. Nossos pacientes
  confiam que um exame de gravidez ou de HIV fica só entre eles e o médico."

---

## E2 — Entrevista com Rafael Lima, coordenador de TI

*Realizada em 11/09/2026.*

- **E2.1** — "Somos três na TI, das 8h às 18h. À noite e no fim de semana, se der problema, o
  plantonista do laboratório me liga no celular."
- **E2.2** — "O SIL roda num servidor físico aqui na sede, com Windows Server 2012 R2 e banco
  SQL Server. A Kintal diz que a versão nova do sistema roda em Windows Server 2022, mas a
  migração custa caro e nunca entrou no orçamento."
- **E2.3** — "Os técnicos da Kintal entram no servidor por uma ferramenta de acesso remoto. A
  senha é a mesma para todos os técnicos deles desde a implantação, em 2019. Não sei quem lá
  conhece essa senha, nem se alguém que saiu da Kintal ainda sabe."
- **E2.4** — "O backup do SIL roda todo dia às 23h para o NAS, que fica na mesma sala do
  servidor e aparece no servidor como unidade de rede. Uma vez por mês, copio tudo para um HD
  externo e levo para casa — o HD não tem criptografia. Restauração completa? Nunca testamos; só
  recuperamos arquivos soltos."
- **E2.5** — "Três analisadores têm um computador acoplado com Windows 7. O fabricante não deixa
  atualizar: diz que o equipamento perde a validação. Eles estão na mesma rede que todo mundo."
- **E2.6** — "A rede da sede é uma só: estações, analisadores, servidor e o Wi-Fi dos
  visitantes. Os postos se ligam à sede por VPN."
- **E2.7** — "O e-mail é em nuvem. Só as cinco contas da diretoria têm MFA; para o resto, o
  pessoal reclamou e a gente desligou."
- **E2.8** — "Usamos um antivírus tradicional nas estações. Os logs do servidor ficam guardados
  sete dias e depois são sobrescritos. Ninguém olha log no dia a dia."
- **E2.9** — "Quando alguém sai da empresa, o RH deveria me avisar por e-mail. Às vezes avisa."
- **E2.10** — "O Portal de Resultados foi feito por um freelancer. O contrato acabou em 2024 e,
  desde então, ninguém mexe no código. Ele roda numa máquina virtual alugada de um provedor de
  nuvem."
- **E2.11** — "A sala de servidores fica no térreo, a duas quadras do canal. Tem um
  ar-condicionado só e um nobreak que segura uns 20 minutos. Gerador, não temos. Parte da sala
  virou depósito de caixas de material de coleta."
- **E2.12** — "As câmaras de amostras têm sensores de temperatura que mandam alerta. O painel do
  fabricante é acessado pela internet; acho que ninguém trocou a senha que veio de fábrica."
- **E2.13** — "Os quatro notebooks, da TI e da diretoria, têm criptografia de disco ativada."
- **E2.14** — "Cada posto de coleta tem um único link de internet. Em 2024, o link do posto do Guarujá
  caiu duas vezes, por umas três horas cada: o posto cadastrou os pacientes no papel e lançou tudo
  depois. Os exames de urgência dos hospitais são todos feitos na sede."

---

## E3 — Entrevista com Juliana Costa, supervisora de atendimento

*Realizada em 12/09/2026.*

- **E3.1** — "O agendamento é quase todo pelo WhatsApp Business, num celular da recepção da sede.
  Seis atendentes usam o mesmo aparelho, que fica sem senha de bloqueio para agilizar."
- **E3.2** — "Os pacientes mandam foto do pedido médico, da carteirinha do convênio e, às vezes,
  do documento. Fica tudo na galeria do celular."
- **E3.3** — "Quando o paciente não consegue entrar no portal, a gente manda o laudo em PDF pelo
  WhatsApp mesmo."
- **E3.4** — "Nos computadores da recepção, usamos o login `recepcao1`. Todo mundo sabe a senha:
  está num post-it no monitor."
- **E3.5** — "A senha do Wi-Fi dos visitantes está impressa num cartaz no balcão."
- **E3.6** — "Treinamento de segurança? Nunca tivemos. No ano passado, alguém clicou num e-mail
  falso de 'atualização do convênio', mas a TI disse que não deu em nada."
- **E3.7** — "Para entrar no portal, o paciente só digita CPF e data de nascimento. Muita gente
  gosta, porque não precisa lembrar senha."

---

## E4 — Resumo da varredura de vulnerabilidades

*Feita em 18/09/2026 por uma empresa especializada contratada pelo laboratório, com autorização da diretoria.*

> 🔎 **O que é uma varredura de vulnerabilidades?** É um teste feito com ferramentas automáticas
> que examinam os sistemas em busca de falhas **já conhecidas** (versões antigas, configurações
> inseguras, senhas de fábrica). Ela **não prova** que a falha pode ser explorada naquele
> ambiente, mas mostra **onde olhar**. A coluna "Severidade" é a opinião da ferramenta sobre a
> falha isolada — **não é** o nível de risco da Maré Viva, que depende dos critérios de
> probabilidade e impacto do laboratório.

| # | Ativo examinado | Exposto a | Componente detectado | Achado | Severidade |
|---|---|---|---|---|---|
| **E4.1** | Portal de Resultados (`portal.mareviva.example`) | Internet | PHP 7.4.33 | Versão sem suporte do fabricante desde novembro de 2022 | Alta |
| **E4.2** | Portal de Resultados | Internet | OpenSSH 7.4, porta 22 aberta para qualquer endereço | Acesso administrativo exposto à internet; versão antiga | Média |
| **E4.3** | Portal de Resultados | Internet | TLS 1.0 e 1.1 habilitados | Protocolos de criptografia obsoletos | Média |
| **E4.4** | Portal de Resultados | Internet | Endereço dos laudos no formato `/laudos/2026/000184532.pdf` | Número do laudo **sequencial e previsível**; o portal não confere se o laudo pertence a quem está logado | Alta |
| **E4.5** | Site institucional (WordPress) | Internet | WordPress e 4 plugins sem atualização há 14 meses | Componentes com vulnerabilidades públicas conhecidas | Alta |
| **E4.6** | Painel dos sensores de temperatura | Internet | Painel web do fabricante | **Aceita a senha padrão de fábrica** | Crítica |
| **E4.7** | Servidor do SIL (`SRV-SIL01`) | Rede interna | Windows Server 2012 R2 | Sistema operacional sem suporte desde outubro de 2023 | Alta |
| **E4.8** | Servidor do SIL | Rede interna | Ferramenta de acesso remoto (versão de 2021) | Software desatualizado; uma única senha para todos os técnicos do fornecedor | Alta |
| **E4.9** | 3 computadores de analisadores | Rede interna | Windows 7 com SMBv1 habilitado | Sistema sem suporte desde janeiro de 2020; vulnerável às falhas corrigidas pelo boletim MS17-010 da Microsoft | Crítica |
| **E4.10** | NAS de backup | Rede interna | Painel de administração por HTTP (sem o "S") | Usuário e senha trafegam sem criptografia na rede | Média |
| **E4.11** | Wi-Fi de visitantes | Rede interna | Mesma faixa de endereços das estações | Visitantes alcançam as estações e o servidor | Alta |

---

## E5 — Registro de ocorrências dos últimos 12 meses

*Compilado a partir de e-mails da TI e anotações da recepção.*

| # | Data | O que aconteceu | Consequência |
|---|---|---|---|
| **E5.1** | 14/11/2025 | Atendente da recepção clicou num e-mail falso (phishing) de "atualização cadastral do convênio" e digitou a senha do e-mail numa página falsa | A TI trocou a senha no dia seguinte. Ninguém verificou se houve acesso indevido à conta |
| **E5.2** | 22/01/2026 | Chuva forte com maré alta: falta de energia de **3 h 10 min** na sede | O nobreak acabou em 20 minutos e o servidor do SIL desligou de forma abrupta. Dois exames de urgência foram entregues com atraso: multa de R$ 6 mil |
| **E5.3** | 07/03/2026 (sábado) | O único ar-condicionado da sala de servidores parou | A sala chegou a 41 °C e o servidor do SIL se desligou sozinho por 2 horas |
| **E5.4** | 17/04/2026 | A conta de e-mail do gerente financeiro (sem MFA) foi invadida. O criminoso enviou a um fornecedor um boleto com dados bancários alterados, e o pagamento foi feito | Prejuízo de **R$ 38 mil** |
| **E5.5** | 09/06/2026 | Uma atendente enviou pelo WhatsApp o laudo de um paciente para o número de outro paciente | Reclamação formal do paciente. O caso não foi registrado como incidente de segurança |
| **E5.6** | 30/07/2026 | Uma ex-funcionária da recepção, desligada em maio, entrou no ERP com a própria conta, que continuava ativa | Descoberto por acaso. A conta foi desativada; não se sabe o que ela consultou |
| **E5.7** | 21/08/2026 | O alarme de temperatura de uma câmara de amostras não disparou durante a madrugada | **46 amostras descartadas**; pacientes chamados para nova coleta. Depois se viu que a configuração do alarme tinha sido alterada no painel, e ninguém da equipe se lembra de ter feito isso |

---

## E6 — Mensagens recebidas

- **E6.1** — Mensagem de uma paciente pelo "Fale conosco" do site, em 02/09/2026:
  > "Ao abrir meu exame pelo link do portal, troquei sem querer um número no endereço e apareceu
  > o exame de outra pessoa, com nome completo e resultado. Isso é muito grave!"

  *Situação em 30/09/2026: a mensagem foi encaminhada à TI. O portal continua funcionando do
  mesmo jeito (veja E4.4).*

- **E6.2** — E-mail de um pesquisador de segurança independente, em 15/09/2026:
  > "Encontrei num repositório público de código, na conta pessoal de um desenvolvedor, o
  > código-fonte do Portal de Resultados da Maré Viva. Um arquivo de configuração contém a chave
  > de acesso à API de autorização de exames dos convênios e a senha do banco de dados do portal.
  > Recomendo trocar essas credenciais o quanto antes."

  *Situação em 30/09/2026: as credenciais ainda não foram trocadas. O laboratório não conseguiu
  contato com o ex-freelancer.*

---

[⬅️ Voltar ao roteiro](../README.md) · [⬅️ Voltar ao cenário](laboratorio-mare-viva.md)
