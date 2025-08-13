# ProyectoProgra-Diagrama.md
```mermaid
classDiagram
    class Grupo3_Sistema_Gimnasio {
        +main()
    }

    class Menu {
        +mostrarMenu()
    }

    class Metodos {
        +generarDataInicialActividaddes()
        +dividirClases()
        +crearClases()
        +editarClases()
        +eliminarClase()
        +registrarSocioClase()
        +eliminarSocioDeClase()
        +salaPesas()
        +llenarCabinas()
        +reservarCabina()
        +mostrarReservarCabinas()
        +eliminarReservaDecabina()
        +mostrarHorarioAuditorio()
        +inscribirSocioAuditorio()
        +mostrarInscritosAuditorio()
        +eliminarSocioInscripcion()
        +inicializarEspaciosRecreativos()
        +visualizarEspaciosRecreativosDisponibles()
        +reservarEspacioRecreativo()
        +cancelarReservaRecreativoOPingPong()
        +parqueo()
    }

    class espaciossRecreativos {
        -capacidadMaxima
        -capacidadActual
        +registrarEntrada()
        +registrarSalida()
        +verCapacidad()
    }

    class PingPong {
        -reservas
        +getReservas()
        +setFecha()
    }

    class Parqueo {
        +inicializarNiveles()
        +asignarEspacio()
    }

    class Actividad {
        -nombreActividad
        -momento
        -horario
        -numeroUnico
        -capacidadActividad
        -cantidadActual
        +getSocios()
    }

    class GUI {
        +interfazGrafica()
    }

    %% Relaciones
    Grupo3_Sistema_Gimnasio --> Menu : ejecuta
    Menu --> Metodos : usa
    Metodos --> Actividad : gestiona
    Metodos --> espaciossRecreativos : controla
    Metodos --> PingPong : reserva
    Metodos --> Parqueo : administra
    GUI --> Metodos : interactúa

    ```
