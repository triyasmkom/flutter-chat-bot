# Chat Bot Flutter


## Install Flutter Package
```bash
flutter pub add flutter_gemini_bot
```

## Get Google Api Key
Kunjungi laman https;//ai.google.dev dan dapatkan google AI Api key.

## Use Package

```dart
List<ChatModel> chatList = [];
String apiKey = "your_api_key";

FlutterGeminiChat(
    chatContext: 'Example_context',
    chatList: chatList,
    apiKey: apiKey,
)
```


### Example of using the package

```dart
import 'package:flutter/material.dart';
import 'package:flutter_dotenv/flutter_dotenv.dart';
import 'package:flutter_gemini_bot/flutter_gemini_bot.dart';
import 'package:flutter_gemini_bot/models/chat_model.dart';

void main() async {
  await dotenv.load(fileName: ".env");
  runApp(const MyHomePage());
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key});

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  List<ChatModel> chatList = [];
  String apiKey = dotenv.get("api_key");

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          centerTitle: true,
          title: const Text(
            "CHAT BOT APPS",
          ),
        ),
        body: FlutterGeminiChat(
          chatContext: 'Example_context',
          chatList: chatList,
          apiKey: apiKey,
        ),
      ),
    );
  }
}

```

## Output

![image](/public/images/image1.png)


## Referensi

https://pub.dev/documentation/flutter_gemini_bot/latest/index.html


