---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112118"
---
# <span data-ttu-id="8c7a6-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8c7a6-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="8c7a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7a6-103">Retorna informações sobre os servidores de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="8c7a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c7a6-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c7a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7a6-106">O cmdlet **Get-AzSqlServer** retorna informações sobre um ou mais servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="8c7a6-107">Especifique o nome de um servidor para ver informações somente para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="8c7a6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c7a6-108">EXAMPLES</span></span>

### <span data-ttu-id="8c7a6-109">Exemplo 1: obter todas as instâncias do SQL Server atribuídas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8c7a6-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="8c7a6-110">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure atribuídos à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8c7a6-111">Exemplo 2: obter informações sobre um servidor de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="8c7a6-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="8c7a6-112">Esse comando obtém informações sobre o servidor do banco de dados SQL do Azure chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="8c7a6-113">Exemplo 3: obter todas as instâncias do SQL Server na assinatura</span><span class="sxs-lookup"><span data-stu-id="8c7a6-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="8c7a6-114">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="8c7a6-115">Exemplo 4: obter todas as instâncias do SQL Server atribuídas a um grupo de recursos usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="8c7a6-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="8c7a6-116">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure atribuídos ao grupo de recursos ResourceGroup01 que começam com "servidor".</span><span class="sxs-lookup"><span data-stu-id="8c7a6-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="8c7a6-117">OS</span><span class="sxs-lookup"><span data-stu-id="8c7a6-117">PARAMETERS</span></span>

### <span data-ttu-id="8c7a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7a6-118">-DefaultProfile</span></span>
<span data-ttu-id="8c7a6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8c7a6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c7a6-121">Especifica o nome do grupo de recursos ao qual os servidores são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7a6-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8c7a6-122">-ServerName</span></span>
<span data-ttu-id="8c7a6-123">Especifica o nome do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7a6-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c7a6-124">-Confirm</span></span>
<span data-ttu-id="8c7a6-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7a6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c7a6-126">-WhatIf</span></span>
<span data-ttu-id="8c7a6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c7a6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7a6-129">CommonParameters</span></span>
<span data-ttu-id="8c7a6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7a6-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c7a6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7a6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c7a6-132">INPUTS</span></span>

### <span data-ttu-id="8c7a6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7a6-133">System.String</span></span>

## <span data-ttu-id="8c7a6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c7a6-134">OUTPUTS</span></span>

### <span data-ttu-id="8c7a6-135">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8c7a6-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="8c7a6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c7a6-136">NOTES</span></span>

## <span data-ttu-id="8c7a6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c7a6-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c7a6-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8c7a6-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="8c7a6-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8c7a6-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="8c7a6-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8c7a6-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="8c7a6-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8c7a6-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


