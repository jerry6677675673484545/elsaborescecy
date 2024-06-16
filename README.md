<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>El Sabores - Taquería</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e8e8e8;
            margin: 0;
            padding: 20px;
        }
        header, footer, nav, section {
            margin-top: 20px;
            padding: 20px;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 0 10px;
        }
        nav {
            background-color: #3498db;
            padding: 10px;
            color: #ffffff;
        }
        .form-group {
            margin: 10px 0;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input, select, textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }
        .menu-table {
            width: 100%;
            text-align: center;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        .menu-table th, .menu-table td {
            border: 1px solid #ddd;
            padding: 8px;
        }
        .menu-table th {
            background-color: #3498db;
            color: white;
        }
    </style>
</head>
<body>

    <!-- Mensaje de bienvenida -->
    <header>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7DPpEAGxzq3PcvaW94yRa6y1ViH6B8lMHVQ&s" alt="El Sabores" style="width: 200px;">
        <h1>Bienvenidos a El Sabores - La mejor taquería</h1>
        <p>Disfruta de nuestros deliciosos tacos y sabores auténticos.</p>
        <section id="informacion">
            <footer style="text-align: center; background-color: #3498db; color: white; padding: 20px;">
                <p>El Sabores es una auténtica taquería mexicana que ofrece una amplia variedad de tacos, bebidas refrescantes y un servicio excepcional. Nuestros tacos se preparan con ingredientes frescos y sabrosos que te transportarán directamente a las calles de México.</p>
            </div>
                <p>Proveer a nuestros clientes los mejores tacos con ingredientes de alta calidad, manteniendo el sabor tradicional y el compromiso con el servicio excelente.</p>
            </div>
                <p>Ser la taquería líder en el mercado local, reconocida por nuestra autenticidad y excelencia en la gastronomía mexicana.</p>
            </div>
        </section>
        
    </header>

    <!-- Barra de Navegación -->
    <nav>
        <a href="#registro-inicio">Registro e Inicio de Sesión</a>
        <a href="#menu">Menú</a>
        <a href="#pedidos">Realización de Pedido</a>
        <a href="#ubicacion">Ubicación</a>
        <a href="#informacion">Información</a>
    </nav>

    <!-- Registro e Inicio de Sesión -->
    <section style="margin-top: 20px; padding: 20px; background-color: #ffffff; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);">
        <h2>Registro e Inicio de Sesión</h2>
        <div style="display: flex; justify-content: space-around; text-align: left;">
            <!-- Formulario de registro -->
            <form action="/register" method="post" style="flex: 1; padding-right: 20px;">
                <h3>Registrarse</h3>
                <label para="email">Correo electrónico:</label>
                <input type="email" id="email" name="email" style="width: 100%;"><br>

                <label para="password">Contraseña:</label>
                <input type="password" id="password" name="password" style="width: 100%;"><br>

                <button type="submit" style="background-color: #3498db; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Registrarse</button>
            </form>

            <!-- Formulario de inicio de sesión -->
            <form action="/login" method="post" style="flex: 1;">
                <h3>Iniciar Sesión</h3>
                <label para="login-email">Correo electrónico:</label>
                <input para="login-email" type="email" id="login-email" name="email" style="width: 100%;"><br>

                <label para="login-password">Contraseña:</label>
                <input para="login-password" type="password" id="login-password" name="password" style="width: 100%;"><br>

                <button type="submit" style="background-color: #3498db; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Iniciar Sesión</button>
            </form>
        </div>

        <div style="margin-top: 20px; text-align: center;">
            <p>O regístrate o inicia sesión con redes sociales:</p>
            <button style="background-color: #3b5998; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Iniciar con Facebook</button>
            <button style="background-color: #db4437; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Iniciar con Google</button>
        </div>
    </section>

    <!-- Catálogo de Tacos -->
    <section id="menu">
        <h2>Menú de Tacos</h2>
        <table class="menu-table">
            <thead>
                <tr>
                    <th>Imagen</th>
                    <th>Tipo de Taco</th>
                    <th>Descripción</th>
                    <th>Precio</th>
                    <th>Agregar</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><img src="https://assets.unileversolutions.com/recipes-v2/236509.jpg" alt="Taco de Pastor" style="width: 50px;"></td>
                    <td>Taco de Pastor</td>
                    <td>Cerdo adobado con especias mexicanas.</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Pastor', 25)">Agregar</button></td>
                </tr>
                <!-- Repite el mismo formato para los demás tacos -->
                <tr>
                    <td><img src="https://cheforopeza.com.mx/wp-content/uploads/2020/11/tacos-de-bistec-a-la-cerveza.jpg" alt="Taco de Bistek" style="width: 50px;"></td>
                    <td>Taco de Bistek</td>
                    <td>Bistek sazonado y cocido a la parrilla.</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Bistek', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://cdn2.cocinadelirante.com/sites/default/files/images/2023/01/receta-de-tacos-de-suadero-con-costra-de-queso.jpg" alt="Taco de Suadero" style="width: 50px;"></td>
                    <td>Taco de Suadero</td>
                    <td>Carne de suadero cocida lentamente.</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Suadero', 25)">Agregar</button></td>
                </tr>
                <td><img src="https://cocina-casera.com/mx/wp-content/uploads/2017/12/tacos-de-arrachera.jpg" alt="Arrachera" style="width: 50px;"></td>
                    <td>Arrachera</td>
                    <td>Corte premium de carne</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Arrachera', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://cocinamia.com.mx/wp-content/uploads/2020/02/a-12-1-1100x500.png" alt="Alambre" style="width: 50px;"></td>
                    <td>Alambre</td>
                    <td>Mezcla de carnes y vegetales</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Alambre', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://cdn0.recetasgratis.net/es/posts/4/1/4/tacos_de_barbacoa_75414_orig.jpg" alt="Barbacoa" style="width: 50px;"></td>
                    <td>Barbacoa</td>
                    <td>Carne de cordero cocida al vapor</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Barbacoa', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://www.mccormick.com/-/media/project/oneweb/mccormick-us/el-guapo/recipes/800x800/tacos_de_lengua_800x800.jpg?rev=5c0b9eadb63b4d14afd086f325a20d4e&vd=20220203T165347Z&hash=4DB2F92B662CC3E0E5754CD0F425DF50" alt="Lengua" style="width: 50px;"></td>
                    <td>Lengua</td>
                    <td>Lengua de res guisada</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Lengua', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://pronacatqma.com/images/com_yoorecipe/banner_superior/8208_1.jpg" alt="Chicharrón" style="width: 50px;"></td>
                    <td>Chicharrón</td>
                    <td>Chicharrón crujiente</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Chicharrón', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://49efdeedfa.cbaul-cdnwnd.com/58bf4bb742aba32a44cec100e04e88ef/200000010-8fba98fbab/700/tacos%207.jpg?ph=49efdeedfa" alt="Longaniza" style="width: 50px;"></td>
                    <td>Longaniza</td>
                    <td>Embutido especiado</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Longaniza', 25)">Agregar</button></td>
                </tr>
                <tr>
                    <td><img src="https://www.paulinacocina.net/wp-content/uploads/2023/06/tacos-de-camaron-receta.jpg" alt="Camarones" style="width: 50px;"></td>
                    <td>Camarones</td>
                    <td>Camarones fritos y sazonados</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Taco de Camarones', 25)">Agregar</button></td>
                </tr>
            </tbody>
        </table>
    </section>

    <!-- Tabla de Bebidas -->
    <section id="bebidas">
        <h2>Bebidas</h2>
        <table class="menu-table">
            <thead>
                <tr>
                    <th>Producto</th>
                    <th>Descripción</th>
                    <th>Precio</th>
                    <th>Agregar</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Agua de Jamaica (1L)</td>
                    <td>Refrescante agua de jamaica natural.</td>
                    <td>$25</td>
                    <td><button onclick="addToOrder('Agua de Jamaica (1L)', 25)">Agregar</button></td>
                </tr>
            </tr>
            <tr>
                <td>Agua de Limón con Chía (1L)</td>
                <td>Refrescante agua de Limón con Chía.</td>
                <td>$25</td>
                <td><button onclick="addToOrder('Agua de Limón con Chía (1L)', 25)">Agregar</button></td>
            </tr>
            </tr>
                <td>Agua de Horchata (1L)</td>
                <td>Refrescante agua de Horchata.</td>
                <td>$25</td>
                <td><button onclick="addToOrder('Agua de Horchata (1L)', 25)">Agregar</button></td>
            </tr>
            <tr>
                <td>Refresco Mundet (755ml)</td>
                <td>Refresco de Manzana.</td>
                <td>$35</td>
                <td><button onclick="addToOrder('Refresco Mundet (755ml)', 35)">Agregar</button></td>
            </tr>
            <tr>
                <td>Coca Cola (755ml)</td>
                <td>Refresco de Cola.</td>
                <td>$35</td>
                <td><button onclick="addToOrder('Coca Cola (755ml)', 35)">Agregar</button></td>
            </tr>
            <tr>
                <td>Sprite (755ml)</td>
                <td>Refresco de Limón.</td>
                <td>$35</td>
                <td><button onclick="addToOrder('Pepsi (755ml)', 35)">Agregar</button></td>
            </tr>
            <tr>
                <td>Boing de Mango (755ml)</td>
                <td>Jugo de Mango.</td>
                <td>$35</td>
                <td><button onclick="addToOrder('Boing de Mango (755ml)', 35)">Agregar</button></td>
            </tr>
            <tr>
                <td>Boing de Guayaba (755ml)</td>
                <td>Jugo de Guayaba.</td>
                <td>$35</td>
                <td><button onclick="addToOrder('Boing de Guayaba (755ml)', 35)">Agregar</button></td>
            </tr>
        </table>
    </div>

    <div class="order-section">
        <h2>Pedido Final</h2>
        <div id="order-summary" class="order-summary">
            <p>No hay elementos en el pedido.</p>
        </div>
    </div>
            </tbody>
        </table>
    </section>

    <!-- Sistema de Pedidos en Línea -->
<section style="margin-top: 20px; padding: 20px; background-color: #ffffff; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); text-align: center;">
    <h2>Haz tu pedido en línea</h2>
    <form action="/order" method="post">
        <label para="nombre">Nombre de quien recibe:</label>
        <input type="text" id="nombre" name="nombre" style="width: 100%;"><br>

        <label para="telefono">Teléfono:</label>
        <input type="tel" id="telefono" name="telefono" style="width: 100%;"><br>

        <label para="delivery">Método de entrega:</label>
        <select id="delivery" name="delivery" style="width: 100%;">
            <option value="pickup">Recolección en tienda</option>
            <option value="delivery">Entrega a domicilio</option>
        </select><br>

        <label para="address">Dirección de entrega:</label>
        <input type="text" id="address" name="address" style="width: 100%;"><br>

        <label para="codigo-postal">Código postal:</label>
        <input type="text" id="codigo-postal" name="codigo-postal" style="width: 100%;"><br>

        <label para="comentarios">Comentarios:</label>
        <textarea id="comentarios" name="comentarios" style="width: 100%; height: 100px;"></textarea><br>

        <button type="submit" style="background-color: #3498db; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Realizar Pedido</button>
    </form>
</section>
<!-- Pago y Confirmación -->
<section style="margin-top: 20px; padding: 20px; background-color: #ffffff; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); text-align: center;">
    <h2>Pago y Confirmación</h2>
    <form action="/payment" method="post">
        <label for="card-number">Número de Tarjeta:</label>
        <input type="text" id="card-number" name="card-number" style="width: 100%;"><br>

        <label for="expiration">Fecha de Expiración:</label>
        <input type="text" id="expiration" name="expiration" style="width: 100%;"><br>

        <button type="submit" style="background-color: #3498db; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Pagar</button>
    </form>
</section>

    <!-- Mapa de Localización -->
    <section style="margin-top: 20px; padding: 20px; background-color: #ffffff; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); text-align: center;">
        <h2>Ubicación de El Sabores</h2>
        <p>Encuentra nuestra taquería:</p>
        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3766.0503248168473!2d-99.10952758421507!3d19.634420836576886!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85d1f6b8f7d36d97%3A0x34c68a287b28a221!2sParque%20Residencial%20Coacalco%2C%20Coacalco%20de%20Berriozabal%2C%20M%C3%A9x.!5e0!3m2!1ses!2smx!4v1642464685780!5m2!1ses!2smx"
            width="600"
            height="450"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
        ></iframe>
    </section>
    <!-- Comentarios y Calificaciones -->
<section style="margin-top: 20px; padding: 20px; background-color: #ffffff; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); text-align: center;">
    <h2>Comentarios y Calificaciones</h2>
    <form action="/feedback" method="post">
        <label for="comment">Comentario:</label>
        <textarea id="comment" name="comment" style="width: 100%; height: 100px;"></textarea><br>

        <label for="rating">Calificación (1-5):</label>
        <input type="number" id="rating" name="rating" min="1" max="5" style="width: 100%;"><br>

        <button type="submit" style="background-color: #3498db; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Enviar Comentario</button>
    </form>
</section>

    <!-- Información de la Taquería -->
    <footer style="text-align: center; background-color: #3498db; color: white; padding: 20px;">
        <h2>Información de El Sabores</h2>
        <p>Dirección: Av Parque, 015, Parque Residencial Coacalco, Estado de México</p>
        <p>Teléfono: +52 55 1234 5678</p>
        <p>Correo electrónico: contacto@elsabores.com</p>
    </footer>

</body>
</html>
