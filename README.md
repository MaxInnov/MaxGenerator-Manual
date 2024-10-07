# Manual de Uso: Gerador de DNS MaxInnov e Integração com Cloudflare

## Introdução

Este manual tem como objetivo guiar o cliente no uso do **Gerador de DNS MaxInnov** para gerar registros DNS de forma rápida e eficiente e, em seguida, realizar a importação dos registros gerados para o Cloudflare.

### O que você vai precisar:

- Acesso ao painel do Cloudflare.
- Informações básicas de DNS, como nome do cliente, domínio base e IP da VPS.
- Acesso ao gerador de DNS fornecido pela MaxInnov.

---

## 1. Utilizando o Gerador de DNS

### Passo 1: Preenchendo os Dados Básicos

1. Acesse o gerador de DNS.
2. Preencha os campos obrigatórios:
   - **Nome do Cliente:** Digite o nome do cliente ou serviço. Esse campo será usado para gerar o subdomínio (ex: `vps.nomecliente.maxinnov.com.br`).
   - **Domínio Base:** Informe o domínio principal (ex: `maxinnov.com.br`).
   - **IP da VPS:** Informe o endereço de IP da sua VPS.

### Passo 2: Selecionando os Serviços

Na seção **Serviços**, você encontrará uma lista de serviços pré-definidos (como Chatwoot, MongoDB, WordPress, etc.). Para cada serviço que você deseja associar à sua VPS:

1. Marque a caixa de seleção correspondente ao serviço que deseja adicionar.
2. Caso o serviço desejado não esteja listado, clique em **Adicionar Serviço Manual** para incluir um serviço personalizado.

### Passo 3: Gerando o Arquivo de Importação

Após preencher todos os campos e selecionar os serviços:

1. Clique no botão **Gerar Arquivo de Importação**.
2. O gerador criará um arquivo de texto (`importacao_dns.txt`) com os registros DNS necessários (A Records e CNAME Records).
3. O arquivo será automaticamente baixado para o seu dispositivo.

---

## 2. Importando o Arquivo para o Cloudflare

### Passo 1: Acessando o Cloudflare

1. Acesse [Cloudflare](https://www.cloudflare.com/) e faça login na sua conta.
2. Selecione o domínio no qual deseja adicionar os registros DNS.

### Passo 2: Navegando até a Configuração de DNS

1. No painel do Cloudflare, clique na aba **DNS**.
2. Verifique se o seu domínio principal está devidamente configurado.

### Passo 3: Importando os Registros DNS

1. Dentro da aba DNS, localize a opção **Importar/Exportar DNS** (geralmente na parte inferior da página).
2. Clique em **Importar Arquivo DNS**.
3. Selecione o arquivo `importacao_dns.txt` que você baixou anteriormente.
4. Confirme a importação dos registros. O Cloudflare automaticamente adicionará os registros de DNS ao seu domínio.

---

## 3. Validação e Testes

Após a importação:

1. Verifique na aba **DNS** se todos os registros foram adicionados corretamente.
2. Aguarde a propagação dos DNS, o que pode levar até 24 horas.
3. Teste os serviços e subdomínios criados para garantir que estão funcionando corretamente.

---

## Dúvidas e Suporte

Caso encontre dificuldades ou precise de mais informações, entre em contato com o suporte da MaxInnov pelo e-mail: **[contato@maxinnov.com.br](mailto:contato@maxinnov.com.br)**.

### Doações

Se você deseja apoiar o desenvolvimento deste projeto, considere fazer uma doação utilizando a chave PIX:

**Chave PIX:** `contato@maxinnov.com.br`.

---

Este manual visa garantir uma experiência simplificada no uso do gerador de DNS e na integração com o Cloudflare.

