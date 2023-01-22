# EP31. 데이터와 단짝 친구, SQL

## 데이터베이스와 SQL은 어떻게 상호작용할까?

- 데이터베이스는 정보를 저장하고 관리하는 시스템입니다. SQL(Structured Query Language)는 데이터베이스를 조작하는 언어로, 데이터베이스에 저장된 정보를 조회, 삽입, 수정, 삭제하는데 사용됩니다. 예를 들어, SQL문을 사용하여 테이블에서 특정 조건을 만족하는 레코드를 조회하거나, 새로운 레코드를 추가하거나, 기존 레코드를 수정하는 것이 가능합니다.

## SQL을 프로그래밍 언어로 쓸 수 있게 해주는 ORM

- ORM (Object-Relational Mapping) is a programming technique that allows developers to interact with a database using an object-oriented programming language, rather than using a language specific to the database, such as SQL. ORM creates a "`**virtual object database**`" that can be used from within the programming language, allowing developers to work with objects and classes, instead of tables and rows. ORM tools automatically handle the translation between the programming language and SQL, allowing developers to write code that interacts with the database in a more natural and intuitive way. This can simplify the process of working with databases and make the code more maintainable, as well as increasing the flexibility in working with different databases.

## 각 언어 ORM

There are many popular ORM tools that are widely used in different programming languages. Some examples include:

- Hibernate for Java: A widely used ORM tool for Java that supports both JPA and native Hibernate APIs.
- ActiveRecord for Ruby on Rails: An ORM tool that is built into the Ruby on Rails web framework and provides a simple, ActiveRecord-like API for working with databases.
- Entity Framework for .NET: A popular ORM tool for the .NET platform that supports a variety of databases and offers both code-first and database-first approaches.
- Doctrine for PHP: A flexible ORM tool for PHP that supports a wide range of databases and offers both active record and data mapper patterns.
- SQLAlchemy for Python: A powerful ORM tool for Python that supports a wide range of databases and offers both a simple and a powerful API.

For Node.js, There are several ORM tools that are widely used with Node.js, such as:

- Sequelize: A popular ORM for Node.js that supports a variety of databases including MySQL, PostgreSQL, and SQLite.
- Mongoose: A popular ORM for MongoDB, Mongoose provides a simple and elegant MongoDB object model.

For Python, some of the most popular ORM tools include:

- SQLAlchemy: A powerful ORM tool for Python that supports a wide range of databases and offers both a simple and a powerful API.
- Django ORM: A built-in ORM tool for the Django web framework that supports a variety of databases, including PostgreSQL, MySQL, and SQLite.
- Peewee: A simple, lightweight ORM tool for Python that supports a variety of databases, including PostgreSQL, MySQL, and SQLite.

These are some examples of ORM tools that are widely used with Node.js and Python, but there are many other options available depending on the specific requirements and the databases you are using.

## Mongoose 사용 예

- Here's an example of how you might use Mongoose in a Node.js application to interact with a MongoDB database:

```jsx

const mongoose = require('mongoose');

// Connect to MongoDB
mongoose.connect('mongodb://localhost/mydb', { useNewUrlParser: true });

// Define a schema for a collection of "Person" documents
const personSchema = new mongoose.Schema({
    name: String,
    age: Number
});

// Create a model for the "Person" collection
const Person = mongoose.model('Person', personSchema);

// Insert a new "Person" document
const jim = new Person({ name: 'Jim', age: 25 });
jim.save(function (err) {
    if (err) return handleError(err);
    // saved!
});

// Find all "Person" documents
Person.find({}, function (err, people) {
    if (err) return handleError(err);
    console.log(people);
});

```

- In this example, we first import the **`mongoose`** module and use it to connect to a MongoDB database. Then we define a schema for a collection of "Person" documents, which will have a name and an age field. The **`mongoose.model()`** function is then used to create a model for the "Person" collection, which can be used to create, read, update and delete documents in the collection.
- In this example, we use the model to insert a new "Person" document and after that, we use the find method to retrieve all people from the collection.
- You can also use the **`mongoose`** module to define relationships between collections and perform more advanced queries, as well as to perform validation and other operations on the data.

## Django ORM 사용 예

- here's an example of how you might use the Django ORM in a Python application to interact with a PostgreSQL database:

```python

from django.db import models

# Define a model for a "Person" table
class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)

# Insert a new person into the "Person" table
p = Person(first_name="John", last_name="Doe")
p.save()

# Find all people in the "Person" table
people = Person.objects.all()
print(people)

```

- In this example, we first import the **`models`** module from **`django.db`** and use it to define a model for a "Person" table, which will have a first_name and last_name fields.
- In this example, we use the model to insert a new "Person" and after that, we use the **`objects.all()`** method to retrieve all people from the table.
- Django ORM provides a lot of querying options like filter, exclude, get, etc. You can also use the **`Django ORM`** to define relationships between tables, perform advanced queries and perform validation and other operations on the data.
- Django ORM is built-in to the Django web framework and it provides a simple, active-record-like API for working with databases. It also provides many other features such as support for migrations, transactions, and more.

## NoSQL VS SQL

- NoSQL과 SQL은 서로 다른 두 종류의 데이터베이스로 각각 장단점이 있다.
- 관계형 데이터베이스라고도 하는 SQL(Structured Query Language) 데이터베이스는 스키마가 고정된 테이블에 데이터를 저장합니다. 데이터는 행과 열로 구성되며 각 행은 단일 레코드를 나타내며 각 열은 해당 레코드의 필드를 나타냅니다. SQL 데이터베이스는 구조화된 데이터를 처리하는 데 적합하며 고급 쿼리 및 인덱싱 기능을 지원합니다. SQL 데이터베이스의 예로는 MySQL, Postgre 등이 있습니다SQL 및 Oracle.
- 반면 NoSQL(Not Only SQL) 데이터베이스는 스키마가 고정되어 있지 않으며 JSON, BSON 또는 키-값 쌍과 같은 다양한 형식으로 데이터를 저장할 수 있습니다. NoSQL 데이터베이스는 많은 양의 비구조화 또는 반구조화 데이터를 처리하도록 설계되었으며 여러 컴퓨터에 걸쳐 수평적으로 확장할 수 있습니다. 그들은 빅 데이터 처리와 실시간 데이터 처리에 적합하다. NoSQL 데이터베이스의 예로는 몽고DB, 카산드라, 레디스 등이 있다.
- NoSQL 데이터베이스는 더 유연하고 수평적으로 확장 가능하며 비정형 데이터를 처리할 수 있지만 SQL 데이터베이스에 비해 복잡한 관계, 복잡한 트랜잭션 및 더 제한된 쿼리 기능에는 적합하지 않습니다. SQL 데이터베이스는 보다 엄격하지만 복잡한 관계와 트랜잭션을 처리하고 고급 쿼리 기능을 제공할 수 있습니다.
- 사용 사례 및 작업 중인 데이터에 따라 특정 프로젝트에 사용할 데이터베이스 유형을 결정하기 전에 두 유형의 데이터베이스 간의 차이점과 기능을 이해하는 것이 중요합니다.
