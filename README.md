# 🧭 Atividade: Identificação, Classificação e Tratamento de Riscos

### Cenário: Laboratório Maré Viva Análises Clínicas (fictício)

> **Disciplina:** Segurança de Sistemas · **Professor:** Claudio Nunes
> **Formato:** em grupo, de **2 a 4 integrantes**
> **Entrega:** uma planilha, pelo **Microsoft Teams** ([veja como entregar](#-como-entregar-no-microsoft-teams))
> **Prazo:** o que estiver indicado na tarefa publicada no Teams
> **Tempo estimado:** até **3 horas** de trabalho por grupo

---

## 🎯 O que você vai fazer

Seu grupo foi contratado como **consultoria de segurança** por um laboratório de análises
clínicas. O laboratório passou por vários sustos: um golpe com boleto falso, uma queda de energia
que atrasou exames de urgência e uma paciente que viu o exame de outra pessoa pelo portal.

Vocês vão:

1. **Ler** o cenário e as evidências.
2. **Identificar** pelo menos **8 riscos**.
3. **Classificar** cada risco com uma nota de probabilidade e de impacto.
4. **Pesquisar** uma vulnerabilidade pública.
5. **Propor um tratamento** para cada risco e estimar o risco que sobra.

Não há nada para instalar nem nenhum sistema para testar: tudo é feito numa planilha.

---

## 📦 O que entregar

**Um único arquivo:** a [planilha-modelo](modelos/registro-de-riscos-mare-viva.xlsx) preenchida,
em **.xlsx**, com o nome `Riscos_MareViva_<Sobrenomes>.xlsx`
(exemplo: `Riscos_MareViva_Silva-Souza-Oliveira.xlsx`).

> [!IMPORTANT]
> Antes de entregar, abra a aba `3 Resumo` da planilha: no fim dela, a **Conferência** mostra ✓
> ou ⚠ para cada exigência deste roteiro.

---

## 📚 Revisão rápida de conceitos

Leia antes de abrir o cenário (10 minutos).

### As peças do risco

| Conceito | O que é | Exemplo (numa escola de idiomas) |
|---|---|---|
| **Ativo** | Algo de valor que precisa ser protegido: informação, sistema, equipamento, pessoa, instalação | O cadastro de alunos |
| **Ameaça** | Quem ou o que **pode causar dano** (um criminoso, um erro humano, uma enchente) | Um golpista |
| **Vulnerabilidade** | A **fraqueza** que a ameaça aproveita | Senha fraca no sistema de matrículas |
| **Risco** | A **possibilidade** de a ameaça aproveitar a vulnerabilidade e causar um **impacto** | O golpista adivinhar a senha e copiar o cadastro |
| **Controle** | Medida que **reduz** o risco | Exigir senha forte e segundo fator (um código no celular, além da senha) |

> 💡 **Teste rápido:** a ameaça é o **"quem ou o quê"**, a vulnerabilidade é o **"por onde"** e o
> impacto é o **"e daí?"**.

### C-I-D: o que o risco afeta

| Letra | Propriedade | Pergunta |
|:-:|---|---|
| **C** | Confidencialidade | Só quem tem permissão **vê** a informação? |
| **I** | Integridade | A informação está **correta**? |
| **D** | Disponibilidade | O sistema funciona **quando é preciso**? |

### Probabilidade, impacto e matriz

- **Probabilidade (P):** a chance de acontecer nos próximos 12 meses, de 1 (rara) a 3 (provável).
- **Impacto (I):** o tamanho do dano se acontecer, de 1 (baixo) a 3 (alto).
- **Nível = P × I.** De 1 a 2 é **baixo**, de 3 a 4 é **médio** e de 6 a 9 é **alto**.
- **Matriz de risco:** tabela que cruza P e I e mostra onde estão os riscos mais graves. A
  planilha monta a matriz sozinha.

As notas não são "achismo": usem os **critérios do laboratório**, que estão no
[cenário](cenario/laboratorio-mare-viva.md#5-critérios-de-risco-do-laboratório).

### As quatro opções de tratamento

| Opção | O que significa | Exemplo |
|---|---|---|
| **Mitigar** | Aplicar um controle que diminui a chance ou o dano | Ativar segundo fator |
| **Evitar** | Deixar de fazer a atividade que gera o risco | Parar de guardar cópia do documento dos alunos |
| **Transferir** | Passar parte do prejuízo para outra empresa | Contratar um seguro |
| **Aceitar** | Decidir, por escrito, conviver com o risco | Aceitar que o site informativo fique fora do ar algumas horas por ano |

**Risco residual** é o que sobra **depois** do tratamento. Nenhum controle zera o risco.

### Vulnerabilidades públicas: CVE, CVSS e KEV

- **CVE** (*Common Vulnerabilities and Exposures*): código único de uma falha de software já
  divulgada, como `CVE-2021-44228`.
- **CVSS** (*Common Vulnerability Scoring System*): nota de 0 a 10 para a gravidade da falha.
- **KEV** (*Known Exploited Vulnerabilities*): lista da agência de cibersegurança dos EUA (CISA)
  com as falhas **já usadas em ataques reais**.

---

## 🛠️ Passo a passo

| Passo | Tarefa | Tempo |
|:-:|---|:-:|
| 1 | Organizar o grupo e baixar a planilha | 10 min |
| 2 | Ler o cenário e as evidências | 30 min |
| 3 | Identificar os riscos | 50 min |
| 4 | Dar as notas de probabilidade e impacto | 30 min |
| 5 | Pesquisar uma vulnerabilidade pública | 15 min |
| 6 | Propor o tratamento e o risco residual | 35 min |
| 7 | Conferir e entregar | 10 min |
| | **Total** | **3 h** |

### Passo 1 — Organizar o grupo e baixar a planilha

1. Formem o grupo (2 a 4 pessoas).
2. Baixem a [planilha](modelos/registro-de-riscos-mare-viva.xlsx): no GitHub, abram o arquivo e
   cliquem no botão **Download raw file** (seta para baixo, à direita).
3. Preencham a aba `Leia-me` com o nome e o RA (registro acadêmico) de cada integrante.

> 💡 A planilha funciona no **Excel** (inclusive o Excel na web, com a conta da universidade) e no
> **LibreOffice Calc**. Para editar juntos, coloquem o arquivo num chat do grupo no Teams.

### Passo 2 — Ler o cenário e as evidências

Leiam o [cenário](cenario/laboratorio-mare-viva.md) inteiro. Ele é curto e traz a empresa, os
termos técnicos, as evidências (E1 a E18) e os critérios de risco.

Para cada evidência, perguntem: **o que pode dar errado aqui?** Muitas vezes, duas evidências
falam do mesmo problema (por exemplo, uma entrevista conta a fraqueza e uma ocorrência mostra que
ela já foi explorada).

### Passo 3 — Identificar os riscos

Na aba `1 Riscos`, registrem **pelo menos 8 riscos**, um por linha. Para cada um, preencham o
ativo afetado, a ameaça, a vulnerabilidade, a letra C, I ou D e as evidências. Depois escrevam a
descrição com esta frase:

> **"Devido a** *[vulnerabilidade]*, *[ameaça]* **pode** *[o que acontece]*, **o que causaria**
> *[impacto]***."**

| ❌ Fraco | ✅ Bom (exemplo fora do cenário) |
|---|---|
| "Hackers invadirem o sistema." | "Devido à falta de segundo fator no sistema de matrículas, um golpista pode entrar com uma senha roubada e copiar o cadastro de alunos, o que causaria vazamento de dados." |

Exigências:

- [ ] pelo menos **8 riscos**;
- [ ] pelo menos **1 risco de cada letra**: C, I e D;
- [ ] **cada risco** com pelo menos uma evidência (por exemplo, `E5; E13`).

### Passo 4 — Dar as notas de probabilidade e impacto

Para cada risco, deem **P** e **I** de 1 a 3, seguindo os
[critérios do laboratório](cenario/laboratorio-mare-viva.md#5-critérios-de-risco-do-laboratório).
A planilha calcula o nível e a cor sozinha.

Na coluna **Justificativa**, escrevam uma frase curta dizendo qual critério usaram. Exemplo:

> *P3: já aconteceu (E13). I3: atrasou exames de urgência.*

### Passo 5 — Pesquisar uma vulnerabilidade pública

A evidência **E18** diz que os computadores dos analisadores são vulneráveis às falhas do boletim
**MS17-010**. Na aba `2 CVE`, registrem:

1. o **código CVE** de uma dessas falhas;
2. com as palavras do grupo, **o que ela permite** fazer;
3. a **nota CVSS**;
4. se ela está na lista **KEV** (sim ou não);
5. o **ID do risco** da aba `1 Riscos` a que ela se liga.

> 💡 Pesquisem "MS17-010" na [NVD](https://nvd.nist.gov/vuln/search) (*National Vulnerability
> Database*, a base de vulnerabilidades do governo dos EUA) e depois procurem o código CVE no
> [catálogo KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog).

### Passo 6 — Propor o tratamento e o risco residual

Para cada risco, escolham a **opção de tratamento** (mitigar, evitar, transferir ou aceitar) e
descrevam a **ação** de forma concreta: **o quê** e **onde**.

| ❌ Vago | ✅ Concreto (exemplo fora do cenário) |
|---|---|
| "Melhorar a segurança." | "Ativar segundo fator em todas as contas do sistema de matrículas." |

Depois, deem as notas **P residual** e **I residual**: como o risco fica **depois** da ação? O
controle reduz a chance (P), o dano (I) ou os dois?

Regras:

- [ ] nenhum risco **alto** pode ser aceito;
- [ ] usem **pelo menos 2 opções** de tratamento diferentes;
- [ ] o nível residual deve ficar em **4 ou menos**.

### Passo 7 — Conferir e entregar

1. Na aba `Leia-me`, indiquem se o grupo usou ferramentas de **inteligência artificial (IA)** e
   para quê. Usar como apoio é permitido, desde que seja declarado.
2. Confiram a coluna **Alertas** da aba `1 Riscos` e a **Conferência** da aba `3 Resumo`.
3. Entreguem no Teams (veja abaixo).

---

## 💡 Erros comuns

| Erro | Como corrigir |
|---|---|
| Confundir ameaça com vulnerabilidade ("a ameaça é a senha fraca") | A senha fraca é a **fraqueza**; a ameaça é **quem** se aproveita dela |
| Risco genérico ("ataque hacker") | Use a frase-padrão, com o ativo e o impacto concretos |
| Nota sem justificativa | Diga qual critério usou e cite a evidência |
| Dar nota máxima para tudo | Siga os critérios: um site só informativo fora do ar não é risco alto |
| Esquecer a **integridade** | Num laboratório, um laudo errado pode prejudicar o paciente |
| Risco residual zero | Nenhum controle elimina o risco; o mínimo é 1 |

---

## 📤 Como entregar no Microsoft Teams

1. No **Microsoft Teams**, entrem na equipe da disciplina e abram a aba **Tarefas**.
2. Abram a tarefa **"Atividade — Gestão de Riscos (Laboratório Maré Viva)"**.
3. Cliquem em **+ Adicionar trabalho** → **Carregar deste dispositivo** e anexem a planilha.
4. Cliquem em **Entregar** e confiram se o status mudou para **Entregue**.

> [!TIP]
> Se a tarefa estiver configurada **em grupo**, um integrante entrega por todos. Se não estiver,
> **cada integrante** anexa a mesma planilha. Até o prazo, dá para clicar em **Desfazer entrega**
> e trocar o arquivo.

---

## ❓ Perguntas frequentes

<details>
<summary><b>Precisa ter exatamente 8 riscos?</b></summary>

No mínimo 8. Qualidade vale mais que quantidade: 8 riscos bem escritos e justificados valem mais
que 15 genéricos.
</details>

<details>
<summary><b>Dois grupos podem dar notas diferentes para o mesmo risco?</b></summary>

Podem. O que importa é a nota seguir os critérios e estar justificada.
</details>

<details>
<summary><b>A planilha mostra ⚠ na coluna "Alertas". O que fazer?</b></summary>

O alerta avisa sobre algo incompleto ou contra as regras, como um risco alto marcado como
"Aceitar". Corrijam a linha até aparecer ✓.
</details>

<details>
<summary><b>Não tenho Excel. E agora?</b></summary>

Use o Excel na web, em [office.com](https://www.office.com), com a conta da universidade, ou o
LibreOffice Calc, que é gratuito. No Excel instalado no computador, use a versão 2019 ou mais
nova (ou o Microsoft 365).
</details>

---

## 📂 Estrutura deste repositório

```
gestao-risco/
├── README.md                              ← este roteiro
├── cenario/
│   └── laboratorio-mare-viva.md           ← empresa, termos, evidências e critérios
└── modelos/
    └── registro-de-riscos-mare-viva.xlsx  ← planilha para preencher e entregar
```

---

## 📜 Aviso de uso

Material **exclusivamente educacional**. O Laboratório Maré Viva, as pessoas e os fornecedores
citados são **fictícios**. A atividade é de análise: **não faça testes ou tentativas de acesso** a
sistemas reais. Testar sistemas de terceiros sem autorização é ilegal.
