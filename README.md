# cuestionario_oftalmologico

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Formulario de Consulta Oftalmológica</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 800px;
      margin: 30px auto;
      padding: 20px;
      background-color: #f9f9f9;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    label {
      font-weight: bold;
    }
    input[type="text"],
    textarea {
      width: 100%;
      padding: 10px;
      font-size: 14px;
      border: 1px solid #ccc;
      border-radius: 5px;
      resize: vertical;
    }
    input:invalid, textarea:invalid {
      border-color: red;
      background-color: #ffecec;
    }
    fieldset {
      padding: 15px;
      border: 1px solid #ddd;
      border-radius: 5px;
      background-color: #f3f3f3;
    }
    legend {
      font-weight: bold;
      font-size: 1.1em;
      margin-bottom: 10px;
    }
    fieldset div {
      margin-bottom: 10px;
    }
    .exploracion {
      padding: 10px;
      border: 1px solid #ddd;
      border-radius: 5px;
      background-color: #f3f3f3;
    }
    button {
      padding: 12px;
      font-size: 16px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 10px;
    }
    button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>

  <h1>Formulario de Consulta Oftalmológica</h1>

  <p>
    Usted va a ser atendido en el servicio de oftalmología tan pronto como sea posible.<br>
    Con ánimo de prestar el mejor servicio posible, le rogamos que antes de pasar a consulta, por favor, conteste las preguntas con <strong>LA MÁXIMA SINCERIDAD</strong>
  </p>

