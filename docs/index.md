---
author: rosanevallim
title: Windows Machine Learning
description: With Windows ML, you can use trained machine learning models in your Windows applications.
ms.author: rovalli
ms.date: 12/12/2018
ms.topic: article
keywords: windows 10, windows ai, windows ml, winml, windows machine learning
ms.localizationpriority: medium
ms.custom: RS5
---

# Windows Machine Learning

With Windows ML, you can integrate trained machine learning models in your Windows apps.

![Windows ML graphic](images/winml-graphic.png)

## Overview

:::row:::
    :::column:::
    Windows ML allows you to use trained machine learning models in your Windows apps (C#, C++, and JavaScript). The Windows ML inference engine evaluates trained models locally on Windows devices, removing concerns of connectivity, bandwidth, and data privacy. Hardware optimizations for CPU and GPU additionally enable high performance for quick evaluation results.

    For the latest Windows ML features and fixes, see our [release notes](release-notes.md).
    :::column-end:::
    :::column:::
        ![windows ml layers](images/overview-diagram.png)
    :::column-end:::
:::row-end:::

The following video gives a brief overview of Windows Machine Learning.

<br/>

> [!VIDEO https://www.youtube.com/embed/riGxT0Pd6IA]

## Develop

![windows ml developer flow](images/winml-flow.png)

To build apps with Windows ML, you'll:

1. [Get a trained ONNX model](get-onnx-model.md), or convert models trained in other ML frameworks into ONNX with [WinMLTools](convert-model-winmltools.md).
1. Add the ONNX model file to your app.
1. [Integrate the model](integrate-model.md) into your app's code.
1. Run on any Windows device!

To see Windows ML in action, you can try out the sample apps in the [Windows-Machine-Learning](https://github.com/Microsoft/Windows-Machine-Learning/tree/master) repo on Github. To learn more about using Windows ML, take a look through our documentation.

## Other machine learning solutions from Microsoft

Microsoft offers a variety of machine learning solutions to suit your needs. These solutions run in the cloud, on-premises, and locally on the device. See [What are the machine learning product options from Microsoft?](https://docs.microsoft.com/azure/machine-learning/service/overview-more-machine-learning) for more information.

[!INCLUDE [help](includes/get-help.md)]
