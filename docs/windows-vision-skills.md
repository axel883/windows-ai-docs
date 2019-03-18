---
author: eliotcowley
title: Windows Vision Skills
description: Learn about the Windows Vision Skills APIs.
ms.author: elcowle
ms.date: 3/18/2019
ms.topic: article
keywords: windows 10, windows ai, windows ml, winml, windows machine learning, windows vision skills
ms.localizationpriority: medium
---

# Windows Vision Skills

Implementing and integrating efficient AI and Computer Vision (CV) solutions is a hard task for developers. The industry is moving at a fast pace and the amount of custom-tailored solutions coming out makes it almost impossible for application developers to keep up easily.

The **Windows Vision Skills** framework is meant to standardize the way AI and CV are put to use within a WinRT (Windows Runtime) application running on the edge (a local device). It aims to abstract away the complexity of AI and CV techniques by simply defining the concept of *skills*, modular pieces of code that process input and produce output. 

The implementation that contains the complex details is encapsulated by an extensible WinRT API that inherits the base classes and interfaces in the [Microsoft.AI.Skills.SkillInterfacePreview](TODO) namespace. This API leverages built-in Windows primitives, which in turn eases interop with built-in or external third-party acceleration frameworks. 

While this preview focuses on vision-oriented scenarios and primitives, this API is meant to accomodate any kind of input and output variable and a wide range of scenarios (vision, audio, text, and more).

The **Microsoft.AI.Skills.SkillInterfacePreview** namespace provides a set of base interfaces to be extended by all skills as well as classes and helper methods for skill implementers on Windows.

* [Get the NuGet package](TODO)

* [View samples on GitHub](https://github.com/Microsoft/WindowsVisionSkillsPreview)

* [Read the documentation](TODO)

### Important concepts

This API is meant to streamline the way skills work and how developers interact with them. Each skill implements the following interfaces:

1. [ISkillDescriptor](TODO): Provides information on the skill and exposes its requirements (input, output, version, and so on).

2. [ISkillBinding](TODO): Serves as a dictionary and a conduit for input and output variables to be passed back and forth to the [ISkill](TODO). It handles pre- and post-processing of the input/output data and simplifies their access.

3. [ISkill](TODO): Exposes the core logic of processing input and forming output via an **ISkillBinding**.

Skills are meant to optimally leverage the hardware capabilities (CPU, GPU, etc.) on each system they run on. Therefore, skills have to expose the set of [ISkillExecutionDevice](TODO)s currently available and filter them into a list of compatible devices. This way, a developer consuming the skill can best chose how to tap into supported hardware resources at runtime on a user's system. 

In order to ensure that input and output variables are passed in the correct format to the skill, the interface defines [ISkillFeature](TODO), which is meant to encapsulate a value in a predefined format. This value is represented by an [ISkillFeatureValue](TODO), for which multiple common derived interfaces are defined (tensor, image, string, etc.). For these derivatives, automatic conversion to the appropriate format occurs when attempting to set a value that does not match the predefined format (i.e. when binding an image in a different format than the one required).
