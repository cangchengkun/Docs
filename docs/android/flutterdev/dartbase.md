# 常使用的库

[material-library](https://api.flutter.dev/flutter/material/material-library.html)

[design](https://material.io/design/)

[widgetLib](https://api.flutter.dev/flutter/widgets/widgets-library.html)

[Google字体库](https://fonts.google.com/)

[FlutterUI列表](https://itsallwidgets.com/)

[大厂Appdemo](https://flutter.dev/showcase)

[Flutter开源列表](https://flutterevents.com/)

[Flutter源代码下载地址](https://flutterx.com/)

[Flutter2019架构](https://flutterx.com/)

[Flutter发布到Githbuio](https://www.youtube.com/watch?v=TJDSQBm51cI&feature=youtu.be)

## 项目中可用UI

[项目中可用UI](https://marcinszalek.pl/flutter/bmi-calculator-gender/)

## 屏幕适配

[适配不同的屏幕](https://www.youtube.com/watch?v=TJDSQBm51cI&feature=youtu.be)

## 机器学习Flutter

[Flutter集成机器学习](https://medium.com/@rishab_28475/running-automl-models-with-flutter-automl-vision-edge-38038139cb14)

[实时图像检测](https://blog.usejournal.com/real-time-object-detection-in-flutter-b31c7ff9ef96)


## Flutter状态处理

可能作为一个前端，在学习 Flutter 的过程中，总感觉非常非常相似 React Native，甚至于，其中还是有state的概念 setState，所以在 Flutter 中，也当然会存在非常多的解决方案，比如 redux 、RxDart 还有 Scoped Model等解决方案。今天，我们主要介绍下常用的两种 State 管理解决方案：redux、scoped model。

scoped_model 支持在子View中能够获取fuView的逻辑

[scoped_model状态处理相关的逻辑](https://pub.flutter-io.cn/packages/scoped_model#-readme-tab-)




# 对平台的操作

    * Information about the environment in which the current program is running.
    *
    * Platform provides information such as the operating system,
    * the hostname of the computer, the value of environment variables,
    * the path to the running program,
    * and so on.

[platform.dart](/Users/cuco/flutter/bin/cache/pkg/sky_engine/lib/io/platform.dart)

[foundation](/Users/cuco/flutter/packages/flutter/lib/src/foundation/platform.dart)

## 异步处理

    // -------------------------------------------------------------------
    // Controller for creating and adding events to a stream.
    // Type of a stream controller's `onListen`, `onPause` and `onResume` callbacks.
    // -------------------------------------------------------------------

# 需要解决的问题:

    How to create constructors
    Different ways to specify parameters
    When and how to create getters and setters
    How Dart handles privacy
    How to create factories
    How functional programming works in Dart
    Other core Dart concepts

# 为什么Flutter使用Dart
[Why Flutter Uses Dart](https://hackernoon.com/why-flutter-uses-dart-dd635a054ebf)


# 开发资源

## 方法级联

## Dart如何实现多线程

Note: All Dart code runs in the context of an isolate that owns all of the memory that the Dart code uses. While Dart code is executing, no other code in the same isolate can run.


If you want multiple parts of Dart code to run concurrently, you can run them in separate isolates. (Web apps use workers instead of isolates.) Multiple isolates run at the same time, usually each on its own CPU core. Isolates don’t share memory, and the only way they can interact is by sending messages to each other. For more information, see the documentation for isolates or web workers.
Asynchrony support, a section in the language tour.
API reference documentation for

[futures](https://api.dart.dev/stable/2.4.0/dart-async/Future-class.html),

[isolates](https://api.dart.dev/stable/2.4.0/dart-isolate/dart-isolate-library.html), and

[web workers](https://api.dart.dev/stable/2.4.0/dart-html/Worker-class.html).

Flutter如何设置显示方向？
The MyAppBar widget creates a Container with a height of 56 device-independent pixels with an internal padding of 8 pixels
Theme.of(context).primaryColor; 处理APP样式相关的数据

# 调试工具

# 优化、优化工具的使用
# 函数式编程

# first coding
1.定义类
2.定义私有变量
3.定义get、set方法
4.toString的使用
5.构造方法的使用
6.定义只读、只写的变量
7.Dart doesn't support overloading constructors and handles this situation differentl
8.可选的名字参数

    class Bicycle{
      int cadence;
      int _speed = 10;
      int get speed => this._speed;
      int gear;

      Bicycle(int cadence,int gear){
        this.cadence = cadence;
        this.gear = gear;
      }

      void applyBrake(int decrement){
        this._speed -= decrement;
      }

      void speedUp(int increment){
        _speed += increment;
      }
      @override
      String toString() => 'Bicycle:$_speed mph';

    }


    void main(){
      var bike = Bicycle(2,1);
      print(bike);
    }


## 可选参数
1.参数使用名字


    import 'dart:math';

    class Rectangle {
      int width;
      int height;
      Point origin;
      Rectangle({this.origin = const Point(0, 0), this.width = 0, this.height = 0});

      @override
      String toString() =>
          'Origin: (${origin.x}, ${origin.y}), width: $width, height: $height';
    }

    main() {
      print(Rectangle(origin: const Point(10, 20), width: 100, height: 200));
      print(Rectangle(origin: const Point(10, 10)));
      print(Rectangle(width: 200));
      print(Rectangle());
    }
