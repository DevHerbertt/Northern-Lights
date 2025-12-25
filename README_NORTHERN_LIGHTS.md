# 📘 Plataforma Northern Lights - Documentação Completa

## 📋 Índice
- [Visão Geral](#visão-geral)
- [Funcionalidades](#funcionalidades)
- [Tecnologias](#tecnologias)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Frontend](#frontend)
- [Backend](#backend)
- [Configuração e Instalação](#configuração-e-instalação)
- [API Endpoints](#api-endpoints)
- [Sistema de Autenticação](#sistema-de-autenticação)
- [Banco de Dados](#banco-de-dados)

---

## 🎯 Visão Geral

A **Plataforma Northern Lights** é um sistema completo de gestão educacional que auxilia professores no gerenciamento de atividades, questões, provas e estudantes, enquanto oferece aos alunos acesso a aulas, questões, correções e ferramentas de apoio ao aprendizado.

---

## 🚀 Funcionalidades

### 👩‍🏫 Para Professores

#### Gerenciamento de Questões
- **Criar questões** com:
  - Imagens anexadas
  - Múltipla escolha (com múltiplas opções)
  - Resposta em texto livre
  - Diferentes tipos de questões (QuestionType enum)
- **Editar e excluir questões**
- **Visualizar todas as questões criadas**
- **Importar/Exportar questões via CSV**

#### Gerenciamento de Provas
- **Criar provas** associando questões existentes
- **Visualizar provas criadas**
- **Gerenciar provas e suas questões**

#### Correção de Atividades
- **Visualizar respostas dos alunos**
- **Corrigir atividades manualmente**
- **Sistema de correção automática** (via AutoCorrectionScheduler)
- **Atribuir notas** (Grade enum: A+, A, A-, B+, B, B-, C+, C, C-, D+, D, F)
- **Visualizar feedback das correções**

#### Gerenciamento de Alunos
- **Visualizar lista completa de alunos**
- **Ver detalhes de cada aluno**:
  - Perfil completo
  - Todas as notas de lições (WeeklyGrade)
  - Todas as notas de provas (ExamGrade)
  - Gráficos de evolução das notas
  - Médias separadas (atividades e provas)
- **Criar novos alunos**
- **Receber notificações** quando um novo estudante é criado
- **Visualizar estatísticas** (número de estudantes cadastrados)

#### Gerenciamento de Professores
- **Criar novos professores** com:
  - **Senha aleatória gerada automaticamente**
  - Senha enviada por **e-mail**
  - Obrigatoriedade de **alterar a senha no primeiro login**
- **Visualizar número de professores** cadastrados
- **Gerenciar permissões e acessos**

#### Aulas e Gravações
- **Criar aulas ao vivo** (Meets) com:
  - Link do Google Meet
  - Data e hora agendadas
  - Envio de e-mail automático para alunos
- **Gerenciar galeria de aulas gravadas**:
  - Adicionar aulas gravadas
  - Editar informações das aulas
  - Excluir aulas
  - Suporte para vídeos do YouTube e links externos

#### Sistema de Notas
- **Atribuir notas semanais** (WeeklyGrade) para atividades
- **Atribuir notas de provas** (ExamGrade)
- **Exportar notas para CSV**
- **Visualizar progresso dos alunos**

---

### 👨‍🎓 Para Estudantes

#### Autenticação e Perfil
- **Registrar-se** na plataforma
- **Fazer login** com credenciais
- **Editar perfil**:
  - Foto de perfil
  - Informações pessoais
  - Nível de inglês (LevelEnglish enum)

#### Questões e Atividades
- **Visualizar questões** criadas pelos professores
- **Responder questões**:
  - Questões de múltipla escolha
  - Questões de texto livre
  - Upload de imagens nas respostas
- **Usar tradução nas questões**, dependendo do **nível de inglês** configurado
- **Visualizar status das respostas** (pendente, corrigida, etc.)

#### Aulas
- **Visualizar aulas ao vivo** (Meets) agendadas
- **Assistir aulas gravadas** na galeria:
  - Vídeos do YouTube (embed automático)
  - Links externos
  - Filtro por data

#### Notas e Desempenho
- **Visualizar notas de lições** (WeeklyGrade)
- **Visualizar notas de provas** (ExamGrade)
- **Ver feedback das correções**
- **Acompanhar progresso acadêmico**

#### Estatísticas
- **Ver número total de estudantes** da plataforma
- **Visualizar estatísticas pessoais**

---

## 🛠️ Tecnologias

### Frontend
- **JavaScript (ES6+)** - Linguagem principal
- **HTML5** - Estrutura
- **CSS3** - Estilização (com variáveis CSS e gradientes)
- **Font Awesome 6.4.0** - Ícones
- **Chart.js** - Gráficos e visualizações de dados
- **Fetch API** - Comunicação com backend
- **LocalStorage** - Armazenamento de tokens JWT

### Backend
- **Java 21** - Linguagem principal
- **Spring Boot 3.5.4** - Framework principal
- **Spring Security** - Autenticação e autorização
- **Spring Data JPA** - Persistência de dados
- **JWT (JSON Web Tokens)** - Autenticação stateless
  - Biblioteca: `jjwt` versão 0.11.5
- **MapStruct 1.6.2** - Mapeamento de objetos (DTOs)
- **Lombok 1.18.30** - Redução de boilerplate
- **Spring Mail** - Envio de e-mails
- **MySQL Connector** - Driver do banco de dados
- **Spring Boot DevTools** - Desenvolvimento

### Banco de Dados
- **MySQL** - Banco de dados relacional

### Infraestrutura
- **Maven** - Gerenciamento de dependências e build
- **Docker** (docker-compose.yml) - Containerização (opcional)

---

## 📂 Estrutura do Projeto

### Frontend (`NORTHERN LIGHTS-FrontEND/`)

```
NORTHERN LIGHTS-FrontEND/
├── components/          # Componentes HTML reutilizáveis
│   ├── profile-modal.html
│   └── help-modal.html
├── css/                 # Estilos CSS
│   ├── teacher-dashboard.css
│   └── ...
├── js/                  # Scripts JavaScript
│   ├── auth-service.js
│   ├── classroom-manager.js
│   ├── students-manager.js
│   ├── questions-manager.js
│   ├── mobile-navbar.js
│   └── ...
├── page/                # Páginas HTML
│   ├── teacher-dashboard.html
│   ├── student-dashboard.html
│   ├── DashBoardTeacher-Nav/
│   │   ├── Students.html
│   │   ├── Questions.html
│   │   ├── ClassRoom.html
│   │   └── Corrections.html
│   └── ...
└── README.md
```

### Backend (`NORTHERN LIGHTS/demo/`)

```
NORTHERN LIGHTS/demo/
├── src/
│   ├── main/
│   │   ├── java/com/NorthrnLights/demo/
│   │   │   ├── config/              # Configurações
│   │   │   ├── controller/           # Controllers REST
│   │   │   │   ├── AuthController.java
│   │   │   │   ├── QuestionController.java
│   │   │   │   ├── StudentController.java
│   │   │   │   ├── TeacherController.java
│   │   │   │   ├── ExamController.java
│   │   │   │   ├── AnswerController.java
│   │   │   │   ├── CorrectionController.java
│   │   │   │   ├── WeeklyGradeController.java
│   │   │   │   ├── ExamGradeController.java
│   │   │   │   ├── MeetController.java
│   │   │   │   ├── RecordedClassController.java
│   │   │   │   ├── CsvExportController.java
│   │   │   │   └── ...
│   │   │   ├── domain/               # Entidades JPA
│   │   │   │   ├── User.java
│   │   │   │   ├── Student.java
│   │   │   │   ├── Teacher.java
│   │   │   │   ├── Question.java
│   │   │   │   ├── Answer.java
│   │   │   │   ├── Exam.java
│   │   │   │   ├── WeeklyGrade.java
│   │   │   │   ├── ExamGrade.java
│   │   │   │   ├── Meet.java
│   │   │   │   ├── RecordedClass.java
│   │   │   │   └── ...
│   │   │   ├── dto/                  # Data Transfer Objects
│   │   │   │   ├── AuthLogin.java
│   │   │   │   ├── AuthRegister.java
│   │   │   │   ├── QuestionDTO.java
│   │   │   │   ├── StudentDTO.java
│   │   │   │   └── ...
│   │   │   ├── repository/           # Repositórios JPA
│   │   │   │   ├── UserRepository.java
│   │   │   │   ├── StudentRepository.java
│   │   │   │   ├── QuestionRepository.java
│   │   │   │   └── ...
│   │   │   ├── service/              # Lógica de negócio
│   │   │   │   ├── AuthService.java
│   │   │   │   ├── QuestionService.java
│   │   │   │   ├── StudentService.java
│   │   │   │   └── ...
│   │   │   ├── security/             # Configuração de segurança
│   │   │   │   ├── SecurityConfig.java
│   │   │   │   └── JwtFilter.java
│   │   │   ├── util/                 # Utilitários
│   │   │   │   ├── JwtService.java
│   │   │   │   ├── EmailService.java
│   │   │   │   ├── AutoCorrectionScheduler.java
│   │   │   │   └── ...
│   │   │   └── NorthernLightsApplication.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── application-secret.properties
│   └── test/                          # Testes
├── pom.xml                            # Configuração Maven
└── docker-compose.yml                 # Configuração Docker
```

---

## 🔧 Configuração e Instalação

### Pré-requisitos

#### Frontend
- Navegador moderno (Chrome, Firefox, Edge, Safari)
- Servidor web (opcional, pode abrir HTML diretamente)

#### Backend
- **Java 21** ou superior
- **Maven 3.6+**
- **MySQL 8.0+** ou superior
- **IDE** (IntelliJ IDEA, Eclipse, VS Code) - recomendado

### Configuração do Backend

1. **Clone o repositório** (se aplicável)

2. **Configure o banco de dados MySQL**:
   - Crie um banco de dados chamado `northern_lights` (ou o nome de sua preferência)
   - Configure as credenciais no arquivo `application-secret.properties`

3. **Configure o arquivo `application-secret.properties`**:
   ```properties
   # Banco de Dados
   spring.datasource.url=jdbc:mysql://localhost:3306/northern_lights?createDatabaseIfNotExist=true&useSSL=false&serverTimezone=America/Sao_Paulo
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   
   # JWT
   jwt.secret=sua_chave_secreta_jwt_muito_segura_e_longa
   jwt.expiration=86400000
   
   # E-mail (Gmail)
   spring.mail.username=seu_email@gmail.com
   spring.mail.password=sua_senha_de_app
   ```

4. **Compile o projeto**:
   ```bash
   cd NORTHERN\ LIGHTS/demo
   mvn clean install
   ```

5. **Execute a aplicação**:
   ```bash
   mvn spring-boot:run
   ```
   
   Ou execute a classe `NorthernLightsApplication.java` diretamente no IDE.

6. **A aplicação estará rodando em**: `http://localhost:8080`

### Configuração do Frontend

1. **Abra o projeto**:
   ```bash
   cd NORTHERN\ LIGHTS-FrontEND
   ```

2. **Configure a URL da API**:
   - Edite os arquivos JavaScript que contêm a constante `API`
   - Exemplo em `auth-service.js`:
     ```javascript
     const API = 'http://localhost:8080/api';
     ```

3. **Abra as páginas HTML**:
   - Abra diretamente no navegador, ou
   - Use um servidor local (ex: Live Server no VS Code, Python HTTP Server, etc.)

---

## 📡 API Endpoints

### Autenticação
- `POST /api/auth/login` - Login (retorna JWT token)
- `POST /api/auth/register` - Registro de estudante
- `POST /api/auth/change-password` - Alterar senha (primeiro login)

### Usuários
- `GET /api/users/me` - Obter dados do usuário logado
- `PUT /api/users/me` - Atualizar perfil do usuário

### Professores
- `GET /api/teachers` - Listar todos os professores
- `POST /api/teachers` - Criar novo professor
- `GET /api/teachers/{id}` - Obter professor por ID
- `PUT /api/teachers/{id}` - Atualizar professor
- `DELETE /api/teachers/{id}` - Excluir professor

### Estudantes
- `GET /api/students` - Listar todos os estudantes
- `POST /api/students` - Criar novo estudante
- `GET /api/students/{id}` - Obter estudante por ID
- `PUT /api/students/{id}` - Atualizar estudante
- `DELETE /api/students/{id}` - Excluir estudante
- `GET /api/students/profile` - Obter perfil do estudante logado

### Questões
- `GET /api/questions` - Listar todas as questões
- `POST /api/questions` - Criar nova questão
- `GET /api/questions/{id}` - Obter questão por ID
- `PUT /api/questions/{id}` - Atualizar questão
- `DELETE /api/questions/{id}` - Excluir questão
- `POST /api/questions/batch` - Criar múltiplas questões

### Provas
- `GET /api/exams` - Listar todas as provas
- `POST /api/exams` - Criar nova prova
- `GET /api/exams/{id}` - Obter prova por ID
- `PUT /api/exams/{id}` - Atualizar prova
- `DELETE /api/exams/{id}` - Excluir prova

### Respostas
- `GET /api/answers` - Listar todas as respostas
- `POST /api/answers` - Criar nova resposta
- `GET /api/answers/{id}` - Obter resposta por ID
- `GET /api/answers/student/{studentId}` - Respostas de um estudante
- `GET /api/answers/question/{questionId}` - Respostas de uma questão

### Correções
- `GET /api/corrections` - Listar todas as correções
- `POST /api/corrections` - Criar nova correção
- `GET /api/corrections/{id}` - Obter correção por ID
- `PUT /api/corrections/{id}` - Atualizar correção
- `GET /api/corrections/answer/{answerId}` - Correção de uma resposta

### Notas Semanais (WeeklyGrade)
- `GET /api/weekly-grades` - Listar todas as notas semanais
- `POST /api/weekly-grades` - Criar nova nota semanal
- `GET /api/weekly-grades/student/{studentId}` - Notas semanais de um estudante

### Notas de Provas (ExamGrade)
- `GET /api/exam-grades` - Listar todas as notas de provas
- `POST /api/exam-grades` - Criar nova nota de prova
- `GET /api/exam-grades/student/{studentId}` - Notas de provas de um estudante

### Aulas ao Vivo (Meets)
- `GET /api/meets` - Listar todas as aulas
- `POST /api/meets` - Criar nova aula
- `GET /api/meets/{id}` - Obter aula por ID
- `PUT /api/meets/{id}` - Atualizar aula
- `DELETE /api/meets/{id}` - Excluir aula
- `POST /api/meets/{id}/send-email` - Enviar e-mail da aula

### Aulas Gravadas (RecordedClass)
- `GET /api/recorded-classes` - Listar todas as aulas gravadas (estudantes)
- `GET /api/recorded-classes/teacher` - Listar aulas gravadas do professor
- `POST /api/recorded-classes` - Criar nova aula gravada
- `GET /api/recorded-classes/{id}` - Obter aula gravada por ID
- `PUT /api/recorded-classes/{id}` - Atualizar aula gravada
- `DELETE /api/recorded-classes/{id}` - Excluir aula gravada

### Exportação/Importação CSV
- `POST /api/csv/import/questions` - Importar questões via CSV
- `GET /api/csv/export/grades` - Exportar notas para CSV

### Upload de Arquivos
- `POST /api/files/upload` - Upload de arquivos (imagens, etc.)
- `GET /api/files/{filename}` - Obter arquivo

---

## 🔐 Sistema de Autenticação

### JWT (JSON Web Tokens)

O sistema utiliza **JWT** para autenticação stateless:

1. **Login**: O usuário faz login e recebe um token JWT
2. **Armazenamento**: O token é armazenado no `localStorage` do navegador
3. **Requisições**: Todas as requisições autenticadas incluem o header:
   ```
   Authorization: Bearer <token>
   ```
4. **Validação**: O backend valida o token em cada requisição via `JwtFilter`

### Roles (Papéis)

- **STUDENT** - Estudante
- **TEACHER** - Professor
- **ADMIN** - Administrador (se implementado)

### Segurança

- Tokens JWT com expiração configurável
- Senhas hasheadas (BCrypt)
- Proteção CSRF (Spring Security)
- Validação de entrada (Bean Validation)
- CORS configurado para frontend

---

## 💾 Banco de Dados

### Principais Entidades

#### User
- Tabela base para todos os usuários (estudantes e professores)
- Campos: id, email, password, role, etc.

#### Student
- Extensão de User
- Campos específicos: levelEnglish, status, etc.

#### Teacher
- Extensão de User
- Campos específicos: department, etc.

#### Question
- Questões criadas pelos professores
- Relacionamentos: QuestionOption, Exam

#### Answer
- Respostas dos estudantes
- Relacionamentos: Student, Question, Correction

#### Exam
- Provas criadas pelos professores
- Relacionamentos: Question (muitas questões)

#### WeeklyGrade
- Notas semanais de atividades
- Relacionamentos: Student

#### ExamGrade
- Notas de provas
- Relacionamentos: Student, Exam

#### Meet
- Aulas ao vivo agendadas
- Campos: link, dateTime, etc.

#### RecordedClass
- Aulas gravadas
- Campos: title, description, videoUrl, classDate

### Relacionamentos Principais

- **User** → **Student** / **Teacher** (herança)
- **Question** → **QuestionOption** (1:N)
- **Exam** → **Question** (N:M)
- **Student** → **Answer** (1:N)
- **Answer** → **Correction** (1:1)
- **Student** → **WeeklyGrade** (1:N)
- **Student** → **ExamGrade** (1:N)
- **Exam** → **ExamGrade** (1:N)

---

## 📢 Sistema de Notificações

### E-mail

O sistema envia e-mails automáticos para:

1. **Criação de Professor**:
   - Senha aleatória gerada
   - Instruções para primeiro login
   - Link para alterar senha

2. **Criação de Aluno**:
   - Notificação para o professor responsável

3. **Aulas ao Vivo**:
   - E-mail para alunos com link do Google Meet
   - Data e hora da aula

### Configuração de E-mail

Configure no `application-secret.properties`:
```properties
spring.mail.username=seu_email@gmail.com
spring.mail.password=sua_senha_de_app
```

**Nota**: Para Gmail, é necessário usar uma "Senha de App" em vez da senha normal.

---

## 🎨 Interface do Usuário

### Design
- **Tema escuro** com gradientes modernos
- **Responsivo** - Funciona em desktop, tablet e mobile
- **Navbar mobile** - Menu hambúrguer para dispositivos móveis
- **Animações suaves** - Transições e efeitos visuais
- **Cores principais**:
  - Azul (#3b82f6) - Primária
  - Teal (#14b8a6) - Secundária
  - Amarelo (#fbbf24) - Destaque

### Componentes Principais

- **Dashboard** - Visão geral com estatísticas
- **Sidebar** - Navegação principal
- **Modais** - Perfil, ajuda, confirmações
- **Tabelas** - Listagens de dados
- **Gráficos** - Visualização de notas (Chart.js)
- **Formulários** - Criação e edição de dados

---

## 🚀 Funcionalidades Avançadas

### Correção Automática
- Sistema de correção automática via `AutoCorrectionScheduler`
- Compara respostas com gabaritos
- Atribui notas automaticamente quando possível

### Importação/Exportação CSV
- Importar questões em lote via CSV
- Exportar notas para análise externa

### Upload de Arquivos
- Upload de imagens para questões
- Upload de imagens para respostas
- Upload de fotos de perfil
- Armazenamento em `uploads/`

### Tradução de Questões
- Baseada no nível de inglês do estudante (LevelEnglish)
- Suporte para diferentes níveis: BEGINNER, INTERMEDIATE, ADVANCED, FLUENT

---

## 📝 Notas de Desenvolvimento

### Padrões Utilizados

- **RESTful API** - Endpoints seguindo padrões REST
- **DTO Pattern** - Separação entre entidades e DTOs
- **Service Layer** - Lógica de negócio isolada
- **Repository Pattern** - Abstração de acesso a dados
- **JWT Authentication** - Autenticação stateless
- **CORS** - Configurado para permitir requisições do frontend

### Boas Práticas

- Validação de entrada (Bean Validation)
- Tratamento de exceções global (GlobalExceptionHandler)
- Logging adequado
- Código limpo e documentado
- Separação de responsabilidades

---

## 🔄 Próximos Passos / Melhorias Futuras

- [ ] Testes automatizados (JUnit, Mockito)
- [ ] Documentação da API (Swagger/OpenAPI)
- [ ] Cache de dados frequentes
- [ ] Paginação em listagens grandes
- [ ] Filtros e busca avançada
- [ ] Notificações em tempo real (WebSocket)
- [ ] Dashboard com mais métricas
- [ ] Relatórios em PDF
- [ ] Integração com mais plataformas de vídeo
- [ ] App mobile (React Native / Flutter)

---

## 📞 Suporte

Para dúvidas ou problemas:
1. Verifique a documentação
2. Consulte os logs da aplicação
3. Verifique a configuração do banco de dados
4. Verifique as credenciais de e-mail

---

## 📄 Licença

Este projeto é de uso educacional.

---

**Desenvolvido com ❤️ para facilitar o aprendizado e ensino**

---

*Última atualização: Janeiro 2025*


