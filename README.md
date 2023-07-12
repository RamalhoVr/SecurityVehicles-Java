# SecurityVehicles-Java

# Segurança de Veículos - Resumo

Este projeto implementa um sistema para calcular o preço do seguro de veículos com base na idade do proprietário.

## Classes

### Vehicles

- Classe abstrata que representa um veículo.
- Contém atributos para informações gerais do veículo, como cor, placa, chassi, propriedade e idade.
- Possui um atributo estático para armazenar o preço do seguro.
- Contém um método abstrato para calcular o preço do seguro.

### Car

- Subclasse de `Vehicles` que representa um carro.
- Possui um atributo booleano para indicar se o carro possui um degrau.
- Implementa o método `CalculateSecurity` para calcular o preço do seguro com base na idade do proprietário.

### Motocycle

- Subclasse de `Vehicles` que representa uma motocicleta.
- Possui um atributo booleano para indicar se a motocicleta possui um SissyBar.
- Implementa o método `CalculateSecurity` para calcular o preço do seguro com base na idade do proprietário.

### SwitchVehicles

- Classe que contém o método `CalculateSecurity` para calcular o preço do seguro de um veículo genérico.
- Recebe um objeto do tipo `Vehicles` como parâmetro e chama o método `CalculateSecurity` do veículo para calcular o preço do seguro.


# CalculeSecurity

Este programa calcula o preço do seguro para um veículo com base nas escolhas do usuário.

## Lógica do programa:

1. Importa a classe `javax.swing.JOptionPane` para exibir caixas de diálogo para o usuário.

2. Define a classe `CalculeSecurity` que contém o método `main`, que é o ponto de entrada do programa.

3. Declara as variáveis `option` e `age` para armazenar a escolha do tipo de veículo e a idade do usuário, respectivamente.

4. Cria objetos das classes `Car` e `Motocycle` para calcular o preço do seguro.

5. Usa caixas de diálogo para solicitar ao usuário o tipo de veículo e idade.

6. Atribui a idade informada à variável estática `Age` na classe `Vehicles`.

7. Utiliza condicionais para verificar a opção escolhida pelo usuário e chama o método `CalculateSecurity` do objeto de veículo correspondente.

8. Exibe o preço do seguro calculado na tela por meio da caixa de diálogo `JOptionPane`.

# Vehicles

A classe abstrata `Vehicles` é uma classe base para representar veículos e contém a lógica básica relacionada ao cálculo do preço do seguro.

## Lógica do código:

1. A classe `Vehicles` possui uma variável estática `PriceSecurity` para armazenar o preço do seguro.

2. Possui variáveis de instância (`Color`, `Plate`, `Chassis`, `Propierty`) que armazenam informações específicas de cada veículo.

3. Possui uma variável estática `Age` para armazenar a idade do proprietário do veículo.

4. Tem um construtor padrão vazio que pode ser utilizado pelas subclasses.

5. Contém um método abstrato `CalculeSecurity()` que deve ser implementado pelas subclasses para calcular o preço do seguro.

6. O método abstrato retorna `0` por padrão, mas deve ser substituído pelas subclasses para fornecer a implementação real do cálculo do preço do seguro.

# SwitchVehicles

A classe `SwitchVehicles` contém um método que calcula o preço do seguro para um veículo específico.

## Lógica do código:

1. A classe `SwitchVehicles` possui o método `CalculateSecurity`, que recebe um objeto do tipo `Vehicles`.

2. O objetivo deste método é chamar o método `CalculeSecurity()` do objeto `vehicles` e retornar o resultado do cálculo do seguro.

3. O método `CalculateSecurity` retorna um valor do tipo `double`.

4. Ao chamar o método `CalculeSecurity()` no objeto `vehicles`, a implementação específica do cálculo do seguro é executada, pois o método é abstrato na classe `Vehicles` e deve ser implementado pelas subclasses.

5. O cálculo do seguro é realizado de acordo com a implementação da subclasse específica do objeto `vehicles`.

6. O resultado do cálculo do seguro é retornado pelo método `CalculateSecurity`

# Car

A classe `Car` é uma subclasse da classe `Vehicles` e contém métodos específicos para calcular o preço do seguro de um carro com base na idade do usuário.

## Lógica do código:

- A classe `Car` possui uma variável booleana `step` para indicar se o carro possui um degrau.

- Ela possui um construtor padrão que chama o construtor da classe pai (`Vehicles`).

- O método `CalculateSecurity` é responsável por calcular o preço do seguro com base na idade fornecida como parâmetro.

- O preço do seguro é calculado de acordo com a faixa etária do motorista:
  - Se a idade for 18 anos, o preço é calculado multiplicando 5228.87 por 1.075.
  - Se a idade for maior que 18 anos, o preço é calculado multiplicando 2851.75 por 1.15.
  - Se a idade estiver entre 30 e 50 anos, o preço é calculado multiplicando 3041.78 por 1.25.
  - Se a idade for menor que 18 anos, o preço é 1.
  - Para qualquer outra idade, o preço é calculado multiplicando 3365.15 por 1.30.

- O preço do seguro calculado é atribuído à variável `PriceSecurity` da classe pai (`Vehicles`).
- 
# Motocycle

A classe `Motocycle` é uma subclasse da classe `Vehicles` e representa uma motocicleta. Ela contém a lógica necessária para calcular o preço do seguro com base na idade do proprietário.

## Atributos

- `SissyBar` (boolean): indica se a motocicleta possui um SissyBar.

## Construtor

- `Motocycle()`: o construtor padrão que chama o construtor da classe pai (`Vehicles`).

## Métodos

