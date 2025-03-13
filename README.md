# Perceptron
# Atividade 1
from sklearn.linear_model import Perceptron

X = [[0, 0], [0, 1], [1, 0], [1, 1]]

Y = [0, 1, 1, 1]

modelo = Perceptron()
modelo.fit(X, Y)

print("Previsões:")
testes = [[0,0], [0,1], [1,0], [1,1]]
for teste in testes:
  previsao = modelo.predict([teste])
  print(f"Nuvens: {teste[0]}, Previsão Chuva: {teste[1]} => Levar Guarda-chuva? {'Sim' if previsao[0] == 1 else 'Não'}")

Previsões:
Nuvens: 0, Previsão Chuva: 0 => Levar Guarda-chuva? Não
Nuvens: 0, Previsão Chuva: 1 => Levar Guarda-chuva? Sim
Nuvens: 1, Previsão Chuva: 0 => Levar Guarda-chuva? Sim
Nuvens: 1, Previsão Chuva: 1 => Levar Guarda-chuva? Sim

# Atividade 2
from sklearn.linear_model import Perceptron

X = [[0,0,0], [0,1,0], [1,0,0], [1,1,0], [0,0,1], [0,1,1], [1,0,1], [1,1,1]]

Y = [0, 1, 1, 1, 0, 0, 0, 0]

modelo = Perceptron()
modelo.fit(X, Y)

print("Previsões:")
testes = [[0,0,0], [0,1,0], [1,0,0], [1,1,0], [0,0,1], [0,1,1], [1,0,1], [1,1,1]]
for teste in testes:
  previsao = modelo.predict([teste])
  print(f"Ensolarado: {teste[0]}, Final de semana: {teste[1]}, Parque lotado: {teste[2]} => Ir ao parque? {'Não' if previsao[0] == 0 else 'Sim' }")

Previsões:
Ensolarado: 0, Final de semana: 0, Parque lotado: 0 => Ir ao parque? Não
Ensolarado: 0, Final de semana: 1, Parque lotado: 0 => Ir ao parque? Sim
Ensolarado: 1, Final de semana: 0, Parque lotado: 0 => Ir ao parque? Sim
Ensolarado: 1, Final de semana: 1, Parque lotado: 0 => Ir ao parque? Sim
Ensolarado: 0, Final de semana: 0, Parque lotado: 1 => Ir ao parque? Não
Ensolarado: 0, Final de semana: 1, Parque lotado: 1 => Ir ao parque? Não
Ensolarado: 1, Final de semana: 0, Parque lotado: 1 => Ir ao parque? Não
Ensolarado: 1, Final de semana: 1, Parque lotado: 1 => Ir ao parque? Não

# Atividade 3
from sklearn.linear_model import Perceptron

X = [[0,1,1,1], [1,0,1,1], [1,1,0,1], [0,0,1,0], [1,1,1,1], [0,1,0,0], [1,0,0,1], [0,0,0,1]]

Y = [0, 1, 0, 1, 1, 0, 0, 0]

modelo = Perceptron()
modelo.fit(X, Y)

print("Previsões:")
testes = [[0,1,1,1], [1,0,1,1], [1,1,0,1], [0,0,1,0], [1,1,1,1], [0,1,0,0], [1,0,0,1], [0,0,0,1]]
for teste in testes:
  previsao = modelo.predict([teste])
  print(f"Cansado: {teste[0]}, Ingredientes em casa: {teste[1]}, Restaurante aberto: {teste[2]}, Pagamento recente: {teste[3]} => Comer fora? {'Não' if previsao[0] == 0 else 'Sim' }")

Previsões:
Cansado: 0, Ingredientes em casa: 1, Restaurante aberto: 1, Pagamento recente: 1 => Comer fora? Não
Cansado: 1, Ingredientes em casa: 0, Restaurante aberto: 1, Pagamento recente: 1 => Comer fora? Sim
Cansado: 1, Ingredientes em casa: 1, Restaurante aberto: 0, Pagamento recente: 1 => Comer fora? Não
Cansado: 0, Ingredientes em casa: 0, Restaurante aberto: 1, Pagamento recente: 0 => Comer fora? Sim
Cansado: 1, Ingredientes em casa: 1, Restaurante aberto: 1, Pagamento recente: 1 => Comer fora? Sim
Cansado: 0, Ingredientes em casa: 1, Restaurante aberto: 0, Pagamento recente: 0 => Comer fora? Não
Cansado: 1, Ingredientes em casa: 0, Restaurante aberto: 0, Pagamento recente: 1 => Comer fora? Não
Cansado: 0, Ingredientes em casa: 0, Restaurante aberto: 0, Pagamento recente: 1 => Comer fora? Não

