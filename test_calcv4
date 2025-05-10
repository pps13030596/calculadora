import unittest
from unittest.mock import patch, call
from main import calculadora

class TestCalculadoraInteractiva(unittest.TestCase):

    @patch("builtins.input", side_effect=["1", "3", "2", "5"])
    @patch("builtins.print")
    def test_suma(self, mock_print, mock_input):
        calculadora()
        mock_print.assert_has_calls([
            call("\nCalculadora Básica en Python"),
            call("Selecciona una operación:"),
            call("1. Suma"),
            call("2. Resta"),
            call("3. Multiplicación"),
            call("4. División"),
            call("5. Salir"),
            call("Resultado: 5.0"),
        ])

    @patch("builtins.input", side_effect=["2", "5", "3", "5"])
    @patch("builtins.print")
    def test_resta(self, mock_print, mock_input):
        calculadora()
        mock_print.assert_has_calls([
            call("\nCalculadora Básica en Python"),
            call("Resultado: 2.0"),
        ])

    @patch("builtins.input", side_effect=["3", "2", "3", "5"])
    @patch("builtins.print")
    def test_multiplicacion(self, mock_print, mock_input):
        calculadora()
        mock_print.assert_has_calls([
            call("\nCalculadora Básica en Python"),
            call("Resultado: 6.0"),
        ])

    @patch("builtins.input", side_effect=["4", "6", "3", "5"])
    @patch("builtins.print")
    def test_division(self, mock_print, mock_input):
        calculadora()
        mock_print.assert_has_calls([
            call("\nCalculadora Básica en Python"),
            call("Resultado: 2.0"),
        ])

    @patch("builtins.input", side_effect=["4", "6", "0", "5"])
    @patch("builtins.print")
    def test_division_por_cero(self, mock_print, mock_input):
        calculadora()
        mock_print.assert_any_call("No se puede dividir por cero")

    @patch("builtins.input", side_effect=["5"])
    @patch("builtins.print")
    def test_salir(self, mock_print, mock_input):
        calculadora()
        mock_print.assert_any_call("Hasta luego!")

if __name__ == '__main__':
    unittest.main()
