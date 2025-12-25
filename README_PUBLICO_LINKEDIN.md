# 🚀 Northern Lights - Plataforma Educacional Completa

<div align="center">

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.4-brightgreen?style=for-the-badge&logo=spring&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?style=for-the-badge&logo=javascript&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-blue?style=for-the-badge&logo=mysql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-Auth-black?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

**Sistema completo de gestão educacional desenvolvido com tecnologias modernas**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/seu-perfil)

</div>

---

## 📋 Sobre o Projeto

**Northern Lights** é uma plataforma educacional completa que revoluciona a gestão acadêmica, conectando professores e estudantes em um ambiente digital moderno e intuitivo. O sistema foi desenvolvido do zero, utilizando as melhores práticas de desenvolvimento de software e arquitetura de sistemas.

### 🎯 Objetivo

Criar uma solução completa que facilite:
- **Para Professores**: Gerenciamento centralizado de questões, provas, correções e alunos
- **Para Estudantes**: Acesso fácil a aulas, questões, notas e acompanhamento do progresso acadêmico

---

## ✨ Principais Funcionalidades

### 👩‍🏫 Módulo Professor

#### 📝 Gerenciamento de Questões
- ✅ Criação de questões com múltiplos tipos (múltipla escolha, texto livre)
- ✅ Upload de imagens para questões
- ✅ Sistema de tradução automática baseado no nível de inglês do aluno
- ✅ Importação/Exportação em lote via CSV
- ✅ Edição e exclusão de questões

#### 📊 Sistema de Provas
- ✅ Criação de provas associando questões existentes
- ✅ Gerenciamento completo de provas e questões
- ✅ Visualização de estatísticas

#### ✅ Correção Inteligente
- ✅ Sistema de correção automática de questões
- ✅ Correção manual com feedback detalhado
- ✅ Atribuição de notas (sistema de letras: A+ a F)
- ✅ Visualização de todas as respostas dos alunos

#### 👥 Gerenciamento de Alunos
- ✅ Dashboard completo com visualização de todos os alunos
- ✅ **Visualização detalhada de desempenho**:
  - Gráficos de evolução das notas (Chart.js)
  - Médias separadas para atividades e provas
  - Histórico completo de notas
  - Análise de progresso acadêmico
- ✅ Criação e gerenciamento de alunos
- ✅ Sistema de notificações automáticas

#### 🎓 Aulas e Conteúdo
- ✅ **Aulas ao Vivo**: Criação e agendamento com Google Meet
- ✅ **Galeria de Aulas Gravadas**: 
  - Upload e gerenciamento de vídeos
  - Suporte para YouTube e links externos
  - Interface moderna e responsiva
- ✅ Envio automático de e-mails para alunos

#### 📈 Sistema de Notas
- ✅ Notas semanais (WeeklyGrade) para atividades
- ✅ Notas de provas (ExamGrade)
- ✅ Exportação de notas para CSV
- ✅ Relatórios e análises

---

### 👨‍🎓 Módulo Estudante

#### 🎯 Interface do Aluno
- ✅ Dashboard personalizado com estatísticas
- ✅ Visualização de questões disponíveis
- ✅ Sistema de respostas com upload de imagens
- ✅ Tradução automática baseada no nível de inglês

#### 📚 Aulas
- ✅ Visualização de aulas ao vivo agendadas
- ✅ Galeria de aulas gravadas com player integrado
- ✅ Filtros e busca

#### 📊 Acompanhamento Acadêmico
- ✅ Visualização de todas as notas
- ✅ Feedback detalhado das correções
- ✅ Histórico completo de atividades
- ✅ Gráficos de progresso

#### 👤 Perfil
- ✅ Edição completa de perfil
- ✅ Upload de foto de perfil
- ✅ Configuração de nível de inglês
- ✅ Estatísticas pessoais

---

## 🛠️ Stack Tecnológica

### Backend
<div align="center">

| Tecnologia | Versão | Uso |
|------------|--------|-----|
| **Java** | 21 | Linguagem principal |
| **Spring Boot** | 3.5.4 | Framework principal |
| **Spring Security** | - | Autenticação e autorização |
| **Spring Data JPA** | - | Persistência de dados |
| **JWT** | 0.11.5 | Autenticação stateless |
| **MapStruct** | 1.6.2 | Mapeamento de objetos |
| **Lombok** | 1.18.30 | Redução de boilerplate |
| **Spring Mail** | - | Envio de e-mails |
| **MySQL** | 8.0+ | Banco de dados |

</div>

### Frontend
<div align="center">

