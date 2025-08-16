# Compose Performance

Understanding the Jetpack Compose mechanism is important, as it directly impacts your application's performance. Jetpack Compose introduces a new paradigm in declarative UI, driving innovative UI techniques. While the benefits of declarative UI are significant, it also presents challenges in terms of stability and UI updates. This issue is not unique to Jetpack Compose; it also affects other declarative UI frameworks like React and Flutter. These challenges are inherent to all frameworks that use a declarative approach and we can learn across all those various frameworks.

## 📓 Official Android Documentation

* [Practical performance problem-solving in Jetpack Compose](https://developer.android.com/codelabs/jetpack-compose-performance#0): The codelab on Jetpack Compose Performance provides guidelines for optimizing Compose by identifying and fixing performance issues. It covers essential techniques such as using `Lazy` components for efficient list rendering, optimizing recomposition, and leveraging tools like the Layout Inspector and Profile GPU Rendering for performance analysis. Additionally, it emphasizes best practices like minimizing the use of complex layout hierarchies and avoiding unnecessary recompositions to enhance app performance.

* [Jetpack Compose Performance](https://developer.android.com/develop/ui/compose/performance): The Jetpack Compose performance guide outlines best practices for creating efficient and smooth UIs in Compose applications. It emphasizes minimizing recomposition, using `Lazy` components for large data sets, and profiling tools to detect and fix performance issues. Additionally, it provides strategies for optimizing UI rendering and managing state effectively to ensure a responsive user experience.

* [Diagnose stability issues](https://developer.android.com/develop/ui/compose/performance/stability/diagnose): The guide on diagnosing stability issues in Jetpack Compose focuses on identifying and resolving performance problems related to recomposition and state management. It provides tools and techniques for tracking recompositions, understanding state usage, and optimizing code to prevent unnecessary UI updates. By following these practices, developers can diagnose stability issues they are facing on.

* [Fix Stability Issue](https://developer.android.com/develop/ui/compose/performance/stability/fix): The guide on fixing stability issues in Jetpack Compose emphasizes reducing unnecessary recompositions by making state objects stable and immutable. It provides techniques such as using `remember` and `derivedStateOf` to optimize state management, and advises against creating new objects during recomposition. These practices help improve performance and ensure smoother UI updates.

* [Strong Skipping Mode](https://developer.android.com/develop/ui/compose/performance/stability/strongskipping): The guide on strong skipping in Jetpack Compose highlights techniques to minimize recomposition by ensuring that composable functions are only re-executed when necessary. It discusses how the Strong Skipping mode optimizes Compose performance by introducing a new recomposition mechanism.

* [Implement custom modifier behavior using Modifier.Node](https://developer.android.com/develop/ui/compose/custom-modifiers#implement-custom): `Modifier.Node` was designed from the ground up to be far more performant than composed modifiers. For more details on the problems with composed modifiers.

* [AOSP: androidx.compose.runtime.annotation](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-main:compose/runtime/runtime-annotation/src/commonMain/kotlin/androidx/compose/runtime/annotation/compose-runtime-annotation-documentation.md): The `androidx.compose.runtime.annotation` package provides annotations used by the compiler and tooling. These annotations are published in a separate library to allow using these annotations in modules that do not depend on Compose Runtime, but may be used with Compose in other modules.

## 📚 Articles

* [New ways of optimizing stability in Jetpack Compose](https://medium.com/androiddevelopers/new-ways-of-optimizing-stability-in-jetpack-compose-038106c283cc): The article discusses new strategies for optimizing stability in Jetpack Compose, focusing on reducing unnecessary recompositions. It introduces concepts like using stable data types, the `remember` function, and the `key` modifier to manage state changes more efficiently. These methods enhance performance and ensure smoother, more responsive UIs in Compose.

* [Optimize App Performance By Mastering Stability in Jetpack Compose](https://medium.com/proandroiddev/optimize-app-performance-by-mastering-stability-in-jetpack-compose-69f40a8c785d): The article emphasizes the importance of stability in optimizing app performance. It covers techniques for reducing unnecessary recompositions by understanding stabilities, recomposition mechanism, smart recomposition, analyzing Compose Compiler metrics, and effectively stabilizing Composable functions and managing state to ensure smooth and responsive UIs. The article also highlights practical tools and methods to identify and address performance bottlenecks in Jetpack Compose.

* [6 Jetpack Compose Guidelines to Optimize Your App Performance](https://medium.com/proandroiddev/6-jetpack-compose-guidelines-to-optimize-your-app-performance-be18533721f9): The article outlines six guidelines to optimize app performance in Jetpack Compose, focusing on minimizing recomposition, using efficient data structures, and leveraging Compose's built-in tools. Key recommendations include using `remember` and `derivedStateOf` to manage state efficiently, adopting lazy components for large data sets, and profiling your app to identify and resolve performance bottlenecks.

* [Improve Your Android App Performance With Baseline Profiles](https://getstream.io/blog/android-baseline-profile/): The article explains the importance of Android Baseline Profiles in improving app performance. It highlights how these profiles help pre-compile parts of the code, reducing startup time and enhancing runtime performance. The post also provides a step-by-step guide on creating and integrating baseline profiles into Android projects to achieve smoother and faster app experiences.

* [Jetpack Compose: Strong Skipping Mode Explained](https://medium.com/androiddevelopers/jetpack-compose-strong-skipping-mode-explained-cbdb2aa4b900): This article discusses how Compose uses strong skipping to optimize performance by avoiding unnecessary recompositions. It explains the role of stability in Compose, detailing how stable objects help reduce recompositions and enhance app efficiency. The article also covers best practices for achieving stability, such as using stable types and managing state effectively.

* [Jetpack Compose — When should I use derivedStateOf?](https://medium.com/androiddevelopers/jetpack-compose-when-should-i-use-derivedstateof-63ce7954c11b): The article explains the use of `derivedStateOf` in Jetpack Compose for optimizing performance by reducing unnecessary recompositions. It should be used when you have a derived state that depends on other state values, ensuring that recompositions occur only when these dependent states change. This approach helps maintain efficient and responsive UI updates by minimizing computational overhead.

* [Jetpack Compose Stability Explained](https://medium.com/androiddevelopers/jetpack-compose-stability-explained-79c10db270c8): The article "Jetpack Compose Stability Explained" delves into how Jetpack Compose manages the stability of UI elements to optimize performance. It explains the difference between stable and unstable objects and the use of `@Stable` annotation to reduce unnecessary recompositions. The article emphasizes the importance of ensuring stability in Compose applications to achieve efficient and responsive user interfaces. 

* [Why should you always test Compose performance in release?](https://medium.com/androiddevelopers/why-should-you-always-test-compose-performance-in-release-4168dd0f2c71): Testing Compose performance in release mode is essential because debug builds include additional checks and logging that can significantly slow down the app, leading to inaccurate performance assessments. Release builds, however, are optimized for speed and efficiency, providing a true reflection of how the app will perform in the real world. By testing in release mode, developers can identify and resolve performance issues that might otherwise be missed, ensuring a smoother user experience.

* [Mastering Jetpack Compose Performance With Examples: Part 1](https://www.getyourguide.careers/posts/mastering-jetpack-compose-performance-part-1): This article explains how to optimize performance in Jetpack Compose applications. It covers the importance of understanding state management, the distinction between restartable and skippable composables, and the phases of composition, layout, and drawing. The article also provides practical tips for tracking and minimizing unnecessary recompositions using tools like Layout Inspector.

* [Mastering Jetpack Compose Performance With Examples: Part 2](https://www.getyourguide.careers/posts/mastering-jetpack-compose-performance-part-2): This article provides insights into optimizing Jetpack Compose applications by addressing stability and recomposition issues. It discusses the use of the Compose Compiler Metrics Plugin to generate reports that help identify unstable classes and composables, and offers practical solutions like using stable annotations, immutable collections, and configuring a Compose Stability Config File. The article emphasizes the importance of understanding and managing stability to create efficient and performant Compose applications. 

## 🎤 Speaking

* [Jetpack Compose Mechanism](https://speakerdeck.com/skydoves/jetpack-compose-mechanism): This talk covers understanding Compose structures, Declarative UI, Composable functions, stability in Compose to improve Compose performance, and Kotlin Multiplatform.

## 💻 Open-Source Library

* [compose-stable-marker](https://github.com/skydoves/compose-stable-marker): ✒️ Compose stable markers were originated Compose runtime, which improves Compose performance by telling stable and skippable guarantees to the compose compiler from non-compose dependent modules. This library supports Kotlin Multiplatform.

* [compose-effects](https://github.com/skydoves/compose-effects): 🧵 Compose Effects enable you to launch efficient side-effects without unnecessary operations for Android and Kotlin Multiplatform.

* [compose-guard](https://github.com/j-roskopf/ComposeGuard): Compose Guard is a Gradle plugin for detecting regressions in Jetpack Compose / Compose Multiplatform code. It works by adding Gradle tasks to both generate golden stability metrics and verify that no new undesirable Compose Code was added. This plugin supports both Jetpack Compose and Compose Multiplatform.

<a href="https://www.android.skydoves.me/">
<img src="https://github.com/user-attachments/assets/e014ce01-3461-40af-bb2a-eb44f3f55f36" width="13%" align="right"/>
</a>

## 📘 Manifest Android Interview

[Manifest Android Interview](https://www.android.skydoves.me/) is a comprehensive guide designed to enhance your Android development expertise through 108 interview questions with detailed answers, 162 additional practical questions, and 50+ "Pro Tips for Mastery" sections. The interview questions primarily focus on Android development—including the Framework, UI, Jetpack Libraries, and Business Logic—as well as Jetpack Compose, covering Fundamentals, Runtime, and UI.

## Find this repository useful? :heart:
Support it by joining __[stargazers](https://github.com/skydoves/compose-performance/stargazers)__ for this repository. :star: <br>
Also, __[follow me](https://github.com/skydoves)__ on GitHub for my next creations! 🤩

# License
```xml
Designed and developed by 2024 skydoves (Jaewoong Eum)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
