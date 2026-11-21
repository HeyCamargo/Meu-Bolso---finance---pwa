# MeuBolso — Controle Financeiro Pessoal

Projeto acadêmico desenvolvido como uma aplicação web progressiva (PWA) para auxiliar no controle das finanças pessoais, permitindo registrar movimentações, acompanhar o orçamento, organizar metas e consultar informações de moedas.

## Instituição

**Fundação Hermínio Ometto (FHO)**  
Araras — São Paulo

## Integrantes

- **João Victor Camargo** — RA: 113803
- **Guilherme Belem** — RA: 114031

## Sobre o projeto

O **MeuBolso** é uma aplicação de controle financeiro pessoal com interface adaptada para dispositivos móveis. O usuário pode criar uma conta, registrar receitas e despesas, acompanhar o saldo e visualizar análises sobre sua movimentação financeira.

O projeto utiliza tecnologias web e recursos de PWA para permitir que a aplicação seja instalada no dispositivo e tenha recursos básicos de funcionamento offline por meio de cache.

## Funcionalidades

### 1. Acesso e contas
- Cadastro de usuário e senha.
- Login e encerramento de sessão.
- Atalhos para contas salvas no dispositivo.
- Separação dos dados financeiros por usuário no armazenamento local.

### 2. Controle financeiro
- Registro de entradas e saídas.
- Classificação por categorias, como alimentação, transporte, lazer, moradia, saúde, salário/renda e outros.
- Histórico de movimentações organizado por data.
- Cálculo e exibição do saldo disponível.
- Opção para ocultar ou exibir o saldo.
- Definição de uma renda mensal de referência.
- Acompanhamento do orçamento mensal e do percentual utilizado.
- Ajuste manual do saldo e opção para zerar os dados da conta.

### 3. Contas fixas e metas
- Cadastro de despesas recorrentes.
- Lançamento de uma conta fixa diretamente no histórico.
- Criação de metas financeiras com valor desejado e saldo inicial.
- Acompanhamento do progresso das metas.
- Adição de valores às metas cadastradas.

### 4. Análises financeiras
- Resumo de entradas e saídas.
- Cálculo de indicador percentual de economia.
- Distribuição das despesas por categoria.
- Gráfico e barras de progresso para facilitar a visualização dos gastos.

### 5. Cotações e conversor de moedas
- Consulta de cotações de moedas.
- Conversão de valores a partir do real.
- Opções de moeda como dólar, euro, libra, dólar canadense, peso argentino, iene e Bitcoin.
- Estimativa de IOF conforme a modalidade selecionada.
- Gráfico de variação histórica com períodos de 7 e 30 dias.
- Configuração de valor-alvo e notificações de cotação, quando permitidas pelo navegador.
- Atalho para acessar serviços externos de câmbio.

### 6. Localização e mapa de transações
- Obtenção da localização por GPS mediante permissão do usuário.
- Associação das coordenadas à próxima movimentação registrada.
- Exibição, em mapa, das transações que possuem coordenadas salvas.

## Tecnologias e bibliotecas

- **HTML5:** estrutura das páginas e formulários.
- **CSS3:** estilos, layout responsivo e identidade visual.
- **JavaScript:** regras de negócio, interações e manipulação dos dados.
- **LocalStorage:** armazenamento local de contas e informações financeiras.
- **Service Worker:** cache de arquivos e suporte básico a recursos offline.
- **Web App Manifest:** configurações de instalação da PWA.
- **Leaflet.js / OpenStreetMap:** mapa e marcadores de transações.
- **Chart.js:** gráficos financeiros e históricos.
- **Lucide:** ícones da interface.
- **API de cotações:** consulta de valores de moedas.
- **Geolocation API:** captura de coordenadas com autorização do usuário.

## Estrutura dos arquivos

```text
MeuBolso/
├── index.html      # Estrutura das telas e componentes
├── style.css       # Estilos e responsividade
├── app.js          # Lógica e funcionalidades da aplicação
├── manifest.json   # Configurações da PWA
├── sw.js           # Service Worker e cache
└── icon.png        # Ícone da aplicação
```

## Como executar

1. Baixe ou clone os arquivos do projeto.
2. Mantenha os arquivos na mesma pasta e preserve os nomes esperados pela aplicação.
3. Execute o projeto por meio de um servidor local (por exemplo, a extensão Live Server do Visual Studio Code).
4. Abra o endereço local disponibilizado pelo servidor em um navegador atualizado.

> **Importante:** para testar corretamente recursos de PWA, Service Worker, geolocalização e instalação, utilize `localhost` ou publique a aplicação em um endereço HTTPS. A abertura direta do arquivo `index.html` (`file://`) não oferece suporte completo a esses recursos.

## Instalação como PWA

Em um navegador compatível, abra a aplicação pelo endereço HTTPS e utilize a opção de instalação ou de adicionar à tela inicial. O manifesto define o nome, o ícone e a exibição em modo independente. O Service Worker realiza o cache dos arquivos configurados para oferecer suporte básico offline.

## Armazenamento e observações

- Os dados são armazenados no **LocalStorage do navegador**, separados por conta e dispositivo.
- O projeto não utiliza, na implementação apresentada, um servidor ou banco de dados remoto para sincronizar contas.
- Por isso, os dados não são sincronizados automaticamente entre celulares ou computadores. Limpar os dados do navegador ou trocar de dispositivo pode resultar na perda ou indisponibilidade dos registros locais.
- As contas salvas e os dados financeiros permanecem no dispositivo em que foram cadastrados.
- As consultas de cotações, bibliotecas externas, mapas e outros recursos online dependem de conexão com a internet.
- A geolocalização e as notificações dependem do suporte do navegador e da autorização do usuário.
- **Este projeto tem finalidade acadêmica e demonstrativa.** O armazenamento local de credenciais não deve ser considerado um mecanismo de autenticação seguro para uso em produção. Uma versão de produção deve utilizar autenticação e armazenamento protegidos em um backend.

## Objetivo acadêmico

Demonstrar a aplicação integrada de tecnologias de desenvolvimento web na construção de uma ferramenta de organização financeira pessoal, explorando armazenamento no navegador, interfaces responsivas, gráficos, APIs, geolocalização e recursos de Progressive Web App.

---

**MeuBolso — Controle financeiro pessoal**  
Fundação Hermínio Ometto (FHO) — Araras/SP  
João Victor Camargo (RA 113803) • Guilherme Belem (RA 114031)
