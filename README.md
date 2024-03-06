# Actividad-Nro.3---Formulario-con-Datos-


document.addEventListener("DOMContentLoaded", () => {
  const form = document.getElementById("contacto-servicio");

  // Generar el cuento
  form.addEventListener("submit", (event) => {
    event.preventDefault();

    const nombres = document.getElementById("nombres").value;
    const apellidos = document.getElementById("apellidos").value;
    const email = document.getElementById("email").value;
    const telefono = document.getElementById("telefono").value;
    const servicio = document.getElementById("servicio").value;

    const formulario = document.getElementById("formulario");

    const tabla = ` <table>
    <tbody>
      <tr>
        <th scope="row">Nombres</th>
        <td>${nombres}</td>
      </tr>
      <tr>
        <th scope="row">Apellidos</th>
        <td>${apellidos}</td>
      </tr>
      <tr>
        <th scope="row">Email</th>
        <td>${email}</td>
      </tr>
      <tr>
        <th scope="row">Teléfono</th>
        <td>${telefono}</td>
      </tr>
      <tr>
        <th scope="row">Servicio</th>
        <td>${servicio}</td>
      </tr>
    </tbody>
  </table>`;

    formulario.innerHTML = tabla;

    const inputsToClear = Array.from(document.querySelectorAll("#form input"));
    inputsToClear.forEach((input) => (input.value = ""));
  });
});
