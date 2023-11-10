# Inseccion
ya vamos a jugar fortnite?

import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;
import java.util.List;



public class insercion_Alumno {
       public static void main(String[] args) {
        List<Estudiante> estudiantes = new ArrayList<>();
        estudiantes.add(new Estudiante("Juan", 101, 85.5, "Informática"));
        estudiantes.add(new Estudiante("Ana", 102, 92.0, "Matemáticas"));
        estudiantes.add(new Estudiante("Elias", 103, 78.5, "Física"));
        estudiantes.add(new Estudiante("David", 144, 74.5, "POO"));
        estudiantes.add(new Estudiante("Miguelito", 187, 97.0, "Quimica"));
        estudiantes.add(new Estudiante("Tilin", 121, 84.5, "Contabilidad"));
        estudiantes.add(new Estudiante("La Changa", 903, 99.5, "Etica"));

        System.out.println("Orden original:");
        imprimirEstudiantes(estudiantes);

        Collections.sort(estudiantes, Comparator.comparing(e -> e.nombre));
        System.out.println("\nOrden por nombre (ascendente):");
        imprimirEstudiantes(estudiantes);

        Collections.sort(estudiantes, Comparator.comparing(Estudiante::getNombre).reversed());
        System.out.println("\nOrden por nombre (descendente):");
        imprimirEstudiantes(estudiantes);
        Collections.sort(estudiantes, Comparator.comparing(e -> e.numeroControl));
        System.out.println("\nOrden por numero de control (ascendente):");
        imprimirEstudiantes(estudiantes);

        Collections.sort(estudiantes, Comparator.comparing(Estudiante::getNumeroControl).reversed());
        System.out.println("\nOrden por numero de control (descendente):");
        imprimirEstudiantes(estudiantes);
                Collections.sort(estudiantes, Comparator.comparing(e -> e.calificacion));
        System.out.println("\nOrden por calificacion (ascendente):");
        imprimirEstudiantes(estudiantes);

        Collections.sort(estudiantes, Comparator.comparing(Estudiante::getCalificacion).reversed());
        System.out.println("\nOrden por calificacion (descendente):");
        imprimirEstudiantes(estudiantes);
                Collections.sort(estudiantes, Comparator.comparing(e -> e.carrera));
        System.out.println("\nOrden por carrera (ascendente):");
        imprimirEstudiantes(estudiantes);

        Collections.sort(estudiantes, Comparator.comparing(Estudiante::getCarrera).reversed());
        System.out.println("\nOrden por carrera (descendente):");
        imprimirEstudiantes(estudiantes);
    }

    private static void imprimirEstudiantes(List<Estudiante> estudiantes) {
        for (Estudiante estudiante : estudiantes) {
            System.out.println(estudiante);
        }
    }
}



--------------------------------------------

public class Estudiante {
     String nombre;
    int numeroControl;
    double calificacion;
    String carrera;

    public Estudiante(String nombre, int numeroControl, double calificacion, String carrera) {
        this.nombre = nombre;
        this.numeroControl = numeroControl;
        this.calificacion = calificacion;
        this.carrera = carrera;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public int getNumeroControl() {
        return numeroControl;
    }

    public void setNumeroControl(int numeroControl) {
        this.numeroControl = numeroControl;
    }

    public double getCalificacion() {
        return calificacion;
    }

    public void setCalificacion(double calificacion) {
        this.calificacion = calificacion;
    }

    public String getCarrera() {
        return carrera;
    }

    public void setCarrera(String carrera) {
        this.carrera = carrera;
    }

    @Override
    public String toString() {
        return "Nombre: " + nombre + ", Número de Control: " + numeroControl + ", Calificación: " + calificacion + ", Carrera: " + carrera;
    }
}
