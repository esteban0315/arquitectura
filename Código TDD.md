# arquitectura
Codigo test
using Microsoft.VisualStudio.TestTools.UnitTesting;
using Modelo.BaseDatos;
using Modelo.Repositorios;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ProyectoUrgencias.Tests
{
    [TestClass]
    public class AcompananteTest
    {
        [TestMethod]
        public void CalcularCuotaEstrato1()
        {
            //Arrange --> Declarar las variables de prueba
            int estrato = 1;
            double? valorEsperado = 3200;
            double? valorReal = 0;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.CalcularCuota(estrato);

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void CalcularCuotaEstrato2()
        {
            //Arrange --> Declarar las variables de prueba
            int estrato = 2;
            double? valorEsperado = 4000;
            double? valorReal = 0;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.CalcularCuota(estrato);

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void CalcularCuotaEstrato3()
        {
            //Arrange --> Declarar las variables de prueba
            int estrato = 3;
            double? valorEsperado = 7000;
            double? valorReal = 0;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.CalcularCuota(estrato);

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void CalcularCuotaEstrato4()
        {
            //Arrange --> Declarar las variables de prueba
            int estrato = 4;
            double? valorEsperado = 14000;
            double? valorReal = 0;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.CalcularCuota(estrato);

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void CalcularCuotaEstrato5()
        {
            //Arrange --> Declarar las variables de prueba
            int estrato = 5;
            double? valorEsperado = 20000;
            double? valorReal = 0;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.CalcularCuota(estrato);

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void CalcularCuotaEstrato6()
        {
            //Arrange --> Declarar las variables de prueba
            int estrato = 6;
            double? valorEsperado = 32000;
            double? valorReal = 0;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.CalcularCuota(estrato);

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void ConsultaExistenciaPaciente()
        {
            //Arrange --> Declarar las variables de prueba
            int idPaciente = 1;
            bool valorEsperado = true;
            bool valorReal;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.ConsultaPaciente(idPaciente) != null;

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        public void ConsultaNoExistenciaPaciente()
        {
            //Arrange --> Declarar las variables de prueba
            int idPaciente = -1;
            bool valorEsperado = false;
            bool valorReal;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.ConsultaPaciente(idPaciente) != null;

            //Assert -> Validar los resultados
            Assert.AreEqual(valorEsperado, valorReal);
        }

        [TestMethod]
        [ExpectedException(typeof(ArgumentNullException))]
        public void InsertarAcompanante()
        {
            //Arrange --> Declarar las variables de prueba
            Acompanante acompanante = null;
            bool valorReal;
            var repositorio = new UrgenciasRepositorio();

            //Act -> Realizar la prueba  o ejecucion del metodo
            valorReal = repositorio.InsertarAcompanante(acompanante);

            //Assert es manejado por la excepcion  
        }
    }
}
