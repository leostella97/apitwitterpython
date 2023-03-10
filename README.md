# Consumindo a API do Twitter com Python
Para começar, você precisará criar uma conta de desenvolvedor no Twitter e criar um aplicativo para obter as credenciais de autenticação. Em seguida, instale a biblioteca tweepy usando o pip. Você pode fazer isso abrindo o terminal do seu sistema operacional e digitando o seguinte comando:
<code>
pip install tweepy
</code>
Depois de instalar o tweepy, você pode começar a usar a API do Twitter com o Python. Primeiro, importe a biblioteca tweepy e defina as chaves de autenticação da API do Twitter. Você pode fazer isso da seguinte maneira:

<code>
import tweepy

consumer_key = 'sua_consumer_key'
consumer_secret = 'seu_consumer_secret'
access_token = 'seu_access_token'
access_token_secret = 'seu_access_token_secret'

auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)

api = tweepy.API(auth)
</code>
Com isso, você pode usar o objeto api para fazer chamadas para a API do Twitter. Por exemplo, para obter os últimos 20 tweets de um determinado usuário, você pode usar o seguinte código:

<code>
tweets = api.user_timeline(screen_name='nome_do_usuario', count=20)
for tweet in tweets:
    print(tweet.text)
</code>
Isso imprimirá os textos dos últimos 20 tweets do usuário especificado. Há muitas outras funcionalidades disponíveis na API do Twitter que você pode explorar usando o tweepy.