| Tecnologia | Uso |
|----------|-----|
| **JavaScript (ES6+)** | Lógica e interatividade |
| **HTML5** | Estrutura semântica |
| **CSS3** | Estilização moderna |
| **Chart.js** | Gráficos e visualizações |
| **Font Awesome** | Ícones |
| **Fetch API** | Comunicação com backend |

</div>

### Arquitetura e Padrões
- ✅ **RESTful API** - Endpoints seguindo padrões REST
- ✅ **DTO Pattern** - Separação entre entidades e DTOs
- ✅ **Service Layer** - Lógica de negócio isolada
- ✅ **Repository Pattern** - Abstração de acesso a dados
- ✅ **JWT Authentication** - Autenticação stateless e segura
- ✅ **Responsive Design** - Interface adaptável para mobile, tablet e desktop

---

## 🏗️ Arquitetura do Sistema

### Backend (Spring Boot)
```
📦 Arquitetura em Camadas
├── 🎮 Controller Layer (REST APIs)
├── 💼 Service Layer (Lógica de Negócio)
├── 📊 Repository Layer (Acesso a Dados)
├── 🔐 Security Layer (Autenticação JWT)
└── 📝 Domain Layer (Entidades JPA)
```

### Frontend
```
📦 Estrutura Modular
├── 🎨 CSS (Design System)
├── ⚙️ JavaScript (Módulos ES6)
├── 📄 HTML (Páginas Responsivas)
└── 🧩 Componentes Reutilizáveis
```

### Banco de Dados
- **MySQL** com relacionamentos bem definidos
- **JPA/Hibernate** para mapeamento objeto-relacional
- **Migrations** automáticas

---

## 🎨 Interface e Design

### Características Visuais
- 🎨 **Tema escuro moderno** com gradientes
- 📱 **100% Responsivo** - Mobile First
- ⚡ **Animações suaves** e transições
- 🎯 **UX intuitiva** e fácil navegação
- 📊 **Gráficos interativos** (Chart.js)

### Componentes Principais
- Dashboard com estatísticas em tempo real
- Sidebar de navegação responsiva
- Modais para ações rápidas
- Tabelas com filtros e busca
- Formulários com validação
- Sistema de notificações

---

## 🔐 Segurança

### Implementações de Segurança
- ✅ **JWT (JSON Web Tokens)** para autenticação stateless
- ✅ **Spring Security** com configuração customizada
- ✅ **BCrypt** para hash de senhas
- ✅ **CORS** configurado adequadamente
- ✅ **Validação de entrada** em todos os endpoints
- ✅ **Proteção CSRF**
- ✅ **Roles e permissões** (STUDENT, TEACHER)

---

## 📊 Funcionalidades Técnicas Avançadas

### 🔄 Sistema de Correção Automática
- Algoritmo de correção automática de questões
- Comparação inteligente de respostas
- Atribuição automática de notas

### 📧 Sistema de E-mails
- Envio assíncrono de e-mails
- Templates HTML para e-mails
- Notificações automáticas

### 📤 Upload e Gerenciamento de Arquivos
- Upload de imagens para questões
- Upload de imagens para respostas
- Upload de fotos de perfil
- Armazenamento organizado

### 📈 Análise e Relatórios
- Gráficos de evolução de notas
- Cálculo de médias automático
- Exportação para CSV
- Estatísticas em tempo real

### 🌐 Internacionalização
- Sistema de tradução baseado em nível de inglês
- Suporte para múltiplos idiomas
- Interface adaptável

---

## 📈 Métricas e Resultados

### Escalabilidade
- ✅ Suporta múltiplos professores e alunos
- ✅ Sistema de roles e permissões
- ✅ Arquitetura preparada para crescimento

### Performance
- ✅ Queries otimizadas com JPA
- ✅ Lazy loading onde apropriado
- ✅ Cache de dados frequentes
- ✅ Requisições assíncronas para e-mails

### Qualidade de Código
- ✅ Código limpo e bem documentado
- ✅ Separação de responsabilidades
- ✅ Tratamento de exceções global
- ✅ Logging adequado
- ✅ Validação de entrada

---

## 🎓 Aprendizados e Desafios

### Desafios Superados
1. **Autenticação JWT**: Implementação completa de sistema de autenticação stateless
2. **Correção Automática**: Desenvolvimento de algoritmo inteligente de correção
3. **Upload de Arquivos**: Sistema robusto de gerenciamento de arquivos
4. **Gráficos e Visualizações**: Integração com Chart.js para análise de dados
5. **Responsividade**: Interface totalmente adaptável para todos os dispositivos
6. **Sistema de Notas**: Lógica complexa de cálculo e armazenamento de notas

