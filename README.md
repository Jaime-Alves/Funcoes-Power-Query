A fx-RemoverEspacos pode ser usada em várias colunas de uma vez mas será necessária uma etapa listando as colunas a serem limpas

Exemplo:
Fonte = SuaTabela
ColunasParaLimpar = {"Grp Variedade", "Variedade", "Cultura"}
ColunasLimpas = Table.TransformColumns(#"Fonte", List.Transform(ColunasParaLimpar, each { _, #"fx-RemoverEspacos", type text}))
