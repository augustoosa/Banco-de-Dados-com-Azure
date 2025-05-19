# Banco-de-Dados-com-Azure
Atividade prática do curso de Computação em Nuvem com foco na criação de uma Instância Gerenciada de Banco de Dados SQL no Microsoft Azure. O objetivo é explorar os principais recursos da plataforma e documentar o processo de configuração por meio de resumos, anotações e boas práticas.

# Azure SQL Managed Instance - Guia Prático

Este repositório foi criado como parte de uma atividade prática sobre **Computação em Nuvem com Microsoft Azure**. O objetivo é documentar o processo de criação de uma **Instância Gerenciada do Azure SQL**, fornecendo resumos, anotações e dicas úteis para estudo e futuras implementações.

## Etapas para Criar uma Instância de Banco de Dados

### 1. Acesso ao Portal

- Acesse o [Portal do Azure](https://portal.azure.com)
- Vá em: **Criar um recurso** > **Banco de Dados** > **Instância Gerenciada do SQL**

---

### 2. Configurações Básicas

Nesta aba, você define os principais parâmetros da instância:

- **Assinatura:** Plano de cobrança usado. Escolha sua assinatura ativa.
- **Grupo de Recursos:** Contêiner lógico para organizar recursos relacionados. Pode criar um novo ou usar um existente.
- **Nome da Instância:** Nome único e descritivo para a instância SQL.
- **Região:** Escolha a região geográfica onde a instância será hospedada (ex: Brazil South).
- **Camada de Preço (Service Tier):**  
  - *General Purpose:* Ideal para cargas de trabalho comuns e de custo moderado.  
  - *Business Critical:* Alta performance, indicada para aplicações sensíveis ao tempo de resposta.

---

### 3. Configurações de Rede

- Use uma **rede virtual existente**, com uma **sub-rede dedicada** para a instância.
- A sub-rede não deve ter gateways de rede (VPN ou ExpressRoute).
- Configure o acesso à instância de acordo com sua necessidade de segurança e conectividade.

---

### 4. Configurações SQL

- **Tipo de Autenticação:** Pode ser SQL (usuário e senha), Azure Active Directory (AD), ou ambos.
- **Administrador SQL:** Defina o nome do usuário administrador e sua senha.
- **Backup Automático:** O Azure realiza backups automáticos, e você pode definir o tempo de retenção.

---

### 5. Revisar + Criar

- Revise todas as configurações feitas nas abas anteriores.
- Clique em **Criar** para iniciar a implantação.
- O provisionamento pode levar até **6 horas** para ser concluído.

---

## Dicas

- Nomeie instâncias e recursos com padrões consistentes para facilitar o gerenciamento.
- Escolha a região mais próxima dos usuários ou da aplicação para melhorar o desempenho.
- Após a criação, conecte-se usando ferramentas como **SQL Server Management Studio (SSMS)** ou **Azure Data Studio**.

---

## Referência Oficial

-  [Microsoft Learn - Criar Instância SQL Gerenciada (Azure Portal)](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql&tabs=azure-portal)

---

## 🧠 Conclusão

A Instância Gerenciada do Azure SQL é uma solução prática e robusta para hospedar bancos de dados na nuvem com alta compatibilidade com SQL Server. Ideal para migrações de ambientes locais e novas aplicações em nuvem com foco em escalabilidade, segurança e simplicidade operacional.
