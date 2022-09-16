
# CRUD EN MongoDB
# Ing de Software. Bases de datos avanzadas. Iberoamericana

### Brayan Steven Bonilla Castellanos :man: 
### Juan Carlos Monsalve Gómez :man:

Compartimos a continuación los ejemplos de código que nos permiten interactuar a través del Shell de MongoDB con una base de datos no relacional con un Crud.

## Create (Crear) 📝


**Crear: CREATE (uno solo)**


~~~
db.deportistas.insertOne({"documento": 653297, "nombres": "Ricardo Andrés", "apellidos": "Yepes Ortega", "fecha_nacimiento": "2005-10-16","eps": "Sura","poliza": "Sura", "consentimiento": "Pedro Rodriguez", "equipo" : "Colonia F.C" })
~~~

**Crear: CREATE (varios al tiempo)**

~~~
db.deportistas.insertMany([
  {"documento": 215486, "nombres": "Juan Andres", "apellidos": "Garcia Gutierrez", "fecha_nacimiento": "2006-11-25","eps": "Compensar","poliza": "Sura", "consentimiento": "Alfonzo Garcia", "equipo" : "Leones F.C" },
  {"documento": 245618,"nombres": "Carlos Andres", "apellidos": "Peñuela Barbosa","fecha_nacimiento": "2005-05-12", "eps": "Compensar", "poliza": "Sura", "consentimiento": "Alfonzo Garcia","equipo" : "Colonia F.C"},
  {"documento": 154852,"nombres": "Jessica Beltran","apellidos": "Ramirez Diaz","fecha_nacimiento": "2006-09-02", "eps": "Colsanitas","poliza": "Sura", "consentimiento": "Alfonzo Garcia", "equipo" : "Toros F.C"},
  {"documento": 365219,"nombres": "Laura Michell", "apellidos": "Gutierrez Murillo", "fecha_nacimiento": "2006-12-07", "eps": "Colsanitas", "poliza": "Sura", "consentimiento": "Alfonzo Garcia","equipo" : "TigresC"}
])
~~~


## Read (Leer) 👁️


**Para ver documentos en la coleccion X**

~~~
db.deportistas.find()
~~~

**Para ver documentos de una mejor manera**
~~~
db.deportistas.find().pretty()
~~~

## Update (Actualizar) 📝


**Para actualizar un documento (Update)**
Estructura general del comando que permite actualizar:
~~~
db.deportistas.update({}, {})
~~~

**Actualizando un documento por id**
~~~
db.deportistas.update({_id: ObjectId("631ce244e132c4303a5e7808")}, {$set: {nombres: "Maria Cecilia"} })
~~~

**Actualizando un documento por documento**
~~~
db.deportistas.update({"documento": 365219}, {$set: {nombres: "Gloria Patricia"} })
~~~

## Delete (Eliminar) 💣

**Para eliminar un documento (Delete)**

~~~
db.deportistas.deleteOne({"documento": 365219})
~~~



