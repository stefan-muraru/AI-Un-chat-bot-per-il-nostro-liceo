from ollama import chat
from ollama import ChatResponse

# ✅ Caricamento sicuro del file con gestione errori
try:
    with open("C:/Users/vital/Desktop/python/Liceo_Tosi.txt", "r", encoding="utf-8") as file:
        contenuto_scuola = file.read()
except FileNotFoundError:
    print("❌ Errore: Il file 'Liceo_Tosi.txt' non è stato trovato.")
    exit()
except Exception as e:
    print(f"❌ Errore nella lettura del file: {e}")
    exit()

print("✅ Assistente del Liceo Tosi attivo. Scrivi 'esci' per uscire.\n")

# 🔁 Inizio ciclo domanda/risposta
while True:
    messaggio = input("Tu: ")

    if messaggio.strip().lower() in ["esci", "exit", "quit"]:
        print("🛑 Conversazione terminata.")
        break

    # 🔍 Costruiamo un prompt completo includendo il contenuto del file
    prompt_completo = (
        "Sei un assistente virtuale del Liceo Tosi. Rispondi solo usando le informazioni seguenti:\n\n"
        f"{contenuto_scuola}\n\n"
        f"Domanda: {messaggio}\n"
        "Risposta:"
    )

    # 👉 Tutto in un unico messaggio 'user'
    messages = [
        {'role': 'user', 'content': prompt_completo}
    ]

    try:
        response: ChatResponse = chat(model='deepseek-r1', messages=messages)
        risposta = response.message.content if response and response.message else "❌ Nessuna risposta dal modello."
    except Exception as e:
        risposta = f"❌ Errore nella chiamata al modello: {e}"

    print("\nAssistente:", risposta)
    print("-" * 60)