<form 
action="https://formspree.io/f/xqawqvvd" 
method="POST"
>

    <!-- Datos básicos -->
    
    <div>
      <label for="motivo">Motivo de consulta:</label>
      <textarea id="motivo" name="motivo" required></textarea>
    </div>

    <div>
      <label for="anamnesis">Anamnesis:</label>
      <textarea id="anamnesis" name="anamnesis" required></textarea>
    </div>
    
    <!-- Pregunta sobre alergias a medicación -->
    <div>
      <label>¿Tiene alergias a medicación?</label><br>
      <input type="radio" name="alergias_medicacion" value="Sí" required> Sí
      <input type="radio" name="alergias_medicacion" value="No" required> No
    </div>
    <div id="alergiaDetalleContainer" style="display: none;">
      <label for="alergia_detalle">Especifique el tipo de alergia a medicación:</label><br>
      <input type="text" id="alergia_detalle" name="alergia_detalle">
    </div>

    <!-- Sección: Síntomas oculares actuales -->
    <fieldset>
      <legend>Síntomas oculares actuales</legend>
      <div>
        <label>¿Ha notado pérdida de visión intensa?</label><br>
        <input type="radio" name="perdida_vision" value="Sí" required> Sí
        <input type="radio" name="perdida_vision" value="No" required> No
      </div>
      <div>
        <label>¿Percibe manchas flotantes o puntos negros?</label><br>
        <input type="radio" name="moscas" value="Sí" required> Sí
        <input type="radio" name="moscas" value="No" required> No
      </div>
      <div>
        <label>¿Percibe destellos?</label><br>
        <input type="radio" name="destellos" value="Sí" required> Sí
        <input type="radio" name="destellos" value="No" required> No
      </div>
      <div>
        <label>¿Tiene visión doble?</label><br>
        <input type="radio" name="vision_doble" value="Sí" required> Sí
        <input type="radio" name="vision_doble" value="No" required> No
      </div>
      <div>
        <label>¿Desaparece la visión doble al cerrar un ojo?</label><br>
        <input type="radio" name="vision_doble_cierra_ojo" value="Sí" required> Sí
        <input type="radio" name="vision_doble_cierra_ojo" value="No" required> No
      </div>
      <div>
        <label>¿Siente dolor en los ojos?</label><br>
        <input type="radio" name="dolor" value="Sí" required> Sí
        <input type="radio" name="dolor" value="No" required> No
      </div>
      <div>
        <label>¿Le ha caído algo en los ojos?</label><br>
        <input type="radio" name="caida_objeto" value="Sí" required> Sí
        <input type="radio" name="caida_objeto" value="No" required> No
      </div>
      <div>
        <label for="que_cayo">¿El qué? (solo si respondió sí):</label><br>
        <input type="text" id="que_cayo" name="que_cayo">
      </div>
      <div>
        <label>¿Siente picor, ardor o resequedad?</label><br>
        <input type="radio" name="resequedad" value="Sí" required> Sí
        <input type="radio" name="resequedad" value="No" required> No
      </div>
      <div>
        <label>¿Ha notado enrojecimiento ocular?</label><br>
        <input type="radio" name="enrojecimiento" value="Sí" required> Sí
        <input type="radio" name="enrojecimiento" value="No" required> No
      </div>
    </fieldset>

    <!-- Sección: Antecedentes oftalmológicos -->
    <fieldset>
      <legend>Antecedentes oftalmológicos</legend>
      <div>
        <label>¿Ha tenido alguna enfermedad ocular previa?</label><br>
        <input type="radio" name="enfermedad_ocular" value="Sí" required> Sí
        <input type="radio" name="enfermedad_ocular" value="No" required> No
      </div>
      <div>
        <label for="enfermedad_ocular_detalle">¿Cuál?</label><br>
        <input type="text" id="enfermedad_ocular_detalle" name="enfermedad_ocular_detalle">
      </div>
      <div>
        <label>¿Ha tenido alguna cirugía ocular previa?</label><br>
        <input type="radio" name="cirugia_ocular" value="Sí" required> Sí
        <input type="radio" name="cirugia_ocular" value="No" required> No
      </div>
      <div>
        <label for="cirugia_ocular_detalle">¿Cuál?</label><br>
        <input type="text" id="cirugia_ocular_detalle" name="cirugia_ocular_detalle">
      </div>
      <div>
        <label>¿Antecedentes familiares de enfermedades oculares (glaucoma, degeneración macular, etc)?</label><br>
        <input type="radio" name="familiar_enfermedad_ocular" value="Sí" required> Sí
        <input type="radio" name="familiar_enfermedad_ocular" value="No" required> No
      </div>
      <div>
        <label for="familiar_enfermedad_ocular_detalle">¿Quién?</label><br>
        <input type="text" id="familiar_enfermedad_ocular_detalle" name="familiar_enfermedad_ocular_detalle">
      </div>
    </fieldset>

    <!-- Sección: Antecedentes médicos -->
    <fieldset>
      <legend>Antecedentes médicos</legend>
      <div>
        <label>¿Tiene alguna enfermedad crónica (diabetes, hipertensión, colesterol, artritis)?</label><br>
        <input type="radio" name="enfermedad_cronica" value="Sí" required> Sí
        <input type="radio" name="enfermedad_cronica" value="No" required> No
      </div>
      <div>
        <label for="enfermedad_cronica_detalle">¿Cuál o cuáles?</label><br>
        <input type="text" id="enfermedad_cronica_detalle" name="enfermedad_cronica_detalle">
      </div>
      <div>
        <label>¿Es fumador o lo ha sido?</label><br>
        <input type="radio" name="fumador" value="Sí" required> Sí
        <input type="radio" name="fumador" value="No" required> No
      </div>
      <div>
        <label>¿Está tomando algún medicamento actualmente?</label><br>
        <input type="radio" name="medicacion_actual_si" value="Sí" required> Sí
        <input type="radio" name="medicacion_actual_si" value="No" required> No
      </div>
      <div>
        <label for="medicacion_actual_detalle">¿Cuáles?</label><br>
        <input type="text" id="medicacion_actual_detalle" name="medicacion_actual_detalle">
      </div>
      <div>
        <label>¿Antecedentes familiares de enfermedades oculares (glaucoma, cataratas, etc)?</label><br>
        <input type="radio" name="familiares_oculares_med" value="Sí" required> Sí
        <input type="radio" name="familiares_oculares_med" value="No" required> No
      </div>
    </fieldset>

    <!-- Sección: Exploración física (opcional) -->
    <div class="exploracion">
      <label>Exploración física (opcional):</label>
      <label for="avsc">AVsc:</label>
      <input type="text" id="avsc" name="avsc">
      <label for="pior">PIOr:</label>
      <input type="text" id="pior" name="pior">
      <label for="bmc">BMC:</label>
      <input type="text" id="bmc" name="bmc">
    </div>

    <button type="submit">Enviar Documento</button>
  </form>

  <script>
    // Mostrar u ocultar el cuadro de texto para especificar alergias a medicación
    document.addEventListener("DOMContentLoaded", function() {
      const radios = document.getElementsByName("alergias_medicacion");
      const detalleContainer = document.getElementById("alergiaDetalleContainer");
      
      radios.forEach(radio => {
        radio.addEventListener("change", function() {
          if (this.value === "Sí") {
            detalleContainer.style.display = "block";
          } else {
            detalleContainer.style.display = "none";
          }
        });
      });
    });
  </script>

</body>
</html>
