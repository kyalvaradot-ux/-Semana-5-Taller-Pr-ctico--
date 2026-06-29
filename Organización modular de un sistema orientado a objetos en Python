restaurante_app/
│
├── modelos/
│   ├── __init__.py
│   ├── producto.py
│   └── cliente.py
│
├── servicios/
│   ├── __init__.py
│   └── restaurante.py
│
└── main.py

README.md
Modelos/producto.py
class Producto:
    """Representa un producto del restaurante."""

    def __init__(self, nombre: str, precio: float, categoria: str, disponible: bool):
        self.nombre = nombre
        self.precio = precio
        self.categoria = categoria
        self.disponible = disponible

    def __str__(self):
        estado = "Disponible" if self.disponible else "No disponible"
        return f"{self.nombre} | {self.categoria} | ${self.precio:.2f} | {estado}"
modelos/cliente.py
class Cliente:
    """Representa un cliente del restaurante."""

    def __init__(self, nombre: str, edad: int, telefono: str, frecuente: bool):
        self.nombre = nombre
        self.edad = edad
        self.telefono = telefono
        self.frecuente = frecuente

    def __str__(self):
        tipo = "Cliente frecuente" if self.frecuente else "Cliente nuevo"
        return f"{self.nombre} | {self.edad} años | {self.telefono} | {tipo}"
Servicios/restaurante.py
from modelos.producto import Producto
from modelos.cliente import Cliente


class Restaurante:

    def __init__(self, nombre: str):
        self.nombre = nombre
        self.productos: list[Producto] = []
        self.clientes: list[Cliente] = []

    def agregar_producto(self, producto: Producto):
        self.productos.append(producto)

    def agregar_cliente(self, cliente: Cliente):
        self.clientes.append(cliente)

    def mostrar_productos(self):
        print("\nPRODUCTOS")
        print("-----------------------------")
        for producto in self.productos:
            print(producto)

    def mostrar_clientes(self):
        print("\nCLIENTES")
        print("-----------------------------")
        for cliente in self.clientes:
            print(cliente)
main.py
from modelos.producto import Producto
from modelos.cliente import Cliente
from servicios.restaurante import Restaurante

# Crear restaurante
restaurante = Restaurante("Restaurante Sabor Andino")

# Crear productos
producto1 = Producto("Arroz con pollo", 6.50, "Plato fuerte", True)
producto2 = Producto("Jugo de mora", 2.25, "Bebida", True)

# Crear clientes
cliente1 = Cliente("Kelly Alvarado", 20, "0991234567", True)
cliente2 = Cliente("Carlos Pérez", 25, "0987654321", False)

# Agregar productos
restaurante.agregar_producto(producto1)
restaurante.agregar_producto(producto2)

# Agregar clientes
restaurante.agregar_cliente(cliente1)
restaurante.agregar_cliente(cliente2)

# Mostrar información
print("=" * 40)
print(restaurante.nombre)
print("=" * 40)

restaurante.mostrar_productos()
restaurante.mostrar_clientes()
