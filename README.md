# ðŸ”§ Sistema de Controle de Equipamentos

Sistema web responsivo para controle de rotas externas e envio de equipamentos para assistÃªncia tÃ©cnica.

## âœ¨ CaracterÃ­sticas

- **Design Moderno**: Interface limpa e profissional em verde e branco
- **Totalmente Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **Sistema de PermissÃµes**: 3 nÃ­veis de acesso (Admin, Editor, Visualizador)
- **Controle de Acesso**: Sistema de login seguro com aprovaÃ§Ã£o de usuÃ¡rios
- **GestÃ£o Completa**: Cadastro, ediÃ§Ã£o e exclusÃ£o de equipamentos
- **Filtros AvanÃ§ados**: Busca por fornecedor, OS, data e status
- **RecuperaÃ§Ã£o de Senha**: Sistema de redefiniÃ§Ã£o de senha com verificaÃ§Ã£o

## ðŸŽ¨ Cores do Sistema

- **Verde Principal**: #22c55e
- **Verde Escuro**: #16a34a
- **Branco**: #ffffff
- **Status coloridos** para fÃ¡cil visualizaÃ§Ã£o

## ðŸ“‹ Funcionalidades

### ðŸ” AutenticaÃ§Ã£o

1. **Login**: Acesso seguro com usuÃ¡rio e senha
2. **Cadastro**: Registro de novos usuÃ¡rios
3. **RecuperaÃ§Ã£o de Senha**: Sistema com verificaÃ§Ã£o por sobrenome
4. **AprovaÃ§Ã£o de UsuÃ¡rios**: Novos usuÃ¡rios aguardam aprovaÃ§Ã£o do admin

### ðŸ‘¥ NÃ­veis de PermissÃ£o

- **Admin**: Acesso total (cadastrar, editar, excluir, aprovar usuÃ¡rios)
- **Editor**: Pode cadastrar novos itens
- **Visualizador**: Apenas visualizar e filtrar

### ðŸ“¦ GestÃ£o de Equipamentos

- Cadastro completo de equipamentos
- Campos obrigatÃ³rios validados
- MÃ¡scara monetÃ¡ria automÃ¡tica
- Status com cores diferenciadas
- EdiÃ§Ã£o e exclusÃ£o (apenas Admin)

### ðŸŽ¯ Status DisponÃ­veis

| Status | Cor |
|--------|-----|
| Aguardando OrÃ§amento | Amarelo |
| Aguardando AprovaÃ§Ã£o | Laranja |
| OrÃ§amento Aprovado | Azul |
| ConcluÃ­da | Verde |
| NÃ£o serÃ¡ feito | Vermelho |
| Aguardando retirada | Roxo |
| Aguardando envio | Cinza |

### ðŸ” Filtros

- Por Fornecedor (Bitmix, LAN7, Outros)
- Por NÃºmero da OS
- Por Data de Envio
- Por Status

## ðŸš€ Como Usar

### InstalaÃ§Ã£o

1. Baixe os arquivos do sistema:
   - `index.html`
   - `styles.css`
   - `script.js`

2. Coloque todos os arquivos na mesma pasta

3. Abra o arquivo `index.html` no navegador

### Primeiro Acesso

1. **Cadastrar o Primeiro UsuÃ¡rio (Admin)**:
   - Clique em "Cadastre-se"
   - Preencha todos os dados
   - O primeiro usuÃ¡rio automaticamente vira **ADMIN**
   - FaÃ§a login com suas credenciais

2. **Aprovar Novos UsuÃ¡rios**:
   - Entre em "ConfiguraÃ§Ãµes" (apenas Admin)
   - Aprove os usuÃ¡rios pendentes
   - Altere as permissÃµes conforme necessÃ¡rio

### Cadastrar Equipamento

1. Clique em "Cadastrar Item"
2. Preencha todos os campos obrigatÃ³rios
3. Selecione "Outros" para adicionar empresas ou equipamentos personalizados
4. Clique em "Salvar Item"

### Editar Equipamento

1. Na lista de equipamentos, clique em "Editar" (apenas Admin)
2. Modifique os campos necessÃ¡rios
3. Clique em "Salvar AlteraÃ§Ãµes"

### Excluir Equipamento

1. Na lista de equipamentos, clique em "Excluir" (apenas Admin)
2. Confirme a exclusÃ£o

