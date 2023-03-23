<h1>Twitter Sentiment Analysys With Roberta</h1>
Este projeto utilizou a API do Twitter para coletar cerca de 50.000 tweets sobre "The Last of Us" e, em seguida, aplicou técnicas de pré-processamento de texto, Word Cloud e análise de sentimento utilizando o modelo pré-treinado Roberta.

<h2>Objetivo</h2>
O objetivo deste projeto era ter uma melhor percepção do que as pessoas que assistiram ou jogaram "The Last of Us" estavam falando no Twitter poucos dias após o término da primeira temporada, utilizando Word Cloud e análise de sentimento utilizando um modelo pré-treinado chamado "Roberta".

<h2>Sobre o modelo "Roberta"</h2>

Roberta é um modelo de linguagem natural pré-treinado criado pela equipe de pesquisa do Facebook AI. Ele é baseado na arquitetura do Transformer e treinado em uma grande quantidade de dados textuais (15 milhões de comentários), incluindo a Wikipedia e o Common Crawl, para aprender padrões na linguagem natural. Em geral, a acurácia da Roberta em análise de sentimento é alta e chega a valores acima de 90%.
Para mais informações: https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment

<h2>Extração e Estruturação dos Dados, Construção da Word Cloud e Análise de Sentimentos</h2>
Foram extraídos aproximadamente 50.000 tweets utilizando a API do Twitter, com a query "the last of us" em inglês e postados entre os dias 16/03/2023 e 20/03/2023. Esses comentários foram estruturados em um DataFrame e pré-processados através de tokenização, remoção de stop words e caracteres especiais. Em seguida, foi aplicado um filtro para selecionar os adjetivos mais mencionados, a fim de obter uma melhor compreensão do sentimento das pessoas em relação à marca.
<div style="display: flex;">
  <img src="https://user-images.githubusercontent.com/110298606/227333588-d9f2bc52-7441-4b03-b566-8dca4c8d6b26.png" height="500px" style="display: inline-block;">
  <img src="https://user-images.githubusercontent.com/110298606/227335216-20cb193f-b606-4f19-be0f-5eddea4c66e5.png" height="500px" width= 630px style="display: inline-block;">
</div>

Após a geração da Word Cloud, foi realizado um pré-processamento adicional dos dados para aplicá-los ao modelo pré-treinado "Roberta". Isso envolveu a criação de uma nova coluna com os dados tratados, a tokenização, a vetorização e a aplicação dos dados no modelo. Os resultados foram colocados em um DataFrame, onde as previsões positivas representaram 20,78% dos comentários, as negativas 19% e as neutras 60%.

<h3>Conclusão</h3>
A Word Cloud gerada a partir dos dados mostrou que os adjetivos positivos foram os mais mencionados. Porém, com a análise de sentimentos realizada, podemos concluir que as opiniões sobre "The Last of Us" estão bastante divididas, com opiniões positivas(20,78%) e negativas (19%) em proporções quase iguais, e a maioria dos comentários sendo neutros (60%).  Esta análise pode ser útil para entender melhor a percepção do público em relação à marca e, assim, tomar decisões mais informadas em futuras campanhas de marketing.



