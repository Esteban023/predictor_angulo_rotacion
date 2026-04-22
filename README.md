
    <h1>🧠 MiniProyecto 3: Predicción de Ángulo de Rotación en MNIST</h1>

    <p>
        Este proyecto implementa un modelo de Machine Learning capaz de predecir el ángulo de rotación 
        entre dos imágenes del dataset MNIST, utilizando transformaciones en el espacio latente 
        estructurado en bloques 2D y entrenamiento conjunto con múltiples funciones de pérdida.
    </p>

    <h2>📌 Descripción del Problema</h2>

    <p>Dadas dos imágenes:</p>
    <ul>
        <li><strong>x₀:</strong> imagen original</li>
        <li><strong>xₜ:</strong> imagen rotada</li>
    </ul>

    <p><strong>Objetivo:</strong></p>
    <p>🔍 Predecir el ángulo de rotación θ aplicado a x₀ para obtener xₜ</p>

    <h2>⚙️ Enfoque Metodológico</h2>

    <p>El modelo se basa en tres ideas clave:</p>

    <h3>1. 🔄 Representación en Espacio Latente</h3>
    <ul>
        <li>Las imágenes se codifican en un espacio latente estructurado</li>
        <li>Este espacio se organiza en bloques 2D, lo que permite aplicar transformaciones geométricas explícitas</li>
    </ul>

    <h3>2. 🧩 Rotación en el Espacio Latente</h3>
    <ul>
        <li>En lugar de rotar directamente la imagen, se rota su representación latente</li>
        <li>Se aplica una rotación paramétrica (θ) sobre cada bloque 2D</li>
    </ul>

    <h3>3. 🎯 Entrenamiento Multi-Objetivo</h3>
    <p>El modelo se entrena con una combinación de pérdidas:</p>
    <ul>
        <li>📉 Pérdida de reconstrucción: asegura que la imagen generada sea coherente</li>
        <li>📐 Pérdida de ángulo: penaliza errores en la predicción de θ</li>
        <li>🔁 (Opcional) Regularizaciones adicionales del espacio latente</li>
    </ul>

    <h2>🏗️ Arquitectura General</h2>

    <pre>
Imagen x₀ ──► Encoder ──► Espacio Latente ──► Rotación(θ) ──► Decoder ──► x̂ₜ
                                   │
                                   └────► Predicción de θ
    </pre>

    <h2>📊 Dataset</h2>

    <ul>
        <li>📦 MNIST</li>
        <li>Imágenes de dígitos (28x28 en escala de grises)</li>
        <li>Transformaciones aplicadas:
            <ul>
                <li>Rotaciones con ángulos conocidos (ground truth)</li>
            </ul>
        </li>
    </ul>

</body>
</html>
