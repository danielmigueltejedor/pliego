# Pliego

Maquetación editorial de Nodalix.

El motor de este repositorio es el código de [storytold/designcraft](https://github.com/storytold/designcraft) en `d582277cc79c4bc9cee174b25b13fb11e6957aa5`.
La licencia de ese código se conserva, igual que `NOTICE` y `docs/upstream-readme.md`.
Pliego es el nombre del producto. El motor puede cambiar sin esperar a upstream.
Un sync posterior compara commits. No se sustituye este árbol con un reset.

## Compilar

```bash
cargo run -p designcraft
```

El binario de escritorio se llama `pliego`.

## Estado

La shell que entra en este import es la de upstream. La interfaz GTK 4 / libadwaita de Nodalix no está cableada todavía. El motor sí está en este repositorio, con sus tests.
