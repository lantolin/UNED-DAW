# Que hay aqui?

Son sitios web estáticos, tomados de código publico de GitHub que usaremos como sitios de prácticas. Simulan el contenido que le llega a un desplegador desde alguna entidad externa (desarrollador, empresa, departamento, etc.)

# Como reconstruirlo?

Si por cualquier razon hubiera que actualizar/reconstruir estos sitios, estas son las instrucciones (mas o menos)

```
git clone git@github.com:whatwg/html.git
git clone git@github.com:whatwg/html-build.git
git clone git@github.com:whatwg/url.git
git clone git@github.com:whatwg/dom.git
cd html-build/
./build.sh --remote
cd url/
make
mv url.html index.html
cd ..
cd dom
make
mv dom.html index.html
cd ..
```

Los sitios estáticos quedan en ./dom ./url y .html-build/output, listos para ponerlos u organizarlos como uno quiera.
