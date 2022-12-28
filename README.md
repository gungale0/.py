# .pydef process_address(address):
    last_digit_index = max([i for i in range(len(address)) if address[i].isdigit()])
    street = address[:last_digit_index].strip()
    number = address[last_digit_index:].strip()

    return (street, number)

# Casos de teste
assert process_address("Miritiba 339") == ("Miritiba", "339")
assert process_address("Babaçu 500") == ("Babaçu", "500")
assert process_address("Cambuí 804B") == ("Cambuí", "804B")
assert process_address("Rio Branco 23") == ("Rio Branco", "23")
assert process_address("Quirino dos Santos 23 b") == ("Quirino dos Santos", "23 b")
assert process_address("4, Rue de la République") == ("Rue de la République", "4")
assert process_address("100 Broadway Av") == ("Broadway Av", "100")
assert process_address("Calle Sagasta, 26") == ("Calle Sagasta", "26")
assert process_address("Calle 44 No 1991") == ("Calle 44", "No 1991")

print("Todos os testes passaram!")
