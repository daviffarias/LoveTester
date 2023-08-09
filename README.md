import tkinter as tk
import random

# Define a função para calcular a compatibilidade amorosa
def calculate_love():
    # Obter os nomes inseridos nos campos de texto
    name1 = name1_entry.get().lower()
    name2 = name2_entry.get().lower()

    # Calcular um valor de compatibilidade aleatório
    love_value = random.randint(1, 100)

    # Atualiza o rótulo de resultado com a mensagem de compatibilidade
    result_label.config(text=f"Compatibilidade amorosa: {love_value}%")

# Cria a janela principal
window = tk.Tk()
window.title("Love Tester")
window.geometry("500x500") # Define o tamanho da janela

# Cria os campos de entrada de nome
name1_label = tk.Label(window, text="Nome da primeira pessoa:")
name1_label.pack()
name1_entry = tk.Entry(window)
name1_entry.pack()

name2_label = tk.Label(window, text="Nome da segunda pessoa:")
name2_label.pack()
name2_entry = tk.Entry(window)
name2_entry.pack()

# Cria o botão para calcular a compatibilidade
calculate_button = tk.Button(window, text="Calcular compatibilidade", command=calculate_love)
calculate_button.pack()

# Cria o rótulo de resultado
result_label = tk.Label(window, text="")
result_label.pack()

# Inicia o loop principal da janela
window.mainloop()
