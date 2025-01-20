# Desafio do Fórum Hub: Construindo o seu próprio Fórum Alura

## Objetivo
Este repositório é dedicado à construção de uma aplicação de fórum inspirada no Fórum da Alura, onde usuários podem criar, listar, atualizar e deletar tópicos. O projeto tem como objetivo consolidar conhecimentos em desenvolvimento backend com Java e Spring Framework.

---

## Passo a Passo para Construção do Projeto

### 1. **Compreensão do Desafio**
Antes de iniciar o desenvolvimento, é importante entender as regras de negócio:
- O fórum permite a troca de conhecimentos entre usuários.
- Tópicos devem possuir:
  - Um título.
  - Uma mensagem.
  - A referência a um curso específico.
  - A data de criação gerada automaticamente pelo servidor.

### 2. **Configuração do Ambiente**
Certifique-se de que o ambiente de desenvolvimento esteja configurado corretamente:
- **Java 17+**: Certifique-se de que a versão do Java esteja instalada e configurada.
- **Spring Framework**: Utilize o Spring Boot para simplificar a criação do projeto.
- **Insomnia**: Ferramenta para testar as requisições da API.

### 3. **Autenticação**
Implemente um sistema de autenticação com Bearer Token:
- Somente usuários logados podem criar, atualizar ou deletar tópicos.
- Utilize o Spring Security para configurar a autenticação e geração de tokens JWT.

### 4. **Funcionalidades Principais**
#### **4.1. Criação de Tópicos**
- Endpoint: `POST /topicos`
- Corpo da requisição (JSON):
  ```json
  {
      "titulo": "Dúvida sobre Spring Boot",
      "mensagem": "Como configuro o Spring Security?",
      "curso": "Spring Framework"
  }
  ```
- A data de criação deve ser gerada automaticamente no servidor.

#### **4.2. Listagem de Tópicos**
- Endpoint: `GET /topicos`
- Retorna uma lista de todos os tópicos cadastrados no banco de dados.

#### **4.3. Atualização de Tópicos**
- Endpoint: `PUT /topicos/{id}`
- Apenas o autor do tópico pode atualizá-lo.
- Corpo da requisição (JSON):
  ```json
  {
      "titulo": "Novo título",
      "mensagem": "Mensagem atualizada"
  }
  ```

#### **4.4. Deleção de Tópicos**
- Endpoint: `DELETE /topicos/{id}`
- Apenas o autor do tópico pode deletá-lo.

### 5. **Testes com Insomnia**
- Teste cada funcionalidade da API:
  - **POST /topicos**: Criar novos tópicos.
  - **GET /topicos**: Listar todos os tópicos.
  - **PUT /topicos/{id}**: Atualizar tópicos existentes.
  - **DELETE /topicos/{id}**: Remover tópicos.
- Verifique se as regras de autenticação estão sendo respeitadas.

## Tecnologias Utilizadas
- **Java 17+**
- **Spring Boot**
- **JWT (JSON Web Token)**
- **Banco de Dados**: H2 ou MySQL
- **Insomnia** para testes de API

---



