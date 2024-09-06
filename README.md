
# Proyecto de mi aplicativo


## ¿En que consiste?

Este proyecto se va a consistir en varias fases, por el cual 
tenemos pensado destacar, para empezar el aplicativo va ser 
para un area de restaurante por el cual se consiste en una 
facturacion que se puede utilizar en diferentes areas, en este caso en un area como un restaurante de comida rapida.


Ahora bien decia que se va a dividir en varias fases, una de ella es en que arquitectura de cloud computing vamos a utilizar 


### Google cloud:
¿Por que es una de las mejores opciones para este proyecto?

por que Google Cloud Platform nos aporta todas las herramientas necesarias para diseñar, hacer testings y lanzar aplicaciones desde gcloud con mucha más seguridad y escalabilidad que cualquier otra herramienta, gracias a la propia infraestructura con la que Google cuenta.

Como muy dice nos da oportunidad para lanzar aplicaciones, por ende es algo que queremos hacer, un aplicativo de facturacion para los restaurantes.

Una de las caracteristicas de esta arquitectura es la siguiente:

Seguro: Google Cloud  cuenta con la infraestructura de Google, nos da fiabilidad y disponibilidad. Sin ningún periodo inactivo programado. Por otro lado, usa sus redes privadas, por lo que los ciberataques son prácticamente imposibles.

Innovador: Se tratan de herramientas modernas, con las últimas novedades del mercado, lo cual permitirá que mi aplicativo esté en un transfondo mas  digital.

Asequible: Algunas de sus herramientas, de hecho, son gratis. Y las que son de pago, tienen precios muy competitivos con diferentes planes; para que cualquier empresa, por grande o pequeña que sea, se pueda beneficiar de los beneficios de Gcloud.


Ya hablamos de la arquitectura, ahora hablemos de la virtualizacion que se utilizara:

### Virtualizacion de aplicaciones

En este caso nosostros elegimos esta virtualizacion ya que es mas abierta a nuestro sistema, ya que es un aplicacion que se desarrollara en bloque que son: 

- Codigo(java)
- Base de datos(Mysql)
- Interfaz grafica

Ahora bien pasemos a las caracteristicas donde me interesa demostrar otras razones de su uso:

- Aislamiento: La aplicación funciona independientemente del sistema operativo y otros programas, evitando conflictos entre aplicaciones y dependencias.

- Portabilidad: Las aplicaciones virtualizadas pueden ejecutarse en diferentes dispositivos o entornos sin necesidad de modificaciones.

- Fácil implementación: Es posible desplegar aplicaciones en múltiples sistemas sin necesidad de configurarlas de forma individual en cada dispositivo.

- Gestión centralizada: Facilita la actualización, parcheo y administración de aplicaciones desde un servidor centralizado.

- Seguridad: Como las aplicaciones están aisladas del sistema operativo y otras aplicaciones, es más difícil que una aplicación comprometida afecte al sistema completo.

### Backend

En este momento quiero mostrarle mi conexion a base de datos.









## Usage/Examples

```javascript
package proyectorestaurante.conexion;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class Conexion {
    private Connection cn;

    public Connection abrirConexion() {
        try {
           Class.forName("com.mysql.cj.jdbc.Driver");
            String urldb = "jdbc:mysql://localhost:3306/mydb?serverTimezone=UTC";
            String usr = "root";
            String psw = "123";
            cn = (Connection) DriverManager.getConnection(urldb, usr, psw);
            
            System.out.println("La conexiòn fue exitosa.");
        } catch (ClassNotFoundException e) {
            System.out.println("Error >> Driver no Instalado!!");
        } catch (SQLException e) {
            System.out.println("Error >> de conexión con la BD");
        }
        return cn;
    }

    public void cerrarConexion() {
        try {
            if (cn != null) {
                cn.close();
                System.out.println("Se cerrò la conexiòn.");
            }
        } catch (SQLException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}


## Integrantes:

-Jose David Roa Peñaloza

-Juan Diego Parra Vasquez

Grupo:B191







