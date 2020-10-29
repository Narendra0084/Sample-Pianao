# Sample-Pianao



import 'package:audioplayers/audio_cache.dart';
import 'package:flutter/material.dart';

void main() => runApp(XylophoneApp());

class XylophoneApp extends StatelessWidget {

  void pianoSound( int numberSound){
    final player = AudioCache();
    player.play('note$numberSound.wav');
  }
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.black,
        body: SafeArea(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.stretch,
            children: <Widget>[
                Expanded(
                  child: FlatButton(
                    color: Colors.red,
                    onPressed: () {
                      pianoSound(1);
                    }, child: Text('Click Me 1'),
                  ),
                ),
              Expanded(
                child: FlatButton(
                  color: Colors.green,
                  onPressed: () {
                    pianoSound(2);
                  }, child: Text('Click Me 2'
                    ),
                ),
              ),
              Expanded(
                child: FlatButton(
                  color: Colors.orange,
                  onPressed: () {
                    pianoSound(3);
                  }, child: Text('Click Me 3'),
                ),
              ),
              Expanded(
                child: FlatButton(
                  color: Colors.yellow,
                  onPressed: () {
                    pianoSound(4);
                  }, child: Text('Click Me 4'),
                ),
              ),
              Expanded(
                child: FlatButton(
                  color: Colors.grey,
                  onPressed: () {
                    pianoSound(5);
                  }, child: Text('Click Me 5'),
                ),
              ),
              Expanded(
                child: FlatButton(
                  color: Colors.white,
                  onPressed: () {
                    pianoSound(6);
                  }, child: Text('Click Me 6'),
                ),
              ),
              Expanded(
                child: FlatButton(
                  color: Colors.teal.shade900,
                  onPressed: () {
                    pianoSound(7);
                  }, child: Text('Click Me 7'),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
