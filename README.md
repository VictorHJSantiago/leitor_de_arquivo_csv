<div align="center">📊 Leitor de Arquivo CSV - Análise de Vendas 📈Uma aplicação de desktop Java Swing para ler, processar e analisar dados de vendas de arquivos CSV.</div>🚀 Sobre o ProjetoEsta aplicação é uma ferramenta de análise de dados de vendas desenvolvida em Java. Ela permite ao utilizador carregar um ficheiro CSV e, automaticamente, processa as informações para exibir:O faturamento total por loja.O produto mais vendido (em quantidade).O conteúdo bruto do ficheiro CSV para visualização.A interface foi criada com Java Swing (JFrame) e o projeto é gerido com Apache Maven.✨ Funcionalidades Principais📂 Menu Arquivo > Procurar...: Abre um seletor de ficheiros (JFileChooser) para localizar e selecionar um ficheiro .csv.📰 Menu Arquivo > Abrir...: Após selecionar um ficheiro, esta ação:Exibe o conteúdo bruto do CSV na área de texto principal.Processa os dados (ignorando o cabeçalho).Calcula e exibe o faturamento total das primeiras quatro lojas encontradas.Calcula e exibe o produto mais vendido e a sua quantidade total.🧹 Botão LIMPAR (CLEAR): Limpa todos os campos de texto e a área de visualização do CSV.🚪 Menu Arquivo > Sair...: Fecha a aplicação.🛠️ Tecnologias UtilizadasJava Swing: Para a construção da interface gráfica (GUI).Apache Maven: Para gestão do projeto e dependências.📋 Formato do CSV EsperadoPara que a leitura e os cálculos funcionem corretamente, o ficheiro CSV deve seguir este formato:Delimitador: Ponto e vírgula (;).Cabeçalho: O programa está configurado para ignorar a primeira linha (cabeçalho).Estrutura das Colunas:Índice da ColunaDado EsperadoUtilização2Nome da LojaAgrupamento de faturamento4Nome do ProdutoContagem de produto mais vendido5Quantidade VendidaUsado no cálculo6Preço UnitárioUsado no cálculoO cálculo do faturamento é feito da seguinte forma: coluna[6] (Preço) * coluna[5] (Quantidade).⚙️ Como Compilar e ExecutarPré-requisitosJDK 21 (ou superior)Apache Maven1. Executando pela Linha de ComandoBash# 1. Clone o repositório
git clone [URL_DO_SEU_REPOSITORIO]

# 2. Navegue até à pasta do projeto (AplicacaoLoja)
cd AplicacaoLoja

# 3. Compile o projeto com Maven
mvn compile

# 4. Execute a classe principal (Painel.java)
# (Use o comando apropriado para o seu SO)

# Windows
java -cp "target/classes" aula02.aplicacaoloja.Painel

# Linux/macOS
java -cp "target/classes" aula02.aplicacaoloja.Painel
2. Executando por uma IDE (Recomendado)Abra a sua IDE preferida (IntelliJ IDEA, NetBeans, Eclipse).Importe o projeto como um Projeto Maven existente.Localize o ficheiro src/main/java/aula02/aplicacaoloja/Painel.java.Clique com o botão direito e selecione "Run" (Executar) no método main.<div align="center"><strong>Autor:</strong> VICTOR HENRIQUE DE JESUS SANTIAGO</div>
