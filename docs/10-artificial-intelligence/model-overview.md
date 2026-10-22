# Modelo y servicio

`web_service.py` implementa FastAPI y WebSocket; carga un modelo Keras `model/lsc_sequence_model.keras` y etiquetas `model/lsc_labels.json`. `recognizer.py` permite reconocimiento local. Se usan secuencias de landmarks y estados como manos no visibles, inactivo, baja confianza o predicción estable. La lista exacta de clases requiere acceso autorizado al artefacto `lsc_labels.json`.
