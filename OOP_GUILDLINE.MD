# GCLog Guildline For OOP Languages

## Design

![gclog](https://user-images.githubusercontent.com/4256921/167370531-66204248-b3aa-4dd8-a87c-7ebf22fd5f27.png)

- GcLog: The main class, which control log writer, log parser and tranfer cURL string to GETCURL link.
- GcLogWriter: The writer, which write your GETCURL link to any source, e.g. Developer Console, Telegram, Slack.
- ConsoleLogWriter: Default log writer, log GETCURL link to Developer Console.
- GcLogParser: The parser, which parse the any object to cURL string.
- StringLogParser: Default log parser, actually don't do anything, just string -> string.
- HttpLogParser: Abstract, help to parse http request object to cURL string.

### Output

- The main function `GcLog > log(any)`: Log any object as a GETCURL link. E.g.
 ```
 let gc = new GgLog();
 gc.log(any: request)
 ```
 
### You need to adapt more writer, parser, so
- Create new class and extend from GcLogWriter, GcLogParser
- Any http request object, which don't have cURL logging builtin function, should extend from HttpLogParser, and implement how to getHeaders(), getBody(), getMethod(), getUrl().

### Things you need to follow
- Logic at function `GcLog > logContent(string)`: Generate GETCURL link from cURL string. 
 ```
  // Create base64, utf8 needed
  // Make URL Encoded
  // Concat to 'https://getcurl.app/#body=<data>'
```
 Example -> [GCLog.swift](https://github.com/docsion/GCLogSwift/blob/42ee48aa896656a3f4f141f0a170c227d30032f1/Sources/GCLog.swift#L102)


### Standard Project
 - ✨ [GCLogSwift](https://github.com/docsion/GCLogSwift)


## OOP Languages

- ✅ [Swift](https://github.com/docsion/GCLogSwift)
- ☑️ [Kotlin](https://github.com/docsion/gclog-kt)
- ☑️ [Java](https://github.com/docsion/gclog-java)
- ☑️ [JavaScript](https://github.com/docsion/gclog-js)
- ☑️ [C++](https://github.com/docsion/gclog-cplusplus)
- C#
- Python
- R
- PHP
- Ruby
- Perl
- Dart
- Scala
- Common Lisp
- MATLAB
- Smalltalk
- SIMSCRIPT
- Object Pascal
- Objective-C
- Visual Basic.NET


## Explore GCLog at another languages
 [Swift, Kotlin, Javascript and 99+ programing languages are supported.](https://github.com/docsion/gclog)

## Contact
 https://getcurl.app/hello
