# mamba-forever
Need some help with my Python Program






def display_menu():
    print('COMMAND MENU')
    print('view - View Country Name')
    print('add = Add a country')
    print('del - Delete a country')
    print('exit - Exit Program')
    print()

def display_country(countries):
    for code in countries.keys():
        print(code)

def view(countries):
    display_country(countries)
    country_code = input('Enter a country code to search: ')
    country_code = country_code.title()
    if country_code in  countries:
        country = countries[country_code]
        print ('Country code: '+ country() +' .\n')
    else:
        print('There is no country with that code.\n')

def add(countries):
    country = input('Enter a code: ')
    country = country.title()
    if country in countries:
        print(country + 'already exists.\n')
    else:
        country = input('Enter a country code: ')
        countries[country] = country
        print(f'{country} was added.\n')

def delete(countries):
    country: input('Enter a country code')
    country = country.title()
    if country in countries:
        country = country.pop(country)
        print(f'{country} was deleted.\n')
    else:
        print('There is no country with that code.\n')

def main():
    country = {'CA' : 'Canada', 'US' : 'United States', 'MX' : 'Mexico'}
    
    display_menu()
    while True:
        command = input('Command: ')
        command = command.lower()
        if command == 'view':
            view(country)
        elif command == 'add':
            add (country)
        elif command == 'del':
            delete (country)
        elif command == 'exit':
            print('Bye')
            break
        else:
            print('Not valid command. Please try again.\n')

main()