- `CalculateSecurity(int Age)`: método responsável por calcular o preço do seguro da motocicleta com base na idade do proprietário. A lógica é a seguinte:

  - Se a idade for 18 anos, o preço do seguro é calculado multiplicando 5228.87 por 1.12.
  - Se a idade for maior que 18 anos, o preço do seguro é calculado multiplicando 2851.75 por 1.20.
  - Se a idade estiver entre 30 e 50 anos, o preço do seguro é calculado multiplicando 3041.78 por 1.15.
  - Se a idade for menor que 18 anos, o preço do seguro é 1.
  - Para qualquer outra idade, o preço do seguro é calculado multiplicando 3365.15 por 1.10.

# SecurityVehicles-Java

## Vehicle Security - Summary

This project implements a system to calculate the price of vehicle insurance based on the owner's age.

## Classes

### Vehicles

- Abstract class representing a vehicle.
- Contains attributes for general vehicle information such as color, plate, chassis, ownership, and age.
- Includes a static attribute to store the insurance price.
- Contains an abstract method to calculate the insurance price.

### Car

- Subclass of `Vehicles` representing a car.
- Has a boolean attribute to indicate if the car has a step.
- Implements the `CalculateSecurity` method to calculate the insurance price based on the owner's age.

### Motorcycle

- Subclass of `Vehicles` representing a motorcycle.
- Has a boolean attribute to indicate if the motorcycle has a SissyBar.
- Implements the `CalculateSecurity` method to calculate the insurance price based on the owner's age.

### SwitchVehicles

- Class that contains the `CalculateSecurity` method to calculate the insurance price of a generic vehicle.
- Receives an object of type `Vehicles` as a parameter and calls the `CalculateSecurity` method of the vehicle to calculate the insurance price.

# CalculeSecurity

This program calculates the insurance price for a vehicle based on user choices.

## Program Logic:

1. Import the `javax.swing.JOptionPane` class to display dialog boxes to the user.

2. Define the `CalculeSecurity` class which contains the `main` method, the entry point of the program.

3. Declare the `option` and `age` variables to store the user's choice of vehicle type and age, respectively.

4. Create objects of the `Car` and `Motorcycle` classes to calculate the insurance price.

5. Use dialog boxes to prompt the user for the vehicle type and age.

6. Assign the provided age to the static `Age` variable in the `Vehicles` class.

7. Use conditionals to check the user's chosen option and call the `CalculateSecurity` method of the corresponding vehicle object.

8. Display the calculated insurance price on the screen using the `JOptionPane` dialog box.

# Vehicles

The abstract class `Vehicles` is a base class for representing vehicles and contains the basic logic related to calculating the insurance price.

## Code Logic:

1. The `Vehicles` class has a static variable `PriceSecurity` to store the insurance price.

2. It has instance variables (`Color`, `Plate`, `Chassis`, `Property`) that store specific vehicle information.

3. It has a static variable `Age` to store the vehicle owner's age.

4. It has an empty default constructor that can be used by subclasses.

5. It contains an abstract method `CalculateSecurity()` that must be implemented by subclasses to calculate the insurance price.

6. The abstract method returns `0` by default but should be overridden by subclasses to provide the actual implementation of the insurance price calculation.

# SwitchVehicles

The `SwitchVehicles` class contains a method that calculates the insurance price for a specific vehicle.

## Code Logic:

1. The `SwitchVehicles` class has the `CalculateSecurity` method, which receives an object of type `Vehicles`.

2. The purpose of this method is to call the `CalculateSecurity` method of the `vehicles` object and return the result of the insurance calculation.

3. The `CalculateSecurity` method returns a value of type `double`.

4. By calling the `CalculateSecurity` method on the `vehicles` object, the specific implementation of the insurance calculation is executed, as the method is abstract in the `Vehicles` class and must be implemented by subclasses.

5. The insurance calculation is performed according to the specific subclass implementation of the `vehicles` object.

6. The result of the insurance calculation is returned by the `CalculateSecurity` method.

# Car

The `Car` class is a subclass of the `Vehicles` class and contains specific methods to calculate the insurance price for a car based on the user's age.

## Code Logic:

- The `Car` class has a boolean variable `step` to indicate if the car has a step.

- It has a default constructor that calls the parent class (`Vehicles`) constructor.

- The `CalculateSecurity` method is responsible for calculating the insurance price based on the provided age parameter.

- The insurance price is calculated based on the driver's age range:
  - If the age is 18 years, the price is calculated by multiplying 5228.87 by 1.075.
  - If the age is above 18 years, the price is calculated by multiplying 2851.75 by 1.15.
  - If the age is between 30 and 50 years, the price is calculated by multiplying 3041.78 by 1.25.
  - If the age is below 18 years, the price is 1.
  - For any other age, the price is calculated by multiplying 3365.15 by 1.30.

- The calculated insurance price is assigned to the `PriceSecurity` variable in the parent class (`Vehicles`).

# Motorcycle

The `Motorcycle` class is a subclass of the `Vehicles` class and represents a motorcycle. It contains the necessary logic to calculate the insurance price based on the owner's age.

## Attributes

- `SissyBar` (boolean): indicates if the motorcycle has a SissyBar.

## Constructor

- `Motorcycle()`: the default constructor that calls the parent class (`Vehicles`) constructor.

## Methods

- `CalculateSecurity(int Age)`: method responsible for calculating the insurance price for the motorcycle based on the owner's age. The logic is as follows:

  - If the age is 18 years, the insurance price is calculated by multiplying 5228.87 by 1.12.
  - If the age is above 18 years, the insurance price is calculated by multiplying 2851.75 by 1.20.
  - If the age is between 30 and 50 years, the insurance price is calculated by multiplying 3041.78 by 1.15.
  - If the age is below 18 years, the insurance price is 1.
  - For any other age, the insurance price is calculated by multiplying 3365.15 by 1.10.


