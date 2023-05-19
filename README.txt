Plugin desarrollado como complemento para la integración con la plataforma VIVO.

Actualmente permite el uso de las siguientes funciones:

1. report_get_courses_by_custom_field
2. report_get_user_by_custom_field
3. report_get_courses_by_teacher_id

Parámetros de las funciones 1 y 2:

customfield_name // Ej. orcid
customfield_value //ej 0000-0029-0008-1983

Parámetros de la función 3:

teacher_id //Ej. 3

Las funciones 2 y 3 son utilitarios de la función 1 ya que ambas se integran en ella.
la funcion (1) report_get_courses_by_custom_field es el propósito fundamental de este plugin ya que permite arrojar salidas en formato JSON o XML exponiendo los metadatos de los cursos impartidos por un individuo dado su identificador unico personalizado, Ej. orcid

Un ejemplo de uso sería la consulta:
https://moodle.example.com/webservice/rest/server.php?wsfunction=report_get_courses_by_custom_field&customfield_name=orcid&customfield_value=0000-0001-9161-3205&moodlewsrestformat=json&wstoken=1eccee0dfe72f9f190c038a00e8ca68f

Cuya salida sería:

{
"courses": [
	{
	"id": 3,
	"course_name": "Física Teórica II",
	"course_faculty": "Facultad de Ingeniería Mecánica e Industrial",
	"start_date": 1588824000,
	"end_date": 1620360000
	},
	{
	"id": 4,
	"course_name": "Programación Web Avanzada",
	"course_faculty": "Facultad de Matemática, Física y
	Computación",
	"start_date": 1588824000,
	"end_date": 1620360000
	},
	{
	"id": 5,
	"course_name": "Ingeniería de Software III",
	"course_faculty": "Facultad de Matemática, Física y
	Computación",
	"start_date": 1588824000,
	"end_date": 1620360000
	}
]}


------------------------------
Carlos Javier Palacios Morales
Copyright UCLV 2023
------------------------------
