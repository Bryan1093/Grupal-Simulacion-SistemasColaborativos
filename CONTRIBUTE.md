# Guia de contribucion

Este documento define las reglas minimas para contribuir al repositorio de **Simulación - Sistemas Colaborativos**. El objetivo es mantener un historial claro, revisable y consistente entre todos los integrantes del equipo.

## Flujo general

1. Actualizar la rama local antes de comenzar a trabajar.
2. Crear una rama para cada cambio o grupo de cambios relacionados.
3. Realizar commits pequenos, descriptivos y con un formato uniforme.
4. Abrir un Pull Request con una descripcion clara del cambio realizado.
5. Esperar revision antes de fusionar cambios importantes.

## Formato de commits

Todos los commits deben seguir este formato:

```text
tipo(alcance): descripcion breve
```

Ejemplo:

```text
docs(documentacion): actualizar informe de desarrollo
```

La descripcion debe escribirse en infinitivo o presente, en minusculas y sin punto final.

### Tipos permitidos

- `docs`: cambios en documentacion, informes, LaTeX, README o archivos academicos.
- `feat`: nueva funcionalidad del proyecto o del modelo de simulacion.
- `fix`: correccion de errores.
- `refactor`: reorganizacion interna sin cambiar comportamiento.
- `style`: cambios visuales, formato o presentacion sin alterar logica.
- `assets`: incorporacion, reemplazo o eliminacion de imagenes, recursos, datos u otros elementos.
- `chore`: tareas de mantenimiento, configuracion o limpieza general.
- `test`: pruebas, simulaciones de prueba o archivos relacionados con QA.

### Alcances recomendados

Usar el alcance para indicar la zona afectada:

- `simulacion`
- `documentacion`
- `readme`
- `assets`
- `repo`

Ejemplos validos:

```text
docs(documentacion): corregir seccion de riesgos
docs(readme): actualizar integrantes del grupo
assets(documentacion): reemplazar imagen de portada
feat(simulacion): agregar agentes al modelo
fix(simulacion): corregir parametros de simulacion
chore(repo): actualizar configuracion de gitignore
```

## Reglas para escribir commits

- Evitar mensajes genericos como `Cambios`, `Actualizacion`, `Subida de archivo` o `Arreglos varios`.
- Cada commit debe representar una intencion clara.
- No mezclar cambios de codigo, documentacion y assets en un mismo commit si no dependen entre si.
- Si un cambio modifica el informe en LaTeX y ademas reemplaza una imagen usada por el mismo, se recomienda separar en dos commits:
  - `assets(documentacion): reemplazar imagen del informe`
  - `docs(documentacion): actualizar contenido del informe`
- No incluir archivos temporales, builds generados o archivos personales.

## Pull Requests

Cada Pull Request debe incluir:

- Resumen breve de lo realizado.
- Archivos o secciones afectadas.
- Motivo del cambio.
- Capturas o evidencia si el cambio es visual.
- Confirmacion de que el proyecto o documento fue revisado cuando aplique.

Formato recomendado:

```markdown
## Resumen
- Describe los cambios principales.

## Archivos afectados
- Lista las carpetas o archivos mas importantes.

## Verificacion
- Indica como se reviso el cambio.
```

## Convenciones para ramas

Usar nombres breves y descriptivos:

```text
docs/informe-riesgos
docs/portada-latex
feat/agentes-movimiento
fix/parametros-simulacion
assets/imagenes-informe
```

## Antes de abrir un PR

- Revisar que el historial de commits sea claro.
- Confirmar que no existan archivos innecesarios en el commit.
- Verificar ortografia en los documentos y reportes.
- Comprobar que las imagenes y referencias usadas existan en el repositorio.
- Mantener la rama actualizada con `master`.