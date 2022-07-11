# SQL_HW_DDL

Таблица employees

Создать таблицу employees

- id. serial, primary key,
- employee_name. Varchar(50), not null
  Наполнить таблицу employee 70 строками.

```SQL
create table employees(
id serial primary key,
employee_name Varchar(50) not null
);

insert into employees(employee_name)
values ('Marcus'),
	('Zeus'),
	('Ike'),
	('Izaiah'),
	('Zephaniah'),
	('Liam'),
	('Hamza'),
	('Quinton'),
	('Jason'),
	('Preston'),
	('Ulrich'),
	('Paul'),
	('Rafael'),
	('Xander'),
	('Juan'),
	('Robert'),
	('Fabian'),
	('Isiah'),
	('Prince'),
	('Atlas'),
	('Yanni'),
	('Justin'),
	('Zack'),
	('Isidro'),
	('Olivier'),
	('Lewis'),
	('Landyn'),
	('Daniel'),
	('Varun'),
	('Kane'),
	('Lukas'),
	('Wiley'),
	('Promise'),
	('Natan'),
	('Tyrone'),
	('Walter'),
	('Ismail'),
	('Myles'),
	('Mark'),
	('Isreal'),
	('Marshall'),
	('John'),
	('Davis'),
	('Zacharias'),
	('Yoshito'),
	('Wilmer'),
	('Juan'),
	('Patrick'),
	('Ziyad'),
	('Vincent'),
	('Jace'),
	('Zac'),
	('Connor'),
	('Fisher'),
	('Uria'),
	('Varden'),
	('Titus'),
	('Trevor'),
	('Promise'),
	('Maddox'),
	('Waylen'),
	('Troy'),
	('Gilbert'),
	('Sawyer'),
	('Issac'),
	('Forrest'),
	('Omari'),
	('Finley'),
	('Ozzy'),
	('Jameson');
```

Таблица salary

Создать таблицу salary

- id. Serial primary key,
- monthly_salary. Int, not null
  Наполнить таблицу salary 15 строками:
- 1000
- 1100
- 1200
- 1300
- 1400
- 1500
- 1600
- 1700
- 1800
- 1900
- 2000
- 2100
- 2200
- 2300
- 2400
- 2500

```SQL
create table salary(
	id serial primary key,
	monthly_salary INT not null
)

insert into salary(monthly_salary)
values (1000),
		(1100),
		(1200),
		(1300),
		(1400),
		(1500),
		(1600),
		(1700),
		(1800),
		(1900),
		(2000),
		(2100),
		(2200),
		(2300),
		(2400),
		(2500);
```

Таблица employee_salary

Создать таблицу employee_salary

- id. Serial primary key,
- employee_id. Int, not null, unique
- salary_id. Int, not null
  Наполнить таблицу employee_salary 40 строками:
- в 10 строк из 40 вставить несуществующие employee_id

```SQL
create table employee_salary(
	id serial primary key,
	emplayee_id INT not null unique,
	salary_id INT not null
)

insert into employee_salary(emplayee_id, salary_id)
values (3,7),
		(1,4),
		(5,9),
		(40,13),
		(23,4),
		(11,2),
		(52,10),
		(15,13),
		(26,4),
		(16,1),
		(33,7),
		(77,12),
		(89,14),
		(98,15),
		(79,2),
		(12,3),
		(97,8),
		(91,10),
		(84,15),
		(45,12),
		(99,9),
		(78,7),
		(107,5),
		(14,12),
		(18,5),
		(7,3),
		(28,7),
		(31,13),
		(29,7),
		(30,2),
		(50,14),
		(53,8),
		(17,10),
		(2,11),
		(19,12),
		(43,13),
		(44,7),
		(67,6),
		(62,3),
		(70,1);
```

Таблица roles

Создать таблицу roles

- id. Serial primary key,
- role_name. int, not null, unique
  Поменять тип столба role_name с int на varchar(30)
  Наполнить таблицу roles 20 строками:

```SQL
create table roles(
id serial primary key,
role_name INT not null unique
)

alter table roles
alter column role_name type VARCHAR(30);

insert into roles(role_name)
values ('Junior Python developer'),
('Middle Python developer'),
('Senior Python developer'),
('Junior Java developer'),
('Middle Java developer'),
('Senior Java developer'),
('Junior JavaScript developer'),
('Middle JavaScript developer'),
('Senior JavaScript developer'),
('Junior Manual QA engineer'),
('Middle Manual QA engineer'),
('Senior Manual QA engineer'),
('Project Manager'),
('Designer'),
('HR'),
('CEO'),
('Sales manager'),
('Junior Automation QA engineer'),
('Middle Automation QA engineer'),
('Senior Automation QA engineer');
```

Таблица roles_employee

Создать таблицу roles_employee

- id. Serial primary key,
- employee_id. Int, not null, unique (внешний ключ для таблицы employees, поле id)
- role_id. Int, not null (внешний ключ для таблицы roles, поле id)
  Наполнить таблицу roles_employee 40 строками:

```SQL
create table roles_employee(
id serial primary key,
employee_id INT not null unique,
foreign key (employee_id)
references employees(id),
role_id INT not null,
foreign key (role_id)
references roles(id)
)

insert into roles_employee(employee_id, role_id)
values (3,7),
(1,4),
(5,9),
(40,13),
(23,4),
(11,2),
(52,10),
(15,13),
(26,4),
(16,1),
(33,7),
(27,12),
(9,14),
(8,15),
(39,2),
(12,3),
(47,8),
(61,10),
(24,15),
(45,12),
(69,9),
(48,7),
(57,5),
(14,12),
(18,5),
(7,3),
(28,7),
(31,13),
(29,7),
(30,2),
(50,14),
(53,8),
(17,10),
(2,11),
(19,12),
(43,13),
(44,7),
(67,6),
(62,3),
(70,1);
```
[Back to page Course_V_Ksendzov](https://yuliakondratsiuk.github.io/Course_V_Ksendzov/) 
