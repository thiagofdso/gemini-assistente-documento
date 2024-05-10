# Assistente para documento de normas
O [projeto](https://github.com/thiagofdso/gemini-assistente-documento/blob/main/%5BImers%C3%A3o_IA_2%C2%AA_edi%C3%A7%C3%A3o%5D_C%C3%B3digo_Projeto_Assistente_Documento.ipynb) visa reponder perguntas com base num documento de normas. Está sendo usado como exemplo as normas da [Portaria SGD/ME nº 5.651, de 28 de junho de 2022](https://www.gov.br/governodigital/pt-br/contratacoes-de-tic/diretrizes-para-contratacao-de-servicos-de-desenvolvimento-e-manutencao-de-sistemas), foi extraido seu conteudo e salvo em um [arquivo txt](https://raw.githubusercontent.com/thiagofdso/gemini-assistente-documento/main/Portaria_SGD_ME_5651_28_06_2022.txt).

## Como funciona
Esta sendo usado o modelo `models/embedding-001` para extrair os tokens do documento, o mesmo processo é feito na pergunta.
Com base nos tokens é feito o produto escalar e são identificados os top 20 indices que estão relacionado com a pergunta.
Usando o modelo `gemini-1.0-pro` solicitamos que seja feito um resumo do conteúdo selecionado sem acrescentar nada.
