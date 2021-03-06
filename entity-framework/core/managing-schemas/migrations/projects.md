---
title: 移轉具有多個專案的 EF Core
author: bricelam
ms.author: bricelam
ms.date: 10/30/2017
ms.technology: entity-framework-core
ms.openlocfilehash: 3684e86cce0005056380d89604d038c734054d14
ms.sourcegitcommit: ced2637bf8cc5964c6daa6c7fcfce501bf9ef6e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/22/2017
ms.locfileid: "27161223"
---
<a name="using-a-separate-project"></a>使用個別的專案
========================
要儲存於一個包含不同的組件中的移轉您`DbContext`。 您也可以使用這項策略來維護多個集合的移轉，例如，一個用於開發，另一個版本的升級。

若要執行相關作業…

1. 建立新的類別庫。

2. 加入 DbContext 組件的參考。

3. 將移轉和模型的快照集檔案移至 類別庫中。
   * 如果您尚未加入任何，加入至 DbContext 專案，然後將它移。

4. 設定移轉組件：

   ``` csharp
   options.UseSqlServer(
       connectionString,
       x => x.MigrationsAssembly("MyApp.Migrations"));
   ```

5. 新增您移轉的組件中的啟動組件的參考。
   * 如果這導致循環相依性時，更新的類別庫的輸出路徑：

     ``` xml
     <PropertyGroup>
       <OutputPath>..\MyStarupProject\bin\$(Configuration)\</OutputPath>
     </PropertyGroup>
     ```

如果您所執行的所有項目正確，您應該能夠專案中加入新的移轉。

``` powershell
Add-Migration NewMigration -Project MyApp.Migrations
```
``` Console
dotnet ef migrations add NewMigration --project MyApp.Migrations
```
