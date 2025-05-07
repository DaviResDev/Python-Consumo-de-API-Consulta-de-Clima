import requests

def obter_clima(cidade):
    api_key = "SUA_CHAVE_API"  # Substitua pela sua chave da API OpenWeatherMap
    url = f"http://api.openweathermap.org/data/2.5/weather?q={cidade}&appid={api_key}&lang=pt_br&units=metric"

    resposta = requests.get(url)
    
    if resposta.status_code == 200:
        dados = resposta.json()
        clima = {
            "Cidade": dados["name"],
            "Temperatura": dados["main"]["temp"],
            "Descrição": dados["weather"][0]["description"]
        }
        return clima
    else:
        return {"Erro": "Cidade não encontrada"}

# Teste
cidade = input("Digite o nome da cidade: ")
print(obter_clima(cidade))
