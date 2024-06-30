C = Create
R = Read
U = Update
D = Delete

* READ (creating a new QuerySet)

# To read all:

SQL -> SELECT * FROM Course
Django -> courses = Course.objects.all()

# To read filtered:

SQL -> SELECT * FROM Instructor WHERE is_full_time=False
Django -> part_time_instructors = Instructor.objects.filter(is_full_time=False)

# To retrieve filtered data where some is exluded:

Django -> filtered_instructor = Instructor.object.exlude(full_time=False).
                                filter(total_learner__gt=30000)
                                filter(first_name_startswith='M')

# To retrieve a single object if we know it is unique:

Django -> instructor_mirko = Instructur.objects.get(first_name='Mirko')
          print(instructor_mirko)

# To retrieve object in related fields:

class Course(models.Model):
    instructors = models.ManyToManyField(Instructor)

class Instructor(models.Model):

courses = Course.objects.filter(instructors__first_name= 'Mirko')