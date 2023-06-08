# README.md

[TOC]

Documentation
=============
This script is designed to calculate subnetting using VLSM (Variable Length Subnet Masking). It is considered useful in cases where a specific number of hosts is needed for different subnets within the same network. Below is a detailed description of the functions and how to use this script.


Overview
-------------
This Python script allows users to input a network address and a set of numbers representing the required number of hosts in each subnet. With this information, the script calculates the necessary subnet masks for each subnet and provides additional information such as the network address, usable IP address range, broadcast address, subnet mask, and number of addressable hosts.

Requisitos
-------------
This script requires Python 3 and the 'colored' library for coloring text in the terminal. To install 'colored', you can use pip:

`pip install colored`

Functions in the script
-------------
The script contains several functions that perform various tasks:

| Functions | Description                    |
| ------------- | ------------------------------ |
| `is_empty(text)`      | 	Checks if the given text is empty.      |
| `is_correct_network_address(address)`   | Checks if the entered network address is valid.     |
| `is_correct_endpoint_numbers_per_network(numbers)`      | Checks if the entered endpoint numbers per network are valid.
| `is_correct_prefix(prefix)`      | Checks if the entered endpoint numbers per network are valid.      |
| `power_bit_length(x)`      | Returns the number of bits required to represent a given number.      |
| `get_mask_from_prefix(prefix)`      | Returns the subnet mask based on the entered prefix.  |
| `get_32bit_format(ip_address)`      | Converts an IP address to its 32-bit binary representation.|
| `get_ip_from_32bit_format(format_32bit)`      | Converts a 32-bit binary representation to an IP address.     |
| `get_first_addressable_ip(network_ip)`      | Gets the first addressable IP of the subnet.  |
| `get_last_addressable_ip(network_ip, mask)`      |  Gets the last addressable IP of the subnet.      |
| `get_broadcast_ip(network_ip, mask)`      | Calculates the broadcast IP address of the subnet  |
| `get_next_network_ip(network_ip, mask)`      |	Gets the next network address.    |
| `calculate_vlsm(network_ip, endpoint_numbers_per_network, prefix)`      | Performs VLSM calculations and returns the subnets.     |
| `inject_data_to_dict(network_ip, length_of_subnets, subnets)`      | Injects the calculated data into a dictionary.      |
| `main()`      |The main function that takes user inputs and calls other functions.
  |

How to Use
-------------
1. Run the Python script in your terminal.
`py vlsm.py`
2. When prompted, enter the initial network address.
3. Next, enter the number of hosts required in each subnet, separated by commas.

4. Finally, you can optionally enter a subnet mask prefix.

5. The script will return the subnet information for each provided number of hosts.


Documentación 
=============

Este script está diseñado para calcular la subnetización utilizando VLSM (Variable Length Subnet Masking). Se considera útil en casos donde se necesita un número específico de hosts para diferentes subredes dentro de la misma red. A continuación, se proporciona una descripción detallada de las funciones y cómo utilizar este script.

Descripción general
-------------
Este script de Python permite a los usuarios introducir una dirección de red y un conjunto de números que representan la cantidad de hosts requeridos en cada subred. Con esta información, el script calcula las máscaras de subred necesarias para cada subred y proporciona información adicional, como la dirección de red, el rango de direcciones IP utilizables, la dirección de difusión, la máscara de subred y el número de hosts direccionables.
Requisitos
-------------
Este script requiere Python 3 y la biblioteca 'colored' para colorear el texto en la terminal. Para instalar 'colored', puede utilizar pip:

`pip install colored`

Funciones en el script
-------------
El script contiene varias funciones que realizan una variedad de tareas:

| Funciones | Descripción                    |
| ------------- | ------------------------------ |
| `is_empty(text)`      | Comprueba si el texto dado está vacío..       |
| `is_correct_network_address(address)`   | Comprueba si la dirección de red introducida es válida.     |
| `is_correct_endpoint_numbers_per_network(numbers)`      | Comprueba si el número de endpoints por red introducido es válido.
| `is_correct_prefix(prefix)`      | Comprueba si el prefijo de subred introducido es válido.       |
| `power_bit_length(x)`      | Devuelve el número de bits necesarios para representar un número dado.      |
| `get_mask_from_prefix(prefix)`      | Comprueba si el texto dado está vacío..      |
| `get_32bit_format(ip_address)`      | Convierte una dirección IP en su representación binaria de 32 bits. |
| `get_ip_from_32bit_format(format_32bit)`      | Convierte una representación binaria de 32 bits en una dirección IP.      |
| `get_first_addressable_ip(network_ip)`      |  Obtiene la primera dirección IP direccionable de la subred.     |
| `get_last_addressable_ip(network_ip, mask)`      |  Obtiene la última dirección IP direccionable de la subred.       |
| `get_broadcast_ip(network_ip, mask)`      | Calcula la dirección IP de difusión de la subred.    |
| `get_next_network_ip(network_ip, mask)`      |Obtiene la dirección de la próxima red.       |
| `calculate_vlsm(network_ip, endpoint_numbers_per_network, prefix)`      | Realiza los cálculos VLSM y devuelve las subredes.      |
| `inject_data_to_dict(network_ip, length_of_subnets, subnets)`      | Inyecta los datos calculados en un diccionario.      |
| `main()`      |La función principal que toma las entradas del usuario y llama a las otras funciones.  |

Cómo usar
-------------
1. Ejecute el script de Python en su terminal.
`py vlsm.py`
2. Cuando se le solicite, introduzca la dirección de red inicial.
3. A continuación, introduzca el número de hosts que se requieren en cada subred, separados por comas.
4. Finalmente, puede introducir un prefijo de máscara de subred opcional.
5. El script devolverá la información de la subred para cada número de hosts que haya proporcionado.
