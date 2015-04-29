# Htmlwidgets Gallery with Isotope
jpmarindiaz  
April 29, 2015  


If you provide filterCols you can select which columns to use as filters.
If you provide sortCols you can select which columns to use to sort the items.
You can also provide custom html templates to render the items.


```r
# devtools::install_github("jpmarindiaz/isotope")
library(isotope)
d <- read.csv(system.file("data/candidatos.csv",package="isotope"), stringsAsFactors = FALSE)

filterCols <- c("genero","profesiones", "niveldeestudios","talante", "pragmaticoideologico","visionpais")
sortCols <- c("nombre","apoyosenadores","apoyorepresentantes")

tpl <- '
<div style="border: 1px solid grey; margin:5px; padding:5px">
  <div class="container">
    <h3 class="nombre">{{nombre}}</h3>
    <div style="width:125px; height: 125px; margin:auto">
      <img src={{foto}} class="circle" width="100px"/>
    </div>
    <p>Profesión: {{profesiones}}, Género: {{genero}},Nivel de estudios: {{niveldeestudios}}</p>
    <div class="apoyosenadores"><em>Apoyo Senadores:</em> {{apoyosenadores}}</div>
    <div class="apoyorepresentantes"><em>Apoyo Representantes:</em> {{apoyorepresentantes}}</div>
  </div>
</div>
'
isotope(d, filterCols = filterCols, sortCols = sortCols, lang = 'es', elemTpl = tpl, ncols=3)
```

