# Comandos Utilizados para Manipulação dos Dados

#### **- Upload do arquivo -**
 	from google.colab import files <br/>
 	arq = files.upload()

#### **- Criando nosso data frame -**
	df = pd.read_excel("AdventureWorks.xlsx")
	
#### **- Criando coluna Custo -**
	df["custo"] = df["Custo Unitário"].mul(df["Quantidade"])
	
#### **- Criando coluna Lucro -**
	df["lucro"] = df["Valor Venda"] - df["custo"]
	
#### **- Criando coluna Tempo_Envio -**
	df["Tempo_envio"] = df["Data Envio"] - df["Data Venda"]
	df["Tempo_envio"] = (df["Data Envio"] - df["Data Venda"]).dt.days
