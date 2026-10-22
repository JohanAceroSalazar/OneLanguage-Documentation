# Manejo de errores

`GlobalExceptionHandler` centraliza errores de API y existe `LoginFailureException`. Los clientes deben mostrar mensajes comprensibles y no exponer trazas, tokens ni datos de otros usuarios. Los códigos y cuerpos reales deben capturarse como evidencia en pruebas de contrato, pues no se ejecutó la aplicación durante esta auditoría.
