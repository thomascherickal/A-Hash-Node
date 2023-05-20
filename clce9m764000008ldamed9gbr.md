---
title: "Part 6: Flutter and Dart MVC Web App Students Database full source code separated into Multiple Files Clean Code"
seoTitle: "Create a Flutter and Dart MVC app in ten minutes!"
seoDescription: "This program will change the world and everything we know so far"
datePublished: Mon Jan 02 2023 03:51:52 GMT+0000 (Coordinated Universal Time)
cuid: clce9m764000008ldamed9gbr
slug: part-6-flutter-and-dart-mvc-web-app-students-database-full-source-code-separated-into-multiple-files-clean-code
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/b8178035ee3252c3c15a2ff5711d6e2d.jpeg
tags: mvc, dart, flutter, clean-code, automatically-created

---

Here is an example of a Flutter and Dart MVC web app that manages a student database:

```python
Copy codeimport 'package:flutter/material.dart';
import 'package:flutter_web/model/student.dart';
import 'package:flutter_web/service/student_service.dart';

class StudentPage extends StatefulWidget {
  @override
  State<StatefulWidget> createState() => new _StudentPageState();
}

class _StudentPageState extends State<StudentPage> {
  List<Student> students;
  StudentService studentService;

  @override
  void initState() {
    studentService = new StudentService();
    studentService.getStudents().then((students) {
      setState(() {
        this.students = students;
      });
    });
    super.initState();
  }

  @override
  Widget build(BuildContext context) {
    return new Scaffold(
      appBar: new AppBar(
        title: new Text('Students'),
      ),
      body: new ListView.builder(
        itemCount: students.length,
        itemBuilder: (BuildContext context, int index) {
          return new Card(
            child: new Column(
              mainAxisSize: MainAxisSize.min,
              children: <Widget>[
                new ListTile(
                  leading: const Icon(Icons.person),
                  title: new Text(students[index].name),
                  subtitle: new Text(students[index].email),
                ),
                new ButtonTheme.bar(
                  child: new ButtonBar(
                    children: <Widget>[
                      new FlatButton(
                        child: const Text('DETAILS'),
                        onPressed: () { /* ... */ },
                      ),
                      new FlatButton(
                        child: const Text('EDIT'),
                        onPressed: () { /* ... */ },
                      ),
                      new FlatButton(
                        child: const Text('DELETE'),
                        onPressed: () { /* ... */ },
                      ),
                    ],
                  ),
                ),
              ],
            ),
          );
        },
      ),
      floatingActionButton: new FloatingActionButton(
        child: const Icon(Icons.add),
        onPressed: () {
          Navigator.of(context).pushNamed('/student/add');
        },
      ),
    );
  }
}
```

This is just a basic example, and you might want to customize it to fit your specific needs. You can also find more information about building web apps with Flutter and Dart in the Flutter documentation: [**https://flutter.dev/docs/get-started/web**](https://flutter.dev/docs/get-started/web)

![Thomas Cherickal](https://chat.openai.com/_next/image?url=https%3A%2F%2Flh3.googleusercontent.com%2Fa%2FAEdFTp7h6Hw9EN3Tk8o1UgJ_F80KYEkIppfFa9TYWevEnA%3Ds96-c&w=64&q=75 align="left")

split it into separate files

Sure! Here is how you can split the code above into separate files:

`student.dart`:

```python
Copy codeimport 'package:flutter/material.dart';
import 'package:flutter_web/model/student.dart';
import 'package:flutter_web/service/student_service.dart';

class StudentPage extends StatefulWidget {
  @override
  State<StatefulWidget> createState() => new _StudentPageState();
}

class _StudentPageState extends State<StudentPage> {
  List<Student> students;
  StudentService studentService;

  @override
  void initState() {
    studentService = new StudentService();
    studentService.getStudents().then((students) {
      setState(() {
        this.students = students;
      });
    });
    super.initState();
  }

  @override
  Widget build(BuildContext context) {
    return new Scaffold(
      appBar: new AppBar(
        title: new Text('Students'),
      ),
      body: new ListView.builder(
        itemCount: students.length,
        itemBuilder: (BuildContext context, int index) {
          return new Card(
            child: new Column(
              mainAxisSize: MainAxisSize.min,
              children: <Widget>[
                new ListTile(
                  leading: const Icon(Icons.person),
                  title: new Text(students[index].name),
                  subtitle: new Text(students[index].email),
                ),
                new ButtonTheme.bar(
                  child: new ButtonBar(
                    children: <Widget>[
                      new FlatButton(
                        child: const Text('DETAILS'),
                        onPressed: () { /* ... */ },
                      ),
                      new FlatButton(
                        child: const Text('EDIT'),
                        onPressed: () { /* ... */ },
                      ),
                      new FlatButton(
                        child: const Text('DELETE'),
                        onPressed: () { /* ... */ },
                      ),
                    ],
                  ),
                ),
              ],
            ),
          );
        },
      ),
      floatingActionButton: new FloatingActionButton(
        child: const Icon(Icons.add),
        onPressed: () {
          Navigator.of(context).pushNamed('/student/add');
        },
      ),
    );
  }
}
```

`student_service.dart`:

```python
Copy codeimport 'package:flutter_web/model/student.dart';

class StudentService {
  List<Student> students = [
    new Student(1, 'Alice', 'alice@example.com'),
    new Student(2, 'Bob', 'bob@example.com'),
    new Student(3, 'Charlie', 'charlie@example.com'),
  ];

  Future<List<Student>> getStudents() async {
    return students;
  }
}
```

`student.dart`:

```python
Copy codeclass Student {
  int id;
  String name;
  String email;

  Student(this.id, this.name, this.email);
}
```

I hope this helps!

[Next: TDD Telephone Database in Go](https://hashnode.com/post/clce9m764000008ldamed9gbr)