## ðŸ“± Responsividade

O sistema se adapta automaticamente a diferentes tamanhos de tela:

- **Desktop**: Layout completo com todas as colunas visÃ­veis
- **Tablet**: Ajuste automÃ¡tico da grid
- **Mobile**: Layout otimizado para telas pequenas

## ðŸ’¾ Armazenamento

O sistema utiliza **LocalStorage** do navegador para armazenar:
- Dados dos usuÃ¡rios
- Dados dos equipamentos
- SessÃ£o do usuÃ¡rio logado

**Importante**: Os dados ficam salvos no navegador. Para backup, vocÃª pode exportar os dados (funcionalidade futura).

## ðŸ”’ SeguranÃ§a

- Senhas armazenadas no localStorage (para produÃ§Ã£o, use backend com criptografia)
- ValidaÃ§Ã£o de permissÃµes em todas as aÃ§Ãµes
- SessÃ£o persistente atÃ© logout manual
- AprovaÃ§Ã£o obrigatÃ³ria de novos usuÃ¡rios

## âš™ï¸ Campos do Cadastro de Equipamento

### Campos ObrigatÃ³rios:

- **Data de envio**: Data que o equipamento foi enviado
- **Garantia**: Sim ou NÃ£o
- **Empresa**: Bitmix, LAN7 ou Outros (especificar)
- **OS**: NÃºmero da Ordem de ServiÃ§o
- **Valor**: Valor monetÃ¡rio (formato R$)
- **Equipamento**: Notebook, Impressora Zebra, Computador, Celular, ThinClient ou Outros
- **Marca/Modelo**: Marca e modelo do equipamento
- **PatrimÃ´nio**: NÃºmero do patrimÃ´nio
- **NÂº de SÃ©rie**: NÃºmero de sÃ©rie do equipamento
- **Chamado**: Formato TI-0000
- **Ãrea Solicitante**: Departamento que solicitou
- **Backup instalado**: Sim ou NÃ£o
- **ConcluÃ­do**: Sim ou NÃ£o
- **Status**: Status atual do equipamento
- **ResponsÃ¡vel pelo chamado**: Nome do responsÃ¡vel

## ðŸŽ¯ Regras de NegÃ³cio

1. **Primeiro usuÃ¡rio** cadastrado = Admin automÃ¡tico
2. **Demais usuÃ¡rios** = Visualizador por padrÃ£o (aguardam aprovaÃ§Ã£o)
3. **Admin** tem acesso total ao sistema
4. **Editor** pode apenas cadastrar novos itens
5. **Visualizador** pode apenas ver e filtrar dados
6. Apenas **Admin** pode editar e excluir equipamentos
7. Apenas **Admin** pode aprovar usuÃ¡rios e alterar permissÃµes

## ðŸ”„ RecuperaÃ§Ã£o de Senha

1. Digite a matrÃ­cula (crachÃ¡)
2. Sistema exibe 3 opÃ§Ãµes de sobrenome (apenas 1 correta)
3. Ao acertar, redireciona para redefinir senha
4. Crie nova senha e confirme

## ðŸ“Š PrÃ³ximas ImplementaÃ§Ãµes

- [ ] ExportaÃ§Ã£o para Excel
- [ ] RelatÃ³rios personalizados
- [ ] GrÃ¡ficos e dashboards
- [ ] NotificaÃ§Ãµes de status
- [ ] HistÃ³rico de alteraÃ§Ãµes
- [ ] Backend com banco de dados real
- [ ] API REST
- [ ] AutenticaÃ§Ã£o JWT

## ðŸ› ï¸ Tecnologias Utilizadas

- **HTML5**: Estrutura semÃ¢ntica
- **CSS3**: Design responsivo com Flexbox e Grid
- **JavaScript ES6+**: LÃ³gica de negÃ³cio
- **LocalStorage**: Armazenamento local

## ðŸ“ž Suporte

Para dÃºvidas ou problemas:
- Verifique se todos os arquivos estÃ£o na mesma pasta
- Limpe o cache do navegador se houver problemas
- Use navegadores modernos (Chrome, Firefox, Edge, Safari)

## ðŸ“„ LicenÃ§a

Sistema desenvolvido para controle interno de equipamentos.

---

**Desenvolvido com ðŸ’š usando as melhores prÃ¡ticas de desenvolvimento web**
