# LearningPlusPlus

[中文](README.md) | English

[![CMake Verification](https://github.com/LiTongShuo-edu/LearningPlusPlus/actions/workflows/cmake.yml/badge.svg)](https://github.com/LiTongShuo-edu/LearningPlusPlus/actions/workflows/cmake.yml)

A C++ fundamentals learning portfolio containing early personal exercises, recreations of lost exercises, and later examples focused on pointers, memory, and test-result statistics. Code is organized under [`代码案例/`](./代码案例/), with directory names distinguishing retained handwritten work, recreated exercises, and later additions.

## Project navigation

| Topic | Where to look | Details |
| --- | --- | --- |
| Pointers, references, and dynamic memory | [`代码案例/指针与引用^`](./代码案例/指针与引用^) and [`代码案例/内存管理^`](./代码案例/内存管理^) | Later fundamentals examples with automated tests |
| Test statistics and verification | [`代码案例/案例-测试结果统计^`](./代码案例/案例-测试结果统计^) and [debugging and verification notes](./docs/调试与验证说明.md) | Pass-rate summaries, retained failures, and test instructions |
| Build and automated tests | [`CMakeLists.txt`](./CMakeLists.txt) and [GitHub Actions](https://github.com/LiTongShuo-edu/LearningPlusPlus/actions) | Windows / MSVC build and CTest |
| Sources and AI collaboration | [source boundaries and originality](./docs/参考边界与原创声明.md) and [AI collaboration record](./docs/AI协作开发记录.md) | Distinguishes handwritten work, AI-assisted recreations, and later examples |

**Recorded verification:** 13 recreated `＊` cases and three `^` extensions built successfully, with 16/16 automated tests passing. All 34 early handwritten programs compiled independently after one missing closing brace was fixed with Codex assistance.

## Background and source labels

The early exercises were written by the author in 2019–2020 on an old computer. Some survived on a personal OneDrive account; others were lost when the computer failed. Directories without a suffix contain retained handwritten source. A full-width `＊` identifies lost exercises recreated with Codex assistance; `^` identifies later examples developed with Codex assistance.

| Directory suffix | Meaning | Publication treatment |
| --- | --- | --- |
| None | Retained early handwritten exercises | Organized from originals; one compilation bug was fixed with Codex assistance |
| `＊` | Recreated lost exercises | Recreated public implementations; no finished course source is included |
| `^` | Later collaborative extensions | Additional exercises on pointers, memory, and test results |

The full-width star is used because Windows filenames cannot contain the ASCII `*`. Both `＊` and `^` sources involved AI programming collaboration; only unsuffixed sources are published as retained early handwritten code.

## Contents

| Stage | Example directories | Topics |
| --- | --- | --- |
| Early handwritten basics | `HelloWorld`, basic types, operators, branching, loops, and other early examples (34 total) | Syntax and control flow |
| Recreated basics | `案例-五只小猪称体重＊`, `案例-数组元素逆置＊`, `冒泡排序＊`, `案例-考试成绩统计＊`, `案例-教师与学生信息＊`, `案例-英雄年龄排序＊` | Arrays, simple algorithms, structures |
| Recreated stage 2 | `案例-通讯录管理系统＊` | Console menus and in-memory CRUD |
| Recreated stage 3 | `案例-立方体类＊`, `案例-点和圆的关系＊`, `案例-多态计算器＊`, `案例-制作饮品＊`, `案例-电脑组装＊` | Classes, composition, inheritance, polymorphism |
| Recreated stage 4 | `案例-职工管理系统＊` | Polymorphic employee types, file I/O, CRUD, sorting |
| Later extensions | `指针与引用^`, `内存管理^`, `案例-测试结果统计^` | Pointers, references, dynamic memory, test summaries |

Further documentation:

- [Learning path and topics](./docs/学习路线与知识点.md)
- [Debugging and verification](./docs/调试与验证说明.md)
- [AI collaboration record](./docs/AI协作开发记录.md)
- [Compilation record for handwritten work](./docs/手写旧作编译记录.md)
- [Source boundaries and originality statement](./docs/参考边界与原创声明.md)

## Build and run

Requirements: a C++17 compiler such as Visual Studio 2022 / MSVC, and CMake 3.16 or later.

The top-level CMake configuration builds all `＊` recreations and `^` extensions by default. Unsuffixed historical exercises are presented separately with independent compilation records; one identified compilation bug received a documented minimal fix.

```powershell
cmake -S . -B build
cmake --build build --config Debug
ctest --test-dir build -C Debug --output-on-failure
```

In Windows command lines, `^` is an escape character. CMake generates safe-path copies of the three extension directories in the build directory for compilation; the public source remains in the directories ending in `^`. GitHub Actions runs the build and CTest on Windows / MSVC for pushes to `main` and pull requests.

## Recorded validation

On 2026-05-27, using Windows, Visual Studio 2022 / MSVC, C++17, and CMake:

- All 13 `＊` cases and three `^` examples built; all 16 automated tests passed.
- The address-book demo covered adding, editing, searching, deleting, and clearing; the employee manager covered file save/load, editing, deletion, and display.
- `案例-测试结果统计^` reported five cases, four passes, one failure, and an 80.0% pass rate.
- All 34 unsuffixed handwritten sources were organized. In addition to UTF-8 conversion and directory organization, a missing loop-closing brace in `代码案例/案例-猜数字/源.cpp` was added with Codex assistance.
- After the fix, all 34 compiled independently under MSVC / C++17.

## Source and collaboration boundaries

- `＊` cases recreate exercises previously practiced by the author but subsequently lost; the public implementations were recreated with Codex assistance.
- Private course materials are not published as project results. The repository contains no course handouts, screenshots, archives, finished source, or other third-party originals.
- Third-party learning materials were not authorized for republication; their source was not copied or renamed for publication.
- `^` examples are additional exercises created during organization.
- Codex assisted implementation, debugging, verification, and organization of recreations, extensions, and documentation. Users should read the code and be able to explain its behavior.
