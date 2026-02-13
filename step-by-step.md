# B2B – Tratativas Manuais dos Principais Erros Críticos
*(RPA rodando em modo debug)*

As instruções **'Sair com segurança'** nos itens abaixo indicam o processo
- no VivoCorp: `Menu > fazer logout` 

Caso você encerre a execução sem fazer este processo, as credenciais serão bloqueadas por 1h, neste caso você precisa fazer o **Processo de desbloqueio das credenciais**:   
- Acessar: `https://www.portalinfob2b.com.br/login`
- Entrar com as credenciais do robô que estão bloqueadas
- Encerrar a sessão no menu esquerdo (última opção)

---

## 1. Erro no workflow de contas **sem popup na tela**

- Sair com segurança do VivoCorp  
- Enviar o pedido de volta para a fila  
- `Stop Debug`  
- Dar `Play` novamente no `main.py`

---

## 2. Erro no workflow de contas **com popup na tela**

- Clicar em **OK** ou fechar o popup  
- Clicar na aba **"Contas"** ou tentar atualizar a página  
- Dar `Play` no VSCode **sem ter dado Stop antes** (para continuar o processo)

---

## 3. Falha ao carregar o iframe de Anexos

- Se houver aba aberta fora da tela do VivoCorp, fechar  
- Na tela VivoCorp, sair com segurança  
- Enviar o pedido de volta para a fila  
- `Stop Debug`  
- Dar `Play` novamente no `main.py`

---

## 4. Erro de conexão com Oracle (site caiu)

> Esse erro não aparece em breakpoint específico, ele grita no navegador.
> Do ponto de vista do código, ele vai em algum except, depende de onde ele estiver

- Se possível, sair com segurança 
- Caso não consiga:
  - `Stop Debug`
  - Processo de desbloqueio das credenciais
Depois:
- Enviar o pedido de volta para a fila  
- Dar `Play` novamente no `main.py`

---

## 5. Site expulsou o RPA do VivoCorp

- Clicar em **Sair** ou **Encerrar**  
- Enviar o pedido de volta para a fila 
- `Stop Debug`  
- Dar `Play` novamente no `main.py`

---

## 6. "Este acesso já está em uso"

- Processo de desbloqueio das credenciais
- Entrar com as credenciais do robô  
- Encerrar a sessão no menu esquerdo (última opção)  
- Dar `Play` no VSCode **sem ter dado Stop antes** (para continuar o processo)

## 7. "Detectamos sessão da Siebel ativa: escolha a opção que se aplica a você." No navegador:

- Clique no primeiro 'Clique aqui'
- Fecha o navegador 
- Enviar o pedido de volta para a fila
- `Stop Debug` 
- Dar `Play` novamente no `main.py`
