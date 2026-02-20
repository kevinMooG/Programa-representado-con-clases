public class Alumno {
    //  Atributos privados (encapsulamiento)
    private String nombre;
    private String materia;
    private double calificacion1;
    private double calificacion2;
    private double calificacion3;

    // Getters y Setters
    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public String getMateria() {
        return materia;
    }

    public void setMateria(String materia) {
        this.materia = materia;
    }

    public double getCalificacion1() {
        return calificacion1;
    }

    public void setCalificacion1(double calificacion1) {
        this.calificacion1 = calificacion1;
    }

    public double getCalificacion2() {
        return calificacion2;
    }

    public void setCalificacion2(double calificacion2) {
        this.calificacion2 = calificacion2;
    }

    public double getCalificacion3() {
        return calificacion3;
    }

    public void setCalificacion3(double calificacion3) {
        this.calificacion3 = calificacion3;
    }

    // Método calcular el promedio
    public double calcularPromedio() {
        return (calificacion1 + calificacion2 + calificacion3) / 3;
    }

    // Método para determinar si aprueba
    public String estado() {
        if (calcularPromedio() >= 6) {
            return "APROBADO";
        } else {
            return "REPROBADO";
        }
    }
}
