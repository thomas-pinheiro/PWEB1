# Testes de Funcionalidades Básicas do Sistema de Autenticação - Cãodominio 🐾

Este documento descreve os testes a serem realizados nas telas de login, registro e recuperação de senha do sistema **Cãodominio**. 

## 📂 Informações do Projeto

- **GitHub:** [Repositório do Projeto](https://github.com/quallifica-tech/caodominio/tree/develop)  
- **Figma:** [Design no Figma](https://www.figma.com/design/f2A5s87LxLyVfra0bjv8RB/ONGS?node-id=331-211&m=dev)

### Credenciais de Teste

- **Conta de Teste:** 
  - E-mail: `teste@teste.com`  
  - Senha: `teste123`
- **Conta de Admin:**  
  - E-mail: `admin@admin.com`  
  - Senha: `admin123`  
  *(Cada conta deve ser configurada com uma role específica.)*

---

## 🔍 Checkpoints para Testes

### Tela de Login

#### **Caminho Feliz**
1. **Campos de Entrada:**
   - Verificar se os campos de e-mail e senha estão visíveis e acessíveis. ✅
   - Testar a entrada de dados válidos e confirmar login bem-sucedido. ⚠️

2. **Botão de Login:**
   - Garantir que o botão é habilitado após a inserção de dados válidos. ✅
   - Confirmar que o botão entra em estado de *loading* durante o processamento. ✅
   - Verificar redirecionamento correto após o login. ⚠️

3. **Responsividade:**
   - Testar em diferentes tamanhos de tela (desktop, tablet, celular). ✅
   - Garantir que campos e botões são facilmente utilizáveis em dispositivos móveis. ✅

#### **Caminho Triste**
1. **Validação de Campos:**
   - Testar com e-mail inválido e verificar mensagens de erro. ✅
   - Testar com senha incorreta e validar mensagens de erro. ⚠️

2. **Campos Vazios:**
   - Confirmar exibição de mensagens de erro ao tentar logar sem preencher os campos. ⚠️

3. **Recuperação de Senha:**
   - Garantir que o link "Esqueci a senha" é funcional e visível. ✅

---

### Tela de Registro

#### **Caminho Feliz**
1. **Campos de Entrada:**
   - Confirmar visibilidade e acessibilidade de todos os campos obrigatórios. ✅
   - Testar registro com dados válidos e confirmar sucesso. ✅

2. **Botão de Registro:**
   - Garantir que o botão é habilitado após preenchimento válido. ✅
   - Confirmar redirecionamento correto após o registro. ⚠️

3. **Responsividade:**
   - Verificar ajuste adequado da interface em diferentes dispositivos. ⚠️

#### **Caminho Triste**
1. **Validação de Campos:**
   - Testar registro com e-mail já cadastrado e validar mensagens de erro. ⚠️
   - Inserir senhas que não atendem aos critérios de segurança e confirmar exibição de erro. ⚠️

2. **Campos Vazios:**
   - Confirmar mensagens de erro ao tentar registrar sem preencher os campos. ✅

3. **Formato Inválido:**
   - Testar com campos no formato errado e validar mensagens de erro. ✅

---

### Tela de "Esqueci a Senha"

#### **Caminho Feliz**
1. **Campo de Entrada:**
   - Confirmar visibilidade do campo de e-mail. ✅
   - Testar com um e-mail válido e verificar mensagem de sucesso. ✅

2. **Botão de Envio:**
   - Garantir habilitação do botão após inserção de e-mail válido. ✅

3. **Responsividade:**
   - Testar em diferentes dispositivos para verificar a adaptabilidade. ✅

#### **Caminho Triste**
1. **Validação de Campos:**
   - Testar recuperação com e-mail não cadastrado. ⚠️ (Informa que foi Enviado com sucesso, não vejo como erro.)

2. **Campo Vazio:**
   - Confirmar exibição de mensagem de erro ao tentar enviar com campo vazio. ✅

3. **Formato de E-mail:**
   - Validar mensagem de erro ao inserir um formato de e-mail inválido. ✅

---

# 🖼️ Imagens de Testes

## Tela de Login

### Testar a entrada de dados válidos e confirmar login bem-sucedido. ⚠️
Ao tentar inserir credenciais válidas de Admin não foi possíve fazer login, login com outros usuários funcionando.

#### Possiveis erros:
- Credenciais fornecidas incorretas, necessário verificar no banco de dados.
- Erro de validação dos dados com banco de dados.

#### Sugestões de melhorias:
- Utilizar UX Writting para esclarecer o erro ocorrido.

![image](https://github.com/user-attachments/assets/8ababf9c-16a7-4101-8969-7932aea8f472)
---
### Testar com senha incorreta e validar mensagens de erro. ⚠️

Ao tentar inserir credenciais inválidas de Admin/User não foi possíve fazer login mas obtive mensagem de sucesso, login com outros usuários e credenciais inválidas também ocorre.

#### Possiveis erros:
- Falha no tratamento de credenciais inválidas, ajustar UX Writting.

#### Sugestões de melhorias:
- Utilizar UX Writting para esclarecer o erro ocorrido
![image](https://github.com/user-attachments/assets/eb7abe16-dc32-4d18-8db6-2fe3aae4180c)
![image](https://github.com/user-attachments/assets/158ba33a-9720-46ea-8aec-b05b88c0ec57)

---
### Verificar redirecionamento correto após o login. ⚠️

Ao acessar com usuário novo cadastrado está aparecendo opções de Admin.

#### Possiveis erros:
- Verificar se cadastro foi realizado como Admin
- Verificar se está direcionando com a Role certa.

![image](https://github.com/user-attachments/assets/71d8255c-c911-49a2-8465-3c33f86c3fb8)

![image](https://github.com/user-attachments/assets/787f9328-fa4e-445a-a1c9-b806b374ea43)

---
### Campos Vazios: Confirmar exibição de mensagens de erro ao tentar logar sem preencher os campos. ⚠️
Mostra que precisa ter no mínimo 6 caracteres, durante registro mostra que o mínimo é 8, ao tentar redefinir senha volta a mostrar 6 caracteres no minimo.

![image](https://github.com/user-attachments/assets/7c526e72-e4f5-4e4d-ad3f-7d56e53fd603)
![image](https://github.com/user-attachments/assets/32ea9e4b-b5bc-4c8e-8e42-96c2b37459d9)
![image](https://github.com/user-attachments/assets/7c1ec3e1-8e3b-4f67-a0e4-0dcad387c79d)

## Tela de Registro

### Botão de Registro: Confirmar redirecionamento correto após o registro. ⚠️

Após realizar registro não redireciona usuario para tela de login.

![image](https://github.com/user-attachments/assets/71d8255c-c911-49a2-8465-3c33f86c3fb8)
---
### Garantir que campos e botões são facilmente utilizáveis em dispositivos móveis. ⚠️
Layout e disposição dos itens fugiram do esperado no Figma. Tela de Registro não tem um aproveitamento bom dos espaços, logo fica no topo da página e com espaço grande até o formulario. O mesmo acontece para desktop.

![image](https://github.com/user-attachments/assets/43b332a1-46cb-4da2-b922-dda421a9095e)

![image](https://github.com/user-attachments/assets/78b9be35-26f5-430b-b5f5-d5588d03baa5)

![image](https://github.com/user-attachments/assets/e3d71128-7c46-4ca1-9fce-a0ded529a75a)
---

### Responsividade: Verificar ajuste adequado da interface em diferentes dispositivos. ⚠️
Quando os inputs são todos incorretos a interface quebra.

![image](https://github.com/user-attachments/assets/66a95129-be10-4375-8fb7-c8f108d25c25)

---
### Validação de Campos: Testar registro com e-mail já cadastrado e validar mensagens de erro. ⚠️
Quando novo cadastro com E-Mail e CPF já cadastrados, não segue o cadastro, mas a mensagem de erro não deixa claro o que aconteceu.

![image](https://github.com/user-attachments/assets/369a289d-7bd8-476c-ac79-a2f79ba797ff)

---
### Validação de Campos: Inserir senhas que não atendem aos critérios de segurança e confirmar exibição de erro. ⚠️

Senha com espaços vazios diz que cadastrou, ao tentar acessar nao faz login. Necessário verificar no Banco de Dados e adicionar validação de senha.

![image](https://github.com/user-attachments/assets/2fc303df-a67a-4973-96e2-7e17e689820e)

---
### EXTRA Validação de Campos: Testar registro com CPF já cadastrado e validar mensagens de erro. ⚠️
Quando novo cadastro com CPF já cadastrado, segue o cadastro, talvez seja bom restringir o cadastro a 1 CPF.

![image](https://github.com/user-attachments/assets/7b280489-2d89-4096-ab77-8cff5f5ab819)

Mesmo CPF email diferente:
![image](https://github.com/user-attachments/assets/61d54943-ad42-4800-ad13-61ca61a813e5)


