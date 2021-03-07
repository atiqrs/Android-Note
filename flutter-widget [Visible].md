## Snakbar

```dart
    void snak(){
        Scaffold.of(context).showSnackBar(SnackBar(
              content: Text('Tap'),
            ));
      }
```
or

      (){Scaffold.of(context).showSnackBar(SnackBar(
          content: Text('Tap'),
        ));
        } 

# Dialog

    showDialog(
                context: context,
                builder: (context) {
                  return AlertDialog(
                    // Retrieve the text the that user has entered by using the
                    // TextEditingController.
                    content: Text(myController.text),
                  );
                },
              );

# FAB

    floatingActionButton: FloatingActionButton(
    
            // When the user presses the button, show an alert dialog containing
            // the text that the user has entered into the text field.
            
            onPressed: () {
              return showDialog(
                context: context,
                builder: (context) {
                  return *****Values*********Values********
            },
            tooltip: 'Show me the value!',
            child: Icon(Icons.text_fields),
          ),

# Button
## Elevated Button
      ElevatedButton(
                        child: Text("Button"),
                        onPressed: 
                        
                        ),

## row and middle space

        Row(
                          mainAxisAlignment: MainAxisAlignment.start,
                          children: <Widget>[
                            Flexible(fit: FlexFit.tight, child: SizedBox()),

                          ],
                        ),
                        Divider(
                          color: Color(0xffeddcd2),
                          thickness: 1,
                        ),

## Card full design

    Card(
                      margin: EdgeInsets.fromLTRB(10, 10, 10, 0),
                      shadowColor: Color(0xffeddcd2),
                      child: Padding(
                        padding: const EdgeInsets.fromLTRB(15, 10, 15, 10),
                        child: Column(
                          mainAxisSize: MainAxisSize.min,
                          children: <Widget>[

                            Row(
                              mainAxisAlignment: MainAxisAlignment.start,
                              children: <Widget>[
                                Flexible(fit: FlexFit.tight, child: SizedBox()),


                              ],
                            ),
                            Divider(
                              color: Color(0xffeddcd2),
                              thickness: 1,
                            ),

                          ],
                        ),
                      )),
