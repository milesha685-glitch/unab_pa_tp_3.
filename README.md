# unab_pa_tp_3.
1. Entender y comprender ejercicios prácticos
2.  Trabajar en grupos
3.  Manejo de IDE (cualquiera a elección)
4.  Manejo de programación básica en Python
5.   Manejo de conceptos vinculados a POO
6.  Manejo básico de Git y GitHub (crear repositorio y subir archivos)
Ejercicio 2:
class Punto:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    # Devuelve el valor de x
    def eje_x(self):
        return self.x

    # Devuelve el valor de y
    def eje_y(self):
        return self.y

    # Representación en string
    def impresion(self):
        return f"Punto({self.x}, {self.y})"

    # Devuelve el punto opuesto
    def opuesto(self):
        return Punto(-self.x, -self.y)

    # Método adicional: distancia al origen
    def distancia_al_origen(self):
        return (self.x**2 + self.y**2) ** 0.5

    # Método adicional: distancia a otro punto
    def distancia_a(self, otro_punto):
        return ((self.x - otro_punto.x)**2 + (self.y - otro_punto.y)**2) ** 0.5

    # Método adicional: mover el punto
    def mover(self, dx, dy):
        self.x += dx
        self.y += dy
    Ejercicio 3:
    class Punto:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def impresion(self):
        return f"({self.x}, {self.y})"

class Punto:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def impresion(self):
        return f"({self.x}, {self.y})"


class Linea:
    # Constructor
    def __init__(self, punto_a, punto_b):
        self._punto_a = punto_a
        self._punto_b = punto_b

    # Mueve la línea hacia la derecha
    def mueve_derecha(self, distancia):
        self._punto_a.x += distancia
        self._punto_b.x += distancia

    # Mueve la línea hacia la izquierda
    def mueve_izquierda(self, distancia):
        self._punto_a.x -= distancia
        self._punto_b.x -= distancia

    # Mueve la línea hacia arriba
    def mueve_arriba(self, distancia):
        self._punto_a.y += distancia
        self._punto_b.y += distancia

    # Mueve la línea hacia abajo
    def mueve_abajo(self, distancia):
        self._punto_a.y -= distancia
        self._punto_b.y -= distancia

    # Método adicional: mostrar la línea
    def impresion(self):
        return f"Línea desde {self._punto_a.impresion()} hasta {self._punto_b.impresion()}"
