## Starting Create Body Class

    import 'package:flutter/cupertino.dart';
    import 'package:flutter/material.dart';

    class HomePage extends StatefulWidget {
      @override
    _HomePageState createState() => _HomePageState();
    }

    class _HomePageState extends State<HomePage> {
      @override
      Widget build(BuildContext context) {
        return SingleChildScrollView(
          child: Padding(
            padding: const EdgeInsets.all(10),
            child: Column(children: [

            ]),
          ));
      }
    }
## Padding

    Padding(
                  padding: const EdgeInsets.fromLTRB(left, top, right, bottom),
                  child: 
                )

## Boarder

    Container(
                  height: 150,
                  width: 600,
                  decoration: BoxDecoration(
                    border: Border.all(
                      color: Colors.blue,
                    ),
                    borderRadius: BorderRadius.circular(10.0),
                  ),
                  child: ***Body***
              )
