import os
import shutil

# Função para criar um novo diretório
def create_directory(directory_name):
    if not os.path.exists(directory_name):
        os.makedirs(directory_name)
        print(f"Diretório '{directory_name}' criado com sucesso.")
    else:
        print(f"Erro: Diretório '{directory_name}' já existe.")

# Função para excluir um diretório existente
def delete_directory(directory_name):
    try:
        shutil.rmtree(directory_name)
        print(f"Diretório '{directory_name}' excluído com sucesso.")
    except FileNotFoundError:
        print(f"Erro: Diretório '{directory_name}' não encontrado.")

# Função para renomear um diretório
def rename_directory(old_name, new_name):
    try:
        os.rename(old_name, new_name)
        print(f"Diretório '{old_name}' renomeado para '{new_name}'.")
    except FileNotFoundError:
        print(f"Erro: Diretório '{old_name}' não encontrado.")

# Função para listar os arquivos em um diretório
def list_files_in_directory(directory_name):
    try:
        files = os.listdir(directory_name)
        print(f"Arquivos em '{directory_name}':")
        for file in files:
            print(f"- {file}")
    except FileNotFoundError:
        print(f"Erro: Diretório '{directory_name}' não encontrado.")

# Função para criar um arquivo em um diretório
def create_file(directory_name, file_name, file_content):
    file_path = os.path.join(directory_name, file_name)
    with open(file_path, 'w') as file:
        file.write(file_content)
    print(f"Arquivo '{file_name}' criado em '{directory_name}' com sucesso.")

# Menu de escolhas
while True:
    print("\n=== Menu ===")
    print("1. Criar Novo Diretório")
    print("2. Excluir Diretório Existente")
    print("3. Renomear Diretório")
    print("4. Criar Arquivo em Diretório")
    print("5. Listar Arquivos no Diretório")
    print("6. Sair")

    choice = input("Escolha uma opção (1-6): ")

    if choice == '1':
        new_directory = input("Digite o nome do novo diretório: ")
        create_directory(new_directory)

    elif choice == '2':
        existing_directory = input("Digite o nome do diretório a ser excluído: ")
        delete_directory(existing_directory)

    elif choice == '3':
        old_name = input("Digite o nome do diretório a ser renomeado: ")
        new_name = input("Digite o novo nome para o diretório: ")
        rename_directory(old_name, new_name)

    elif choice == '4':
        directory_to_create_file = input("Digite o nome do diretório para criar o arquivo: ")
        file_name = input("Digite o nome do arquivo: ")
        file_content = input("Digite o conteúdo do arquivo: ")
        create_file(directory_to_create_file, file_name, file_content)

    elif choice == '5':
        directory_to_list = input("Digite o nome do diretório para listar os arquivos: ")
        list_files_in_directory(directory_to_list)

    elif choice == '6':
        print("Encerrando o programa. Até mais!")
        break

    else:
        print("Opção inválida. Por favor, escolha uma opção válida.")
