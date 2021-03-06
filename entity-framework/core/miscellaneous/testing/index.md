---
title: 使用 Entity Framework 來測試元件 - EF Core
author: rowanmiller
ms.author: divega
ms.date: 10/27/2016
ms.assetid: 1603be0c-69bc-4dd9-9a08-3d0129cdc6c1
ms.technology: entity-framework-core
uid: core/miscellaneous/testing/index
ms.openlocfilehash: c82c25da393c39cf5e2deb46c7322e7395051937
ms.sourcegitcommit: 01a75cd483c1943ddd6f82af971f07abde20912e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2017
ms.locfileid: "26048860"
---
# <a name="testing"></a>測試

您可能會想要使用近似連線至實際資料庫，而不實際進行資料庫 I/O 作業的方式來測試元件。

有兩種主要的方式可以這麼做：
 * [SQLite 記憶體內部模式](sqlite.md) 可讓您對行為類似關聯式資料庫的提供者寫入有效率的測試。
 * [InMemory 提供者](in-memory.md) 是相依性最低的輕量型提供者，但行為不一定永遠都如同關聯式資料庫。