### Tecnologias Dominadas
- ✅ Spring Boot e Spring Ecosystem
- ✅ JWT e autenticação segura
- ✅ RESTful API Design
- ✅ JPA/Hibernate
- ✅ JavaScript ES6+ e módulos
- ✅ CSS3 avançado e responsividade
- ✅ Integração de bibliotecas (Chart.js)
- ✅ Gerenciamento de estado no frontend

---

## 🚀 Destaques do Projeto

### ✨ O que torna este projeto especial:

1. **Sistema Completo**: Do backend ao frontend, tudo desenvolvido do zero
2. **Arquitetura Robusta**: Padrões de design e boas práticas aplicadas
3. **Interface Moderna**: Design atual e experiência de usuário excelente
4. **Segurança**: Implementação completa de autenticação e autorização
5. **Escalável**: Preparado para crescer e adicionar novas funcionalidades
6. **Bem Documentado**: Código limpo e documentação completa

---

## 📸 Demonstração

### Funcionalidades em Destaque

#### Dashboard do Professor
- Visão geral completa do sistema
- Estatísticas em tempo real
- Acesso rápido a todas as funcionalidades

#### Gerenciamento de Alunos
- Visualização detalhada de desempenho
- Gráficos de evolução das notas
- Análise completa do progresso acadêmico

#### Galeria de Aulas
- Interface moderna para aulas gravadas
- Suporte para YouTube e links externos
- Player integrado

#### Sistema de Questões
- Criação intuitiva de questões
- Upload de imagens
- Sistema de tradução automática

---

## 🎯 Próximos Passos e Melhorias Futuras

- [ ] Testes automatizados (JUnit, Mockito)
- [ ] Documentação da API (Swagger/OpenAPI)
- [ ] Cache Redis para melhor performance
- [ ] Paginação em listagens grandes
- [ ] Notificações em tempo real (WebSocket)
- [ ] Dashboard com mais métricas e analytics
- [ ] Relatórios em PDF
- [ ] App mobile (React Native / Flutter)

---

## 💼 Casos de Uso

Este sistema pode ser utilizado por:
- 🏫 **Escolas e Instituições de Ensino**
- 🎓 **Cursos Online**
- 📚 **Plataformas EAD**
- 👨‍🏫 **Professores Particulares**
- 🏢 **Empresas de Treinamento**

---

## 🛠️ Ferramentas e Bibliotecas Utilizadas

### Backend
- Maven (Gerenciamento de dependências)
- Spring Boot DevTools
- Lombok (Redução de boilerplate)
- MapStruct (Mapeamento de objetos)

### Frontend
- Chart.js (Gráficos)
- Font Awesome (Ícones)
- Fetch API (Requisições HTTP)

### Desenvolvimento
- Git (Controle de versão)
- IDE: IntelliJ IDEA / VS Code
- MySQL Workbench

---

## 📚 Conhecimentos Demonstrados

### Backend Development
- ✅ Java 21 e programação orientada a objetos
- ✅ Spring Boot e Spring Ecosystem
- ✅ RESTful API Design
- ✅ JPA/Hibernate e banco de dados relacionais
- ✅ Autenticação e autorização (JWT)
- ✅ Tratamento de exceções
- ✅ Validação de dados
- ✅ Envio de e-mails assíncrono

### Frontend Development
- ✅ JavaScript ES6+ e programação moderna
- ✅ HTML5 semântico
- ✅ CSS3 avançado (Grid, Flexbox, Animations)
- ✅ Responsive Design
- ✅ Integração de APIs REST
- ✅ Gerenciamento de estado
- ✅ Manipulação do DOM

### DevOps e Ferramentas
- ✅ Git e controle de versão
- ✅ Maven e gerenciamento de dependências
- ✅ MySQL e modelagem de banco de dados
- ✅ Debugging e troubleshooting

### Soft Skills
- ✅ Resolução de problemas complexos
- ✅ Arquitetura de sistemas
- ✅ Organização e estruturação de código
- ✅ Documentação técnica

---

## 🎓 Sobre o Desenvolvedor

Desenvolvedor Full Stack com experiência em:
- **Backend**: Java, Spring Boot, REST APIs
- **Frontend**: JavaScript, HTML5, CSS3
- **Banco de Dados**: MySQL, JPA/Hibernate
- **Autenticação**: JWT, Spring Security
- **Arquitetura**: Padrões de design, Clean Code

---

## 📞 Contato

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/seu-perfil)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/seu-usuario)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:seu-email@exemplo.com)

</div>

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais e de portfólio.

---

<div align="center">

**Desenvolvido com ❤️ e dedicação**

*Projeto desenvolvido do zero, demonstrando habilidades em desenvolvimento Full Stack*

⭐ **Se este projeto te interessou, deixe uma estrela!** ⭐

</div>

---

*Última atualização: Janeiro 2025*


