#  VetCare System

> Sistema de gestão projetado para a **VetCare Clínica Veterinária**, com foco no controle de agendamentos, consultas, prontuários, vacinações, estoque de medicamentos, internações e pagamentos integrados com Stripe e notificações via SendGrid.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O <b>VetCare System</b> é um projeto de software desenvolvido para propor uma solução digital para a <b>VetCare Clínica Veterinária</b>, que atualmente realiza grande parte do controle de agendamentos, consultas, prontuários, estoque e cobranças por meio de anotações manuais e planilhas desorganizadas.
        O sistema tem como objetivo melhorar a organização clínica, permitindo o cadastro de tutores, animais, controle de consultas, prescrições, exames, vacinações, internações, estoque de medicamentos, pagamentos e envio automático de lembretes por e-mail.
      </div>
    </td>
    
  </tr>
</table>

---

## 🚧 Status do Projeto

![Status](https://img.shields.io/badge/status-em%20projeto-blue?style=for-the-badge)
![UML](https://img.shields.io/badge/UML-PlantUML-orange?style=for-the-badge)
![Projeto](https://img.shields.io/badge/Projeto%20de%20Software-Documentação-green?style=for-the-badge)
![Versão](https://img.shields.io/badge/Versão-1.0-blue?style=for-the-badge)

> Este projeto não possui implementação de código-fonte. O objetivo é apresentar a documentação, arquitetura e modelagem UML de um sistema proposto.

---

## 📚 Índice

- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Problema Identificado](#-problema-identificado)
- [Objetivos](#-objetivos)
- [Atores do Sistema](#-atores-do-sistema)
- [Casos de Uso](#-casos-de-uso)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Diagramas UML](#-diagramas-uml)
- [Modelos de Dados](#-modelos-de-dados)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Autores](#-autores)

---

## 🔗 Links Úteis

- 📖 **PlantUML:** [https://plantuml.com/](https://plantuml.com/)
- 💳 **Stripe:** [https://stripe.com/br](https://stripe.com/br)
- 📧 **SendGrid:** [https://sendgrid.com/](https://sendgrid.com/)

---

## 📝 Sobre o Projeto

O **VetCare System** é uma proposta de sistema web para a **VetCare Clínica Veterinária**, um estabelecimento que oferece serviços de consultas clínicas, vacinação, exames laboratoriais, cirurgias e internação de animais domésticos. A clínica atende diferentes espécies (cães, gatos, aves e pequenos roedores) e trabalha com diferentes formas de pagamento: dinheiro, cartão de débito, cartão de crédito e Pix.

Atualmente, o controle da clínica é feito principalmente por meio de anotações manuais e planilhas desorganizadas. Esse processo dificulta o acompanhamento do histórico clínico dos animais, o controle de estoque, o gerenciamento da agenda dos veterinários e o acompanhamento financeiro.

A proposta do sistema é centralizar essas informações em uma aplicação digital, integrando pagamentos via **Stripe** e notificações automáticas via **SendGrid**.

---

## ❗ Problema Identificado

A VetCare Clínica Veterinária possui um processo manual para controlar agendamentos, consultas e estoque. Esse controle pode gerar problemas como:

- dificuldade em acompanhar o histórico clínico dos animais;
- falta de controle sobre o estoque de medicamentos e insumos;
- dificuldade no gerenciamento da agenda dos veterinários;
- falta de acompanhamento financeiro das consultas e procedimentos;
- ausência de lembretes automáticos de consultas e reforços de vacinas para os tutores;
- risco de perda de informações por registros manuais.

---

## 🎯 Objetivos

### Objetivo Geral

Projetar um sistema para informatizar o controle de agendamentos, consultas, prontuários, vacinações, estoque, pagamentos e notificações da VetCare Clínica Veterinária.

### Objetivos Específicos

- Cadastrar tutores e animais;
- Agendar e gerenciar consultas veterinárias;
- Registrar consultas, prescrições, exames e prontuários;
- Controlar vacinações e datas de reforço;
- Registrar internações e altas de animais;
- Controlar estoque de medicamentos e insumos;
- Processar pagamentos via Stripe (cartão de crédito/débito);
- Enviar notificações e lembretes por e-mail via SendGrid;
- Gerar orçamentos, notas fiscais e relatórios financeiros;
- Gerenciar usuários e permissões de acesso.

---

## 👥 Atores do Sistema

| Ator | Descrição |
|---|---|
| Administrador | Acesso total ao sistema. Gerencia usuários, serviços, relatórios e configurações. |
| Recepcionista | Cadastra tutores e animais, agenda consultas, registra pagamentos e emite orçamentos. |
| Veterinário | Realiza consultas, prescreve medicamentos, solicita exames e registra internações. |
| Tutor / Cliente | Proprietário do animal. Não acessa o sistema diretamente, mas seus dados são cadastrados. |
| Sistema SendGrid | Serviço de envio de e-mails transacionais para notificações e comprovantes. |
| Sistema Stripe | Plataforma de pagamentos para processar transações com cartão de crédito/débito. |

---

## 📍 Casos de Uso

| ID | Caso de Uso | Ator Principal |
|---|---|---|
| UC-01 | Cadastrar Tutor | Administrador / Recepcionista |
| UC-02 | Cadastrar Animal | Administrador / Recepcionista |
| UC-03 | Agendar Consulta | Recepcionista |
| UC-04 | Cancelar Agendamento | Recepcionista |
| UC-05 | Registrar Consulta | Veterinário |
| UC-06 | Prescrever Medicamento | Veterinário |
| UC-07 | Solicitar Exame | Veterinário |
| UC-08 | Registrar Resultado de Exame | Veterinário |
| UC-09 | Emitir Prontuário | Veterinário |
| UC-10 | Registrar Vacinação | Veterinário |
| UC-11 | Controlar Estoque de Medicamentos | Administrador |
| UC-12 | Registrar Venda de Produto | Administrador / Recepcionista |
| UC-13 | Emitir Orçamento | Recepcionista |
| UC-14 | Registrar Pagamento | Recepcionista |
| UC-15 | Gerar Nota Fiscal | Sistema |
| UC-16 | Enviar Notificação / Lembrete | Sistema |
| UC-17 | Consultar Histórico do Animal | Veterinário / Recepcionista |
| UC-18 | Gerar Relatório Financeiro | Administrador |
| UC-19 | Gerenciar Usuários e Permissões | Administrador |
| UC-20 | Cadastrar Serviço / Procedimento | Administrador |
| UC-21 | Registrar Internação | Veterinário |
| UC-22 | Registrar Alta do Animal | Veterinário |
| UC-23 | Consultar Agenda do Dia | Veterinário / Recepcionista |

---

## ✨ Funcionalidades Principais

- 🔐 **Autenticação de Usuários:** acesso ao sistema por administrador, recepcionista e veterinário.
- 👤 **Cadastro de Tutores:** registro de nome, CPF, telefone, endereço e observações.
- 🐶 **Cadastro de Animais:** cadastro de animais vinculados a tutores (cães, gatos, aves e roedores).
- 📅 **Agendamento de Consultas:** agendamento com data, hora, veterinário e serviço.
- 🩺 **Registro de Consultas:** sintomas, diagnóstico, tratamento e geração de prontuário.
- 💊 **Prescrição de Medicamentos:** prescrições com dose e frequência vinculadas a consultas.
- 🔬 **Solicitação e Resultado de Exames:** registro e anexo de resultados ao prontuário.
- 💉 **Controle de Vacinação:** registro de vacinas aplicadas e próximas datas de reforço.
- 🏥 **Registro de Internações:** controle de internação com motivo, status e alta.
- 📦 **Controle de Estoque:** gerenciamento de entrada e saída de medicamentos e insumos.
- 💰 **Pagamentos via Stripe:** processamento de pagamentos com cartão de crédito/débito.
- 📧 **Notificações via SendGrid:** envio automático de lembretes e comprovantes por e-mail.
- 🧾 **Orçamentos e Notas Fiscais:** emissão de orçamentos detalhados e notas após pagamento.
- 📊 **Relatórios Financeiros:** consulta de receitas, pagamentos e inadimplência.

---

## 🛠 Tecnologias Utilizadas

As tecnologias abaixo são propostas para a arquitetura do sistema, considerando uma aplicação web moderna.

### 💻 Front-end

- **Framework/Biblioteca:** React
- **Build Tool:** Vite
- **Gerenciamento de Rotas:** React Router
- **Deploy:** Vercel

### 🖥️ Back-end

- **Linguagem:** Java 17
- **Framework:** Spring Boot
- **Banco de Dados:** PostgreSQL (Supabase)
- **ORM:** Spring Data JPA / Hibernate
- **Autenticação:** Spring Security com JWT
- **Deploy:** Railway

### 🔗 Integrações Externas

- **Stripe** — processamento de pagamentos (cartão de crédito/débito)
- **SendGrid** — envio de e-mails transacionais e notificações

### 📐 Modelagem e Documentação

- **Diagramas UML:** PlantUML
- **Documentação:** Markdown

---

## 🏗 Arquitetura

O sistema foi projetado com uma arquitetura em camadas, separando as responsabilidades da aplicação em front-end, back-end, banco de dados e integrações externas.

### Camadas Propostas

- **Camada de Apresentação:** interface web em React + Vite, hospedada na Vercel.
- **Camada de Aplicação:** API REST em Java com Spring Boot, hospedada no Railway.
- **Camada de Domínio:** regras de negócio de agendamentos, consultas, pagamentos e estoque.
- **Camada de Persistência:** banco de dados PostgreSQL na Supabase, acessado via Spring Data JPA/Hibernate.
- **Sistemas Externos:** integração com Stripe (pagamentos) e SendGrid (e-mail).

### Visão Geral

```text
Usuário (Navegador)
        ↓
Front-end React + Vite (Vercel)
        ↓
API REST Spring Boot (Railway)
        ↓
Banco de Dados PostgreSQL (Supabase)
        ↓
Sistemas Externos: Stripe | SendGrid
```

---

## 📊 Diagramas UML

Os diagramas do sistema foram elaborados utilizando **PlantUML**. Os arquivos estão localizados na pasta `Códigos/`.

| Diagrama | Arquivo |
|---|---|
| Diagrama de Caso de Uso | `Códigos/caso-de-uso.puml` |
| Diagrama de Classes | `Códigos/diagram-classes.puml` |
| Diagrama de Componentes | `Códigos/componentes.puml` |
| Diagrama de Implantação | `Códigos/implantacao.puml` |
| Diagrama de Comunicação | `Códigos/comunicação-agendar-consulta.puml` |
| Diagrama de Estados - Agendamento | `Códigos/estados-agendamentos.puml` |
| Diagrama de Estados - Pagamento | `Códigos/estados-pagamentos.puml` |
| Sequência - Agendar Consulta | `Códigos/sequancia-agendar-consulta.puml` |
| Sequência - Registrar Consulta | `Códigos/sequancia-registrar-consulta.puml` |
| Sequência - Registrar Pagamento | `Códigos/sequancia-registrar-pagamento.puml` |
| Sequência - Cadastrar Animal | `Códigos/sequancia-cadastrar-animal.puml` |
| Sequência - Cadastrar Serviço | `Códigos/sequancia-cadastrar-servico.puml` |
| Sequência - Cadastrar Tutor | `Códigos/sequancia-cadastrar-tutor.puml` |
| Sequência - Cancelar Agendamento | `Códigos/sequancia-cancelar-agendamento.puml` |
| Sequência - Consultar Agenda do Dia | `Códigos/sequancia-consultar-agenda-dia.puml` |
| Sequência - Consultar Histórico Animal | `Códigos/sequancia-consultar-historio-animal.puml` |
| Sequência - Controlar Estoque | `Códigos/sequancia-controlar-estoque.puml` |
| Sequência - Emitir Orçamento | `Códigos/sequancia-emitir-orcamento.puml` |
| Sequência - Emitir Prontuário | `Códigos/sequancia-emitir-protuario.puml` |
| Sequência - Enviar Notificação | `Códigos/sequancia-enviar-notificacao.puml` |
| Sequência - Gerar Relatório Financeiro | `Códigos/sequancia-gerar-relatorio-financeiro.puml` |
| Sequência - Gerenciar Usuários | `Códigos/sequancia-gerenciar-usuarios.puml` |
| Sequência - Prescrever Medicamentos | `Códigos/sequancia-preescrever-medicamentos.puml` |
| Sequência - Registrar Alta | `Códigos/sequancia-registrar-alta-animal.puml` |
| Sequência - Registrar Internação | `Códigos/sequancia-registrar-internacao.puml` |
| Sequência - Registrar Resultado de Exame | `Códigos/sequancia-registrar-resultado-exame.puml` |
| Sequência - Registrar Vacinação | `Códigos/sequancia-registrar-vacinacao.puml` |
| Sequência - Registrar Venda de Produto | `Códigos/sequancia-registrar-venda-produto.puml` |
| Sequência - Solicitar Exame | `Códigos/sequancia-solicitar-exame.puml` |

---

## 🗄 Modelos de Dados

O modelo de dados apresenta os esquemas propostos para o banco PostgreSQL. As entidades serão mapeadas via Spring Data JPA/Hibernate.

| Tabela | Descrição |
|---|---|
| `usuarios` | Usuários do sistema (recepcionistas, veterinários e administradores) |
| `tutores` | Proprietários dos animais |
| `animais` | Animais cadastrados vinculados a tutores |
| `servicos` | Serviços e procedimentos oferecidos pela clínica |
| `agendamentos` | Agendamentos de consultas com data, hora e status |
| `consultas` | Dados clínicos das consultas realizadas |
| `prescricoes` | Prescrições médicas vinculadas a consultas |
| `exames` | Solicitações e resultados de exames |
| `vacinacoes` | Registro de vacinas aplicadas e datas de reforço |
| `internacoes` | Internações com motivo, status e data de alta |
| `medicamentos` | Estoque de medicamentos e insumos da clínica |
| `orcamentos` | Orçamentos emitidos para tutores |
| `itens_orcamento` | Itens vinculados a cada orçamento |
| `pagamentos` | Registro de pagamentos processados |
| `notas_fiscais` | Notas fiscais emitidas após confirmação de pagamento |

---

## 📁 Estrutura de Pastas

```text
VetCareSystem-ProjetoSoftware/
│
├── README.md
│
├── Docs/
│   └── VetCareSytem-documentação_do_projeto.docx
│
├── Códigos/
│   ├── caso-de-uso.puml
│   ├── diagram-classes.puml
│   ├── componentes.puml
│   ├── implantacao.puml
│   ├── comunicação-agendar-consulta.puml
│   ├── estados-agendamentos.puml
│   ├── estados-pagamentos.puml
│   └── sequancia-*.puml
│
└── Diagramas/
    ├── caso-de-uso.png
    ├── diagram-classes.png
    ├── componentes.png
    ├── implantacao.png
    ├── comunicacao.png
    ├── estados-agendamentos.png
    ├── estados-pagamentos.png
    └── sequancia-*.png
```

---

## 🧪 Testes

Como este projeto não possui implementação de código, os testes foram planejados de forma conceitual, considerando os principais fluxos do sistema.

| Tipo de Teste | Objetivo |
|---|---|
| Teste de Cadastro de Tutor e Animal | Verificar se os dados obrigatórios são registrados corretamente. |
| Teste de Agendamento | Verificar se o agendamento bloqueia o horário do veterinário e envia notificação. |
| Teste de Registro de Consulta | Verificar se a consulta gera entrada no prontuário e atualiza o status do agendamento. |
| Teste de Prescrição | Verificar se a prescrição é vinculada corretamente à consulta. |
| Teste de Vacinação | Verificar se a vacina registra a data de reforço corretamente. |
| Teste de Pagamento via Stripe | Verificar se o pagamento é processado e gera nota fiscal. |
| Teste de Notificação | Verificar se o lembrete é enviado corretamente via SendGrid. |
| Teste de Estoque | Verificar se o estoque é atualizado após venda ou uso de medicamento. |

---

## 📚 Documentações Utilizadas

- [PlantUML](https://plantuml.com/) — ferramenta utilizada para modelagem dos diagramas UML.
- [React](https://react.dev/) — tecnologia proposta para o front-end.
- [Spring Boot](https://spring.io/projects/spring-boot) — tecnologia proposta para o back-end.
- [PostgreSQL](https://www.postgresql.org/) — banco de dados proposto para persistência.
- [Stripe](https://stripe.com/br) — plataforma de pagamentos integrada ao sistema.
- [SendGrid](https://sendgrid.com/) — serviço de e-mail transacional para notificações.
- [Supabase](https://supabase.com/) — plataforma de banco PostgreSQL em nuvem.
- [Railway](https://railway.app/) — plataforma de deploy do back-end.
- [Vercel](https://vercel.com/) — plataforma de deploy do front-end.

---

## 👤 Autores

| Nome | Função |
|---|---|
| Luiz Gustavo Fagundes Teixeira | Elaboração do projeto, documentação e diagramas UML |

---

## 🤝 Contribuição

Este projeto foi desenvolvido como atividade individual da disciplina de Projeto de Software.

Não há fluxo de contribuição externa previsto para esta versão.

---

## 📄 Licença

Este projeto possui finalidade acadêmica.

Todos os direitos reservados ao autor.