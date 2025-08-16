# Challenge-Amigo-Secreto
Este proyecto es una pequeña aplicación en **JavaScript**, **HTML** y **CSS** que permite:

- Agregar nombres a una lista de amigos.
- Mostrar la lista de forma dinámica en pantalla.
- Sortear un amigo de manera aleatoria.
- Reiniciar el juego inmediatamente después de mostrar el ganador.

---

## 📖 Descripción detallada

El proyecto se basa en un archivo JavaScript que implementa la lógica para administrar un sorteo simple.  

### 1️⃣ Array principal
```javascript
let amigos = [];
```
Se declara un array vacío para almacenar los nombres que el usuario vaya ingresando.

---

### 2️⃣ Función `agregarAmigo()`
- Obtiene el valor del campo de entrada (`input`) con id `"amigo"`.
- Elimina espacios innecesarios con `.trim()`.
- Si el campo está vacío, muestra un mensaje de alerta y detiene la ejecución.
- Si el nombre es válido, lo agrega al array `amigos` y actualiza la lista en pantalla llamando a `mostrarLista()`.
- Limpia el campo de entrada para permitir nuevas inserciones.

---

### 3️⃣ Función `mostrarLista()`
- Selecciona el elemento `<ul>` con id `"listaAmigos"`.
- Limpia el contenido actual para evitar duplicados.
- Recorre el array `amigos` y por cada nombre:
  - Crea un elemento `<li>`.
  - Inserta el nombre en ese elemento.
  - Lo agrega a la lista en el DOM.

---

### 4️⃣ Función `sortearAmigo()`
- Verifica que el array `amigos` no esté vacío.
- Genera un índice aleatorio usando:
  ```javascript
  Math.floor(Math.random() * amigos.length);
  ```
- Obtiene el nombre correspondiente y lo muestra en el elemento con id `"resultado"`.
- Llama a la función `reiniciarJuego()` para reiniciar inmediatamente después del sorteo.

---

### 5️⃣ Función `reiniciarJuego()` *(por implementar)*
Aunque en el código original no está definida, se recomienda que:
- Vacíe el array `amigos`.
- Limpie la lista mostrada (`#listaAmigos`).
- Limpie el resultado (`#resultado`).

Ejemplo:
```javascript
function reiniciarJuego() {
    amigos = [];
    document.getElementById("listaAmigos").innerHTML = "";
    document.getElementById("resultado").innerHTML = "";
}
```

---

## 📂 Estructura del proyecto
```
📁 proyecto-sorteo
│── index.html     # Interfaz HTML
│── style.css      # Estilos (opcional)
│── app.js         # Lógica en JavaScript
│── README.md      # Documentación del proyecto
```

---

## 🚀 Uso
1. Abre `index.html` en tu navegador.
2. Escribe el nombre de un amigo y pulsa **Agregar amigo**.
3. Agrega todos los nombres que desees.
4. Pulsa **Sortear amigo** para obtener un ganador.
5. El ganador se mostrará y el juego se reiniciará automáticamente.

---

## 🛠 Tecnologías utilizadas
- **HTML5**
- **CSS3**
- **JavaScript (ES6)**

---

## ✨ Autor
Creado por **Marilys** como práctica de JavaScript en el curso de **Alura Latam**.
