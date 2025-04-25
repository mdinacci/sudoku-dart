# sudoku-dart


## 关于 about

 [![License](https://img.shields.io/badge/License-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE) 
 [![License](https://img.shields.io/badge/BSD-3-Clause.svg)](https://opensource.org/licenses/BSD-3-Clause)
 ![pub package](https://img.shields.io/pub/v/sudoku_dart.svg)

数独 **解题器** 和 **生成器** 开源库 `dart` 版

支持对 唯一/非唯一解数独进行解题 以及 随机唯一解数独生成

open-source sudoku solver and puzzle generator library with `dart`

## 安装 install

### only-dart

Depend on it

Run this command:

With Dart:
```dart
dart pub add sudoku_dart
```

### with-flutter :
```dart
flutter pub add sudoku_dart
```

This will add a line like this to your package's pubspec.yaml (and run an implicit dart pub get):

```yaml
dependencies:
  sudoku_dart: ^1.2.0
```

Import it
```dart
import 'package:sudoku_dart/sudoku_dart.dart';
```

## 使用 tutorial

### 解题 solver
```dart
import 'package:sudoku_dart/sudoku_dart.dart';
// 支持数独解题
// 输入一维数组的puzzle,-1为待填空
 List<int> puzzle = [
    -1,-1,8,    9,-1,6,     -1,-1,5,
    -1,4,3,     -1,-1,-1,   -1,2,-1,
    -1,-1,-1,   -1,-1,-1,   -1,-1,-1,

    -1,-1,4,    -1,-1,-1,   9,-1,-1,
    5,-1,-1,    -1,4,-1,    6,8,-1,
    -1,-1,-1,   1,-1,-1,    -1,-1,-1,

    2,-1,-1,    -1,8,-1,    -1,7,-1,
    -1,-1,-1,   -1,3,4,     1,-1,-1,
    -1,6,-1,    -1,-1,9,    -1,-1,-1,
  ];

sudoku = Sudoku(puzzle);

// if you need check this puzzle is one-solution sudoku or not,use  strict:true 
// sudoku = Sudoku(puzzle, strict: true);

// debug print
sudoku.debug();
// origin puzzle
sudoku.puzzle;
// sudoku solution
sudoku.solution;
```

### 数独生成器 generator
```dart
import 'package:sudoku_dart/sudoku_dart.dart';
// generate random puzzle with one-solution
// Level : easy(简单), medium(中等), hard(困难), expert(专家)
Sudoku sudoku = Sudoku.generate(Level.expert);
// Generate a random puzzle from a seed
int fixedSeed = 4567805;
Sudoku sudoku = Sudoku.generate(Level.expert, fixedSeed);
```

## more
this library use on `sudoku-flutter` , support for android and iOS app  , if interesting welcome visit this repository : 

[einsitang/sudoku-flutter](https://github.com/einsitang/sudoku-flutter)

