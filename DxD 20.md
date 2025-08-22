import random
import time
import sys

print(r"""
    ____           ____  
   |  _ \         |  _ \ 
   | | | |        | | | |
   | |_| |        | |_| |
   |____/    &    |____/ 

              
""")

input("----- Pressione Enter para rolar o dado -----")

for i in range(10):
    print(f"\r🎲 {random.randint(0,20)}", end="")
    time.sleep(1)
print()

print("🎲 Rolando dado... ")
time.sleep(1.5)

print("Quase lá...")
time.sleep(1.5)

dado = list(range(0, 21))
random.shuffle(dado)

resultado = dado[0]
print(f"Resultado do dado: {resultado}")

if resultado <= 5:
    print("💀 Que bosta, você falhou na sua ação, chance de acerto 0")
elif resultado <= 10:
    print("😬 Você conseguiu completar sua ação, porém não foi eficiente")
elif resultado <= 15:
    print("✅ Boa mano, você conseguiu completar sua ação")
elif resultado <= 19:
    print("🔥 Eita porra, sortudo! Você teve um sucesso crítico! Excelente desempenho.")
else:
    print("💥 KRL!! SEU VIADO, VC TIROU 20! Você teve sucesso crítico e ganhou um bônus de acertividade")

jogar_novamente = input("Quer tentar a sorte de novo? (s/n) ")
if jogar_novamente.lower() == 's':
    print("Ótimo, vamos ver se você para de ser um noob dessa vez... 😏")
else:
    print("Caguei pra você então, tchau! 👋")

    
