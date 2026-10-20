# ♻️ Central de Reciclagem & Créditos de Carbono

[![INPI Registrado](https://img.shields.io/badge/INPI-Registrado-0284c7.svg)](https://www.gov.br/inpi/pt-br)
[![Build Status](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions%20Passing-emerald.svg)](#)
[![Stack](https://img.shields.io/badge/Stack-Laravel%2011%20%7C%20Tailwind%20%7C%20MySQL-orange.svg)](#)
[![Ambiente de Produção](https://img.shields.io/badge/Status-Online%20em%20Produção-green.svg)](#)

---

### 🌐 Acesso Rápido à Plataforma

> **Ambiente Oficial de Homologação e Produção:**  
> 🔗 **[Acessar Plataforma Online](https://el-caminodesantiago.com.br/central_reciclagem/)**  
> *(Hospedado com banco de dados relacional e ambiente de produção ativo)*

---

## 📌 Visão Geral do Sistema
O **Central de Reciclagem** é um ecossistema digital desenvolvido para conectar ponta a ponta todos os atores da cadeia de logística reversa e economia circular: **Geradores (Cliente PF e PJ)**, **Catadores/Colaboradores**, **Cooperativas de Triagem**, **Design Thinkers (Upcycling)** e **Indústrias Recicladoras**.

A plataforma monitora a cadeia de custódia dos materiais desde o agendamento de coleta e geolocalização até a prensagem em fardos, leilão no marketplace e cálculo matemático automatizado de emissões evitadas de $CO_2$ (Créditos de Carbono).

---

## 📋 Propriedade Intelectual e Registro
Este software (*Central de Reciclagem e Créditos de Carbono*) é resultado de desenvolvimento independente e possui seus direitos de propriedade intelectual devidamente depositados e registrados junto ao **INPI (Instituto Nacional da Propriedade Industrial)**. Todos os direitos reservados.

---

## 🗺️ A Jornada de Desenvolvimento na Disciplina

Durante o semestre, o projeto foi executado sob metodologia ágil, aplicando práticas rigorosas de **Engenharia de Software**, **Gitflow**, **DevSecOps** e **Mobile-First**:

### 1. Governança e Arquitetura de Branches (Gitflow)
- **Isolamento de Escopo:** Nenhuma alteração foi aplicada diretamente na branch principal. Cada funcionalidade foi isolada em sua respectiva branch `feature/*`, vinculada a uma Issue específica no GitHub.
- **Pull Requests (PRs) Estruturados:** As integrações para a branch `dev` e posteriormente para a `main` seguiram revisões técnicas detalhadas, testes manuais e semântica de *Conventional Commits*.

### 2. Automação e Qualidade (CI/CD com GitHub Actions)
- Configuração de pipeline automatizado executado a cada `push` e `pull_request`.
- Ambiente conteinerizado que roda testes unitários e de integração com **PHPUnit**, assegurando integridade na conversão de créditos de carbono e nas regras de negócio.

### 3. Engenharia de Interfaces: PWA Mobile-First
Desenvolvimento e padronização da experiência mobile progressiva (PWA) com templates Blade, Tailwind CSS e bibliotecas de detecção (`Jenssegers/Agent`), entregando portais específicos para cada ator:
- **Cliente PF (`#14`):** Solicitação simplificada de coletas residenciais, extrato de impacto ambiental e vitrine de recompensas ecológicas.
- **Cliente PJ (`#15`):** Gestão de resíduos corporativos, relatórios ESG, máscara de privacidade para dados cadastrais e certificados de destinação.
- **Design Thinker (`#16`):** Portal de upcycling com marketplace de matéria-prima residual e catálogo de produtos reciclados.
- **Indústria Recicladora (`#17`):** Recepção de lotes industriais, bolsa de materiais e lances em fardos prensados.
- **Cooperativa (`#18`):** Triagem de coletas, prensagem de lotes e atendimento logístico com raio geográfico delimitado.
- **Olimpo Admin (`#5`):** Visão macro de liquidez da rede, métricas ambientais consolidadas e gerenciamento multi-perfis com badges cromáticos e busca em tempo real.

### 4. DevSecOps, Segurança e Conformidade (LGPD)
- Implementação de barreiras de segurança contra injeção SQL via Eloquent ORM e proteção CSRF em formulários.
- Adequação completa à LGPD: inclusão de consentimento obrigatório para **Termos de Uso** e **Política de Cookies** no fluxo de cadastro.
- Versionamento semântico auditável com tags e releases documentadas no GitHub (`v1.1.0` e `v2.0`).

---

## 🛠️ Tecnologias e Infraestrutura

- **Backend:** Laravel 11 (PHP 8.x) com arquitetura MVC.
- **Frontend:** Blade Templates, Tailwind CSS, Alpine.js e Progressive Web App (PWA).
- **Banco de Dados:** MySQL Relacional com integridade referencial e migrações versionadas.
- **Infraestrutura Local:** Docker & Docker Compose.
- **Hospedagem & Deploy:** 
  - **Portal / Showcase:** GitHub Pages (`https://martinsonfreitas.github.io/`)
  - **Servidor da Aplicação:** Hostinger Cloud (PHP + LiteSpeed + MySQL)
- **Controle de Versão:** Gitflow, GitHub Actions (CI/CD) e Releases SemVer.

---

## 👥 Atores do Sistema e Contas de Teste (Homologação)

Para avaliação dos fluxos e regras de negócio no ambiente online, utilize as credenciais de teste disponíveis nos seeders oficiais:

| Perfil | Finalidade Principal | usuário | senha |
| :--- | :--- | :--- | :--- |
| **Administrador** | Gestão de usuários, métricas globais e auditoria do ecossistema | admin@teste.com | password123 |
| **Cooperativa** | Triagem, pesagem, fardos e despacho para recicladoras | cooperativa@teste.com | password123 |
| **Recicladora** | Leilão/compra de lotes prensados de materiais | reciclador@teste.com | abcd1234 |
| **Colaborador (Coletor)** | Logística de rota, coleta em campo e validação de pesagem | colaborador@teste.com | password123 |
| **Cliente PF** | Descarte consciente, histórico e acúmulo de créditos de carbono | cliente.pf@teste.com | abcd@1234 |
| **Cliente PJ** | Descarte consciente, histórico e acúmulo de créditos de carbono | cliente.pj@teste.com | password |
| **Design Thinker** | Resgate de matéria-prima para economia circular e upcycling | design.thinker@teste.com | password |

---

*Projeto acadêmico e de extensão desenvolvido por Martinson Freitas.*
