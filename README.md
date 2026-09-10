-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Grupo 5 
Integrantes:
- Sandra Alulema
- Anthony Armas
- Joselyn Guaman
- Valentina Ortiz
- Andres Vayas
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
import java.util.ArrayList;
import java.util.List;

/**
 * Genera una tabla de aportes en formato Markdown para GitHub (README.md),
 * siguiendo la estructura de la imagen de referencia:
 * Integrante | Usuario GitHub | Rol | Actividad realizada | PR | Commit
 */
public class TablaAportes {

    static class Integrante {
        String nombre;
        String usuarioGitHub;
        String rol;
        String actividad;
        String pr;
        String commitTag;

        Integrante(String nombre, String usuarioGitHub, String rol, String actividad, String pr, String commitTag) {
            this.nombre = nombre;
            this.usuarioGitHub = usuarioGitHub;
            this.rol = rol;
            this.actividad = actividad;
            this.pr = pr;
            this.commitTag = commitTag;
        }
    }

    public static void main(String[] args) {
        List<Integrante> equipo = new ArrayList<>();

        // TODO: reemplaza los valores de usuario, rol, actividad, PR y commit
        // de cada integrante con la información real del proyecto.
        equipo.add(new Integrante("Sandra Alulema", "@SandraAlulema", "Rol pendiente", "Actividad pendiente", "#1", "feat(pendiente)"));
        equipo.add(new Integrante("Anthony Armas", "@AnthonyArmas", "Rol pendiente", "Actividad pendiente", "#2", "feat(pendiente)"));
        equipo.add(new Integrante("Joselyn Guaman", "@JoselynGuaman", "Rol pendiente", "Actividad pendiente", "#3", "feat(pendiente)"));
        equipo.add(new Integrante("Valentina Ortiz", "@ValentinaOrtiz", "Rol pendiente", "Actividad pendiente", "#4", "feat(pendiente)"));
        equipo.add(new Integrante("Andrés Vayas", "@AndresVayas", "Rol pendiente", "Actividad pendiente", "#5", "feat(pendiente)"));

        System.out.println(generarTablaMarkdown(equipo));
    }

    static String generarTablaMarkdown(List<Integrante> equipo) {
        StringBuilder sb = new StringBuilder();

        sb.append("| Integrante | Usuario GitHub | Rol | Actividad realizada | PR | Commit |\n");
        sb.append("|---|---|---|---|---|---|\n");

        for (Integrante i : equipo) {
            sb.append("| ").append(i.nombre)
              .append(" | ").append(i.usuarioGitHub)
              .append(" | ").append(i.rol)
              .append(" | ").append(i.actividad)
              .append(" | ").append(i.pr)
              .append(" | ").append(i.commitTag)
              .append(" |\n");
        }

        return sb.toString();
    }
}
