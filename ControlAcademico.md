# Programa-representado-con-clases
CODIGOS FUENTES
import java.util.Scanner;

public class ControlAcademico {
    public static void main(String[] args) {
        Scanner teclado = new Scanner(System.in);
        Alumno alumno = new Alumno();
        int opcion;

        do {
            System.out.println("\n=== CONTROL ACADEMICO ===");
            System.out.println("1. Registrar nombre");
            System.out.println("2. Registrar materia");
            System.out.println("3. Capturar calificaciones");
            System.out.println("4. Mostrar resultados");
            System.out.println("5. Salir");
            System.out.print("Seleccione una opción: ");
            opcion = teclado.nextInt();
            teclado.nextLine(); // limpiar buffer

            switch (opcion) {
                case 1:
                    System.out.print("Ingrese el nombre del alumno: ");
                    alumno.setNombre(teclado.nextLine());
                    break;

                case 2:
                    System.out.print("Ingrese la materia: ");
                    alumno.setMateria(teclado.nextLine());
                    break;

                case 3:
                    System.out.print("Calificación 1: ");
                    alumno.setCalificacion1(teclado.nextDouble());
                    System.out.print("Calificación 2: ");
                    alumno.setCalificacion2(teclado.nextDouble());
                    System.out.print("Calificación 3: ");
                    alumno.setCalificacion3(teclado.nextDouble());
                    break;

                case 4:
                    System.out.println("\n--- RESULTADOS ---");
                    System.out.println("Alumno: " + alumno.getNombre());
                    System.out.println("Materia: " + alumno.getMateria());
                    System.out.println("Promedio: " + alumno.calcularPromedio());
                    System.out.println("Estado: " + alumno.estado());
                    break;

                case 5:
                    System.out.println("Programa finalizado.");
                    break;

                default:
                    System.out.println("Opción inválida intente de nuevo.");
            }
        } while (opcion != 5);

        teclado.close();
    }
}
