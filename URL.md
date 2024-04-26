#URLS

###Todos los posts
```
GET http://localhost:1337/api/posts
```


###Un posts 
```
GET http://localhost:1337/api/posts/1
```

###Populate
La API REST de forma predeterminada no rellena ninguna relación, campo multimedia, componente o zona dinámica. Utilice el parámetro populate para completar campos específicos.

```
GET http://localhost:1337/api/posts?populate=*
```


###filters

filters[slug]=slug-del-post
```
GET http://localhost:1337/api/posts?filters[slug]=slug-del-post
```

###Sort
sort[createdAt]=asc
```
GET http://localhost:1337/api/posts?sort[createdAt]=asc
```

###Paginación
```
GET http://localhost:1337/api/posts?pagination[page]=1&pagination[pageSize]=4&sort[createdAt]=desc
```

```
"meta": {
    "pagination": {
      "page": 2, // página actual
      "pageSize": 4, // número de elementos por página
      "pageCount": 3, // total de páginas
      "total": 11 // total de elementos
    }
  }
```
