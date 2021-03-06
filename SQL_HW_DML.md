# SQL_HW_DML

1. Вывести все поля и все строки.

	```SQL
	SELECT *
	FROM students;
	```

2. Вывести всех студентов в таблице

	```SQL
	SELECT id, name
	FROM students;
	```

3. Вывести только Id пользователей

	```SQL
	SELECT id
	FROM students;
	```

4. Вывести только имя пользователей

	```SQL
	SELECT name
	FROM students;
	```

5. Вывести только email пользователей

	```SQL
	SELECT email
	FROM students;
	```

6. Вывести имя и email пользователей

	```SQL
	SELECT name, email
	FROM students;
	```

7.  Вывести id, имя, email и дату создания пользователей

	```SQL
	SELECT id, name, email, created_on
	FROM students;
	```

8. Вывести пользователей где password 12333

	```SQL
	SELECT *
	FROM students
	WHERE password = '12333';
	```

9. Вывести пользователей которые были созданы 2021-03-26 00:00:00

	```SQL
	SELECT *
	FROM students
	WHERE created_on = '2021-03-26 00:00:00';
	```

10. Вывести пользователей где в имени есть слово Анна

	```SQL
	SELECT *
	FROM students
	WHERE name LIKE '%Anna%';
	```

11. Вывести пользователей где в имени в конце есть 8

	```SQL
	SELECT *
	FROM students
	WHERE name LIKE '%8';
	```

12. Вывести пользователей где в имени в есть буква а

	```SQL
	SELECT *
	FROM students
	WHERE name LIKE '%a%';
	```

13. Вывести пользователей которые были созданы 2021-07-12 00:00:00

	```SQL
	SELECT *
	FROM students
	WHERE created_on = '2021-07-12 00:00:00';
	```

14. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и имеют пароль 1m313

	```SQL
	SELECT _
	FROM students
	WHERE created_on = '2021-07-12 00:00:00'
	AND password = '1m313';
	```

15. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть слово Andrey

	```SQL
	SELECT *
	FROM students
	WHERE created_on = '2021-07-12 00:00:00'
	AND name like '%Andrey%';
	```

16. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть цифра 8

	```SQL
	SELECT *
	FROM students
	WHERE created_on = '2021-07-12 00:00:00'
	AND name like '%8%';
	```

17. Вывести пользователя у которых id равен 110

	```SQL
	SELECT *
	FROM students
	WHERE id = '110';
	```

18. Вывести пользователя у которых id равен 153

	```SQL
	SELECT \*
	FROM students
	WHERE id = '153';
	```

19. Вывести пользователя у которых id больше 140

	```SQL
	SELECT *
	FROM students
	WHERE id > '140';
	```

20. Вывести пользователя у которых id меньше 130

	```SQL
	SELECT *
	FROM students
	WHERE id < '130';
	```

21. Вывести пользователя у которых id меньше 127 или больше 188

	```SQL
	SELECT *
	FROM students
	WHERE id < '127' OR id > '188';

	OR

	SELECT *
	FROM students
	WHERE id BETWEEN '127' and '188';
	```

22. Вывести пользователя у которых id меньше либо равно 137

	```SQL
	SELECT *
	FROM students
	WHERE id <= '137';
	```

23. Вывести пользователя у которых id больше либо равно 137

	```SQL
	SELECT \*
	FROM students
	WHERE id >= '137';
	```

24. Вывести пользователя у которых id больше 180 но меньше 190

	```SQL
	SELECT \*
	FROM students
	WHERE id > '180' AND id < '190';
	```

25. Вывести пользователя у которых id между 180 и 190

	```SQL
	SELECT \*
	FROM students
	WHERE id BETWEEN 180 AND 190;
	```

26. Вывести пользователей где password равен 12333, 1m313, 123313

	```SQL
	SELECT *
	FROM students
	WHERE password = '12333'
	OR password = '1m313'
	OR password ='123313';

	OR

	SELECT *
	FROM students
	WHERE password IN ('12333',
					   '1m313',
					   '123313')
	```

27. Вывести пользователей где created_on равен 2020-10-03 00:00:00, 2021-05-19 00:00:00, 2021-03-26 00:00:00

	```SQL
	SELECT *
	FROM students
	WHERE created_on = '2020-10-03 00:00:00'
	OR created_on = '2021-05-19 00:00:00'
	OR created_on = '2021-03-26 00:00:00';

	OR

	SELECT *
	FROM students
	WHERE created_on IN ('2020-10-03 00:00:00',
						 '2021-05-19 00:00:00',
						 '2021-03-26 00:00:00');
	```

28. Вывести минимальный id

	```SQL
	SELECT MIN(id)
	FROM students;
	```

29. Вывести максимальный.

	```SQL
	SELECT MAX(id)
	FROM students;
	```

30. Вывести количество пользователей

	```SQL
	SELECT COUNT(\*)
	FROM students;
	```

31. Вывести id пользователя, имя, дату создания пользователя. Отсортировать по порядку возрастания даты добавления пользоватлеля.

	```SQL
	SELECT id, name, created_on
	FROM students
	ORDER by created_on;
	```

32. Вывести id пользователя, имя, дату создания пользователя. Отсортировать по порядку убывания даты добавления пользоватлеля.

	```SQL
	SELECT id, name, created_on
	FROM students
	ORDER by created_on DESC;
	```
[Back to page Course_V_Ksendzov](https://yuliakondratsiuk.github.io/Course_V_Ksendzov/) 
