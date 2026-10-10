# userstyles

Estilos de usuario para las herramientas internas de Mikroways. Se aplican con
[Stylus](https://add0n.com/stylus.html), que existe para Firefox y para Chrome.

| Estilo | Para |
|---|---|
| `redmine-oscuro.user.css` | Modo oscuro de [proyectos.mikroways.net](https://proyectos.mikroways.net) |

## Instalar

Abrí en el browser la URL cruda del estilo y Stylus ofrece instalarlo:

```
https://raw.githubusercontent.com/juanpsm/userstyles/main/redmine-oscuro.user.css
```

Funciona igual en Firefox y en Chrome. Los dos quedan apuntando a esta misma
URL, así que un cambio acá llega a los dos.

## Editar

Cloná, editá, y **subí `@version`**. Stylus compara esa versión contra la que
tiene instalada y, si no subió, no se trae nada aunque el archivo haya cambiado.
El mensaje que muestra es `up-to-date: version is unchanged` y manda a buscar el
problema al lado equivocado, porque el archivo sí cambió.

```bash
git clone git@github.com:juanpsm/userstyles.git
# editar, subir @version
git commit -am "redmine oscuro: ..."
git push
```

Después, en cada browser: ícono de Stylus, *Administrar*, y *Buscar
actualizaciones* en el estilo. También se actualiza solo según el intervalo que
tengas configurado en las opciones de Stylus.

## Probar un cambio sin publicarlo

En la página que querés ver, DevTools y pegar el cuerpo del `@-moz-document` en
una etiqueta `<style>`. Alcanza para iterar sobre el color de algo. Ojo con leer
una propiedad calculada en la misma llamada en que inyectás el estilo: devuelve
el valor viejo.
