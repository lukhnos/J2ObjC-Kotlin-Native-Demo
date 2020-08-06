# J2ObjC Kotlin Native Demo
A demo for J2ObjC - Kotlin/Native Interop where Java code imports and calls Kotlin code, and then the Java and Kotlin code is translated by J2ObjC and Kotlin/Native, respectively.

Compile the Kotlin file with `kotlinc-native KotlinSide.kt -produce framework -o ComGoogleKotlinInterop`. The framework name currently needs to be the same as the package name.

Compile the Java file with `./j2objcc [path-to-file]/JavaSide.m  [path-to-file]/JavaSide.h  -framework ComGoogleKotlinInterop -F [path-to-directory-containing framework] -rpath [path-to-directory-containing framework]`

Run the resulting file with `./a.out ComGoogleKotlinInteropJavaSide`


    Copyright 2020 Google LLC

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    https://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
