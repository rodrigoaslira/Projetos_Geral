# Projetos_Geral
 class Contato:
    def __init__(self, nome, telefone, email):
        self.set_nome(nome)
        self.set_telefone(telefone)
        self.set_email(email)

    def get_nome(self):
        return self.__nome

    def set_nome(self, novo_nome):
        if not isinstance(novo_nome, str) or not novo_nome.strip():
            raise ValueError("Nome inválido")
        self.__nome = novo_nome.strip()

    def get_telefone(self):
        return self.__telefone

    def set_telefone(self, novo_telefone):
        if not re.match(r"^\d{10}$", novo_telefone):
            raise ValueError("Telefone inválido")
        self.__telefone = novo_telefone

    def get_email(self):
        return self.__email

    def set_email(self, novo_email):
        if not re.match(r"^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$", novo_email):
            raise ValueError("E-mail inválido")
        self.__email = novo_email
