---
title: "Microsoft SQL Server 資料庫提供者 - EF Core"
author: rowanmiller
ms.author: divega
ms.date: 10/27/2016
ms.assetid: 2e007c82-c6e4-45bb-8129-851b79ec1a0a
ms.technology: entity-framework-core
uid: core/providers/sql-server/index
ms.openlocfilehash: b2faf932e0484da4df0c1774afa7ba7ae2d077a5
ms.sourcegitcommit: 5e2d97e731f975cf3405ff3deab2a3c75ad1b969
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2017
---
# <a name="microsoft-sql-server-ef-core-database-provider"></a>Microsoft SQL Server EF Core 資料庫提供者

此資料庫提供者可讓 Entity Framework Core 與 Microsoft SQL Server (包括 SQL Azure) 搭配使用。 此提供者會作為 [EntityFramework GitHub 專案](https://github.com/aspnet/EntityFramework)的一部分進行維護。

## <a name="install"></a>Install

安裝 [Microsoft.EntityFrameworkCore.SqlServer NuGet 套件](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/)。

``` powershell
Install-Package Microsoft.EntityFrameworkCore.SqlServer
```

## <a name="get-started"></a>開始使用

下列資源將協助您開始使用此提供者。
* [.NET Framework 使用者入門 (主控台、WinForms、WPF 等等)](../../get-started/full-dotnet/index.md)

* [ASP.NET Core 使用者入門](../../get-started/aspnetcore/index.md)

* [UnicornStore 應用程式範例](https://github.com/rowanmiller/UnicornStore/tree/master/UnicornStore)

## <a name="supported-database-engines"></a>支援的資料庫引擎

* Microsoft SQL Server (2008 及更新版本)

## <a name="supported-platforms"></a>支援的平台

* .NET Framework (4.5.1 及更新版本)

* .NET Core

* Mono (4.2.0 及更新版本)

      Caution: Using this provider on Mono will make use of the Mono SQL Client implementation, which has a number of known issues. For example, it does not support secure connections (SSL).