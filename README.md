# Hello-word-
Mi primer Github de prueba 
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace DatosPersonales
{
   public class Metodos
    {
        public int CalcularEdad(DateTime fechanacimiento) //Parametro de entrada DateTime fechanacimiento
        {
            //Console.WriteLine("Ingresa tu feha de nacimiento con el formato: dd/mm/aa");
            //fechanacimiento = DateTime.Parse(Console.ReadLine());
            //DateTime fecha = DateTime.Now;
            //Console.WriteLine("La fecha actual es: "+fecha);
            int edad = DateTime.Today.AddTicks(-fechanacimiento.Ticks).Year - 1; //Calcula la edad utilizando la fecha de nacimiento y la fecha actual
            //Console.WriteLine("La edad que tienes es: " + edad);
            return edad; 
        }

        public string ObtenerNombreCompleto(string primernombre, string segundonombre, string apellidopaterno, string apellidomaterno) //Parametros de entrada
        {
            //Console.WriteLine("Ingresa tu primer nombre");
            //primernombre = Console.ReadLine();
            //Console.WriteLine("Ingresa tu segundo nombre");
            //segundonombre = Console.ReadLine();
            //Console.WriteLine("Ingresa tu apellido paterno");
            //apellidopaterno = Console.ReadLine();
            //Console.WriteLine("Ingresa tu apellido materno");
            //apellidomaterno = Console.ReadLine();
            string nombrecompleto = ""; //
            if (!string.IsNullOrEmpty(segundonombre)) //pregunta si la cadena es nula o esta vacia--IsNullOrEmpty || El if funciona para preguntar Si segundo nombre es diferente de nulo o vacio
            {
                nombrecompleto = primernombre + " " + segundonombre + " " + apellidopaterno + " " + apellidomaterno;
            }
            else
            {
                nombrecompleto = primernombre + " " + apellidopaterno + " " + apellidomaterno;
            }
            return nombrecompleto;
        }
    }
}
