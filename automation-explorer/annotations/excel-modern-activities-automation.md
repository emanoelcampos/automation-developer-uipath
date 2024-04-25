# Build Automation using Excel Modern Activities

## Scenario:

A company has two departments tracking their data separately in **Excel** spreadsheets.

1. Acquisitions department:
- tracks information about:
	- products 
	- supplies purchased
- spreadsheet includes:
	- document number
	- emission date
	- acquisition total
	- supplier

2. Sales department:
- tracks information about:
	- sales transactions 
- spreadsheet includes:
	- document number
	- client name
	- agent name

### Master Spreadsheet

The company wants to create a master spreadsheet.

- able to easily view and analyze data from both departments in one place.

### Automation Part 1:

1. Use Excel File - Acquisitions
- Seleciona Acquisitions.xlsx como arquivo Excel a ser usado, referencia como Acquisitions
2. Do -> Remove Duplicates
- Seleciona o range de Acquisitions, a Sheet inteira e coluna 'Doc. Number' que vai ser comparada

*A partir desse ponto temos uma planilha Excel Acquisitions sem linhas duplicadas que foram filtradas pela coluna 'Doc. Number'.*

3. Use Excel File - Past Acquisitions
- Na pasta de Output, seleciona o arquivo MonthReport.xlsx que vai ser criado porque não existe, referencia como MonthReportAcquisitions
4. Do -> Copy/Paste Range
- Copia e cola a Sheet inteira de Acquisitions.xlsx sem as partes duplicadas e cola no arquivo novo MonthReport.xlsx com a Sheet de mesmo nome "Acquisitions".

*A partir desse ponto temos uma planilha Excel MonthReport com uma Sheet nomeada de Acquisitions com os valores únicos da planilha de Acquisitions*

1. Use Excel File - Sales
- Seleciona Sales.xlsx como arquivo Excel a ser usado, referencia como Sales
2. Do -> Use Excel File 
- Na pasta de Output, seleciona o arquivo MonthReport.xlsx que já existe, referencia como MonthReportSales
3. Do -> Copy/Paste Range
- Copia e cola a Sheet inteira de Sales.xlsx e cola no arquivo novo MonthReport.xlsx com a Sheet de mesmo nome "Sales".

*A partir desse ponto temos uma planilha Excel MonthReport com duas Sheets, a primeira nomeada de Acquisitions com os valores únicos da planilha de Acquisitions e a segunda Sheet nomeada Sales com os valores da planilha Sales.

1. Use Excel File
- Seleciona MonthReport.xlsx como arquivo Excel a ser usado, referencia como MonthReport
2. Do -> Insert Column
- Seleciona o range da planilha MonthReport usando a Sheet *Sales*.
- Indica que a coluna deve ser inserida *DEPOIS* de 'Agent Name'.
- Adiciona a header *Total Sales*
3. Insert Column
- Seleciona o range da planilha MonthReport usando a Sheet *Sales*.
- Indica que a coluna deve ser inserida *DEPOIS* de 'Total Sales'.
- Adiciona a header *Profit Per Sales*
4. For Each Excel Row - MonthReport
- Seleciona o range da planilha MonthReport usando a Sheet *Sales*
	1. Do -> VLookup
	- Seleciona o valor que deve procurar apontando para a coluna *Doc. Number* usando a função 'ByField()' junto da 'CurrentRow' = `CurrentRow.ByField("Doc. Number")`
	- Seleciona o range de procura do valor, selecionando a planilha MonthReport e a Sheet *Acquisitions*
	- Seleciona '3' como Column Index, que é o valor a ser retornado pela busca, que nesse caso é a coluna *Acquisition Total*
	- Salva o valor em *VLOOKUP_Value*
	2. Write Cell - Total Sales
	- Descreve o que deve ser escrito na célula: VLOOKUP_Value + VLOOKUP_Value * 0.2
	- Seleciona onde escrever deve ser escrito: na coluna *Total Sales* que já foi criada usando a função `.ByField("Total Sales")` junto da current row do for each.
	3. Write Cell - Profit Per Sale
	- Descreve o que deve ser escrito na célula:  VLOOKUP_Value * 0.2
	- Seleciona onde escrever deve ser escrito: na coluna Profit Per Sales que já foi criada usando a função `.ByField("Profit Per Sales")` junto da current row do for each.

*Na planilha final temos o arquivo MonthReport com duas Sheets, Acquisitions e SaLes. Acquisitions permanece com os dados que foram copiadas da planilha Acquisition. A Sheet Sales recebe além dos valores copiados, duas colunas novas: Total Sales e Profit Per Sales com o resultado de cada uma usando as informações da coluna Total Acquisition da Sheet Acquisitions.*
