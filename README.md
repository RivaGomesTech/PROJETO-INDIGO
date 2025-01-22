# PROJETO-INDIGO
Repositório para entrega de Projeto Final do Grupo Indigo - Mulheres Tech | 2024

#OUTUBRO, NOVEMBRO E DEZEMBRO:
arquivo1=pl.read_csv("202310_NovoBolsaFamilia.csv", separator=";", encoding="latin-1") #caminhos dos arquivos
arquivo2=pl.read_csv("202311_NovoBolsaFamilia.csv", separator=";", encoding="latin-1")
arquivo3=pl.read_csv("202312_NovoBolsaFamilia.csv", separator=";", encoding="latin-1")

inicio_tempo=time.time() #marcação do tempo de processamento
df_polars=pl.concat([arquivo1,arquivo2,arquivo3])

display(df_polars.head())

print("Tempo de execução com Polars:", time.time() - inicio_tempo, "segundos")

#OUTUBRO, NOVEMBRO E DEZEMBRO:
arquivo1=pd.read_csv("202310_NovoBolsaFamilia.csv", sep=";", encoding="latin-1") #caminhos dos arquivos
arquivo2=pd.read_csv("202311_NovoBolsaFamilia.csv", sep=";", encoding="latin-1")
arquivo3=pd.read_csv("202312_NovoBolsaFamilia.csv", sep=";", encoding="latin-1")

inicio_tempo=time.time() #marcação do tempo de processamento
df_pandas=pd.concat([arquivo1,arquivo2,arquivo3])

display(df_pandas.head())

print("Tempo de execução com Pandas:", time.time() - inicio_tempo, "segundos")
