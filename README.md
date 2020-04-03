# screeen
///flutter basic
//maindart.
import 'package:flutter/material.dart';
import 'package:screen/loginpage.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(home:LoginPage(),

    );
  }
}

///loginpage
import 'package:flutter/material.dart';
import 'package:screen/mainpage.dart';

class LoginPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: RaisedButton(
          child: Text("login"),
          onPressed: () {
            Navigator.pushReplacement(context,
                MaterialPageRoute(builder:(context){
                  return MainPage();
                }));
          },
        ),
      ),
    );
  }
}
///mainpage
import 'package:flutter/material.dart';
import 'package:screen/secondpage.dart';

class MainPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("mainpage"),
      ),
      body: Center(
        child: RaisedButton(
          child: Text("Go to Second Page"),
          onPressed: () {
            Navigator.push(context, MaterialPageRoute(builder: (context) {
              return SecondPage();
            }));
          },
        ),
      ),
    );
  }
}
///secondpage
import 'package:flutter/material.dart';

class SecondPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(appBar: AppBar(title: Text("Second Page"),),
      body: Center(
        child: RaisedButton(
          child: Text("kembali"),
          onPressed: () {
            Navigator.pop(context);
          },
        ),
      ),
    );
  }
}

