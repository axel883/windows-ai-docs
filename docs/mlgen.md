---
author: rosanevallim
title: Automatic code generation with mlgen
description: Windows ML's code generator mlgen creates an interface (C#, C++/WinRT, and C++/CX) that allows you to easily load, bind, and evaluate a model in your app.
ms.author: rovalli
ms.date: 2/12/2019
ms.topic: article
keywords: windows 10, windows ai, windows ml, winml, windows machine learning
ms.localizationpriority: medium
---

# Automatic code generation with mlgen

<br/>

> [!VIDEO https://www.youtube.com/embed/8MCDSlm326U]

<br/>

Windows Machine Learning's code generator **mlgen** creates an interface (C#, [C++/WinRT](https://docs.microsoft.com/windows/uwp/cpp-and-winrt-apis/), and C++/CX) with wrapper classes that call the [Windows ML API](https://docs.microsoft.com/uwp/api/windows.ai.machinelearning) for you, allowing you to easily load, bind, and evaluate a model in your project.

**mlgen** is provided as a [Visual Studio](https://visualstudio.microsoft.com/downloads/) extension for developers creating WinML applications in VS 2017 or later.

In Windows 10, version 1903 and later, **mlgen** is no longer included in the Windows 10 SDK, so you must download and install the extension. There is one for [Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=WinML.mlgen) and one for [Visual Studio 2019](https://marketplace.visualstudio.com/items?itemName=WinML.mlgenv2).

Once you have **mlgen** installed, inside your Visual Studio project, add your ONNX file to your project’s **Assets** folder, and VS will generate Windows ML wrapper classes in a new interface file. You can use these classes and methods to integrate your model into your application. See [Tutorial: Create a Windows Machine Learning UWP application (C#)](get-started-uwp.md) for a tutorial that integrates a model using this method.

[!INCLUDE [help](includes/get-help.md)]