<!--html_preserve--><div id="htmlwidget-711" style="width:672px;height:480px;" class="isotope"></div>
<script type="application/json" data-for="htmlwidget-711">{"x":{"filterBtns":"<h3>Filtrar por</h3><div id=\"select-car\"></div>","sortBtns":"<div id=\"sorts\" class=\"button-group\">\n  <h3>Ordenar por</h3>\n  <button class=\"button mb1\" data-sort-by=\"original-order\">Original Order</button>\n  <button class=\"button mb1\" data-sort-by=\"nombre\">nombre</button>\n  <button class=\"button mb1\" data-sort-by=\"apoyosenadores\">apoyosenadores</button>\n  <button class=\"button mb1\" data-sort-by=\"apoyorepresentantes\">apoyorepresentantes</button>\n</div>","sortData":{"nombre":".nombre","apoyosenadores":".apoyosenadores","apoyorepresentantes":".apoyorepresentantes"},"items":"<div class=\"element-item genero F profesiones Derecho niveldeestudios Especialización talante Conservador maspoliticoquetecnico No masmicroquemacrogerente Sí cambiamejoramodelo mejorar pragmaticoideologico Sí visionpais Construir visión apoyosenadores 5 apoyorepresentantes 28 foto http://lasillavacia.com/sites/default/files/fotosperfil/MartaLuciaRamirez.jpg nombre Ramírez Blanco Marta Lucía\" style=\"width:33%\" >\n<div style=\"border: 1px solid grey; margin:5px; padding:5px\">\n  <div class=\"container\">\n    <h3 class=\"nombre\">Ramírez Blanco Marta Lucía</h3>\n    <div style=\"width:125px; height: 125px; margin:auto\">\n      <img src=http://lasillavacia.com/sites/default/files/fotosperfil/MartaLuciaRamirez.jpg class=\"circle\" width=\"100px\"/>\n    </div>\n    <p>Profesión: Derecho,, Género: F,Nivel de estudios: Especialización</p>\n    <div class=\"apoyosenadores\"><em>Apoyo Senadores:</em>  5</div>\n    <div class=\"apoyorepresentantes\"><em>Apoyo Representantes:</em> 28</div>\n  </div>\n</div>\n\n</div>\n<div class=\"element-item genero F profesiones Economía niveldeestudios Maestría talante Liberal maspoliticoquetecnico Sí masmicroquemacrogerente No cambiamejoramodelo cambiar pragmaticoideologico No visionpais Visión propia apoyosenadores 5 apoyorepresentantes 3 foto http://lasillavacia.com/sites/default/files/fotosperfil/ClaraLopezQQ.jpg nombre López Obregón Clara Eugenia\" style=\"width:33%\" >\n<div style=\"border: 1px solid grey; margin:5px; padding:5px\">\n  <div class=\"container\">\n    <h3 class=\"nombre\">López Obregón Clara Eugenia</h3>\n    <div style=\"width:125px; height: 125px; margin:auto\">\n      <img src=http://lasillavacia.com/sites/default/files/fotosperfil/ClaraLopezQQ.jpg class=\"circle\" width=\"100px\"/>\n    </div>\n    <p>Profesión: Economía,, Género: F,Nivel de estudios: Maestría</p>\n    <div class=\"apoyosenadores\"><em>Apoyo Senadores:</em>  5</div>\n    <div class=\"apoyorepresentantes\"><em>Apoyo Representantes:</em>  3</div>\n  </div>\n</div>\n\n</div>\n<div class=\"element-item genero M profesiones Economía niveldeestudios Maestría talante Liberal maspoliticoquetecnico Sí masmicroquemacrogerente No cambiamejoramodelo mejorar pragmaticoideologico Sí visionpais Construir visión apoyosenadores 55 apoyorepresentantes 91 foto http://lasillavacia.com/sites/default/files/fotosperfil/Juan%20Manuel%20Santos.jpg nombre Santos Calderón Juan Manuel\" style=\"width:33%\" >\n<div style=\"border: 1px solid grey; margin:5px; padding:5px\">\n  <div class=\"container\">\n    <h3 class=\"nombre\">Santos Calderón Juan Manuel</h3>\n    <div style=\"width:125px; height: 125px; margin:auto\">\n      <img src=http://lasillavacia.com/sites/default/files/fotosperfil/Juan%20Manuel%20Santos.jpg class=\"circle\" width=\"100px\"/>\n    </div>\n    <p>Profesión: Economía,, Género: M,Nivel de estudios: Maestría</p>\n    <div class=\"apoyosenadores\"><em>Apoyo Senadores:</em> 55</div>\n    <div class=\"apoyorepresentantes\"><em>Apoyo Representantes:</em> 91</div>\n  </div>\n</div>\n\n</div>\n<div class=\"element-item genero M profesiones Economía niveldeestudios Maestría talante Conservador maspoliticoquetecnico Sí masmicroquemacrogerente No cambiamejoramodelo mejorar pragmaticoideologico Sí visionpais Construir visión apoyosenadores 20 apoyorepresentantes 18 foto http://lasillavacia.com/sites/default/files/fotosperfil/oscar-ivan-zuluaga.jpg nombre Zuluaga Escobar Óscar Iván\" style=\"width:33%\" >\n<div style=\"border: 1px solid grey; margin:5px; padding:5px\">\n  <div class=\"container\">\n    <h3 class=\"nombre\">Zuluaga Escobar Óscar Iván</h3>\n    <div style=\"width:125px; height: 125px; margin:auto\">\n      <img src=http://lasillavacia.com/sites/default/files/fotosperfil/oscar-ivan-zuluaga.jpg class=\"circle\" width=\"100px\"/>\n    </div>\n    <p>Profesión: Economía,, Género: M,Nivel de estudios: Maestría</p>\n    <div class=\"apoyosenadores\"><em>Apoyo Senadores:</em> 20</div>\n    <div class=\"apoyorepresentantes\"><em>Apoyo Representantes:</em> 18</div>\n  </div>\n</div>\n\n</div>\n<div class=\"element-item genero M profesiones Economía niveldeestudios Doctorado talante Liberal maspoliticoquetecnico No masmicroquemacrogerente Sí cambiamejoramodelo cambiar pragmaticoideologico No visionpais Visión propia apoyosenadores 4 apoyorepresentantes 5 foto http://lasillavacia.com/sites/default/files/fotosperfil/EnriquePenalosaQQ.jpg nombre Peñalosa Londoño Enrique\" style=\"width:33%\" >\n<div style=\"border: 1px solid grey; margin:5px; padding:5px\">\n  <div class=\"container\">\n    <h3 class=\"nombre\">Peñalosa Londoño Enrique</h3>\n    <div style=\"width:125px; height: 125px; margin:auto\">\n      <img src=http://lasillavacia.com/sites/default/files/fotosperfil/EnriquePenalosaQQ.jpg class=\"circle\" width=\"100px\"/>\n    </div>\n    <p>Profesión: Economía,, Género: M,Nivel de estudios: Doctorado</p>\n    <div class=\"apoyosenadores\"><em>Apoyo Senadores:</em>  4</div>\n    <div class=\"apoyorepresentantes\"><em>Apoyo Representantes:</em>  5</div>\n  </div>\n</div>\n\n</div>","selectizeOptions":{"filterValueId":["F","M","Doctorado","Especialización","Maestría","No","Sí","Derecho","Economía","Conservador","Liberal","Construir visión","Visión propia"],"groupId":["genero","genero","niveldeestudios","niveldeestudios","niveldeestudios","pragmaticoideologico","pragmaticoideologico","profesiones","profesiones","talante","talante","visionpais","visionpais"],"filterValueLabel":["F","M","Doctorado","Especialización","Maestría","No","Sí","Derecho","Economía","Conservador","Liberal","Construir visión","Visión propia"]},"selectizeOptgroups":{"groupId":["genero","niveldeestudios","pragmaticoideologico","profesiones","talante","visionpais"],"groupLabel":["genero","niveldeestudios","pragmaticoideologico","profesiones","talante","visionpais"]},"layoutMode":"masonry"},"evals":[]}</script><!--/html_preserve-->
