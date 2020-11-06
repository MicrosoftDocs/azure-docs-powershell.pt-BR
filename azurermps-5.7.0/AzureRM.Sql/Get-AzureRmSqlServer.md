---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432885"
---
# <span data-ttu-id="51f18-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="51f18-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="51f18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51f18-102">SYNOPSIS</span></span>
<span data-ttu-id="51f18-103">Retorna informações sobre os servidores de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="51f18-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51f18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51f18-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f18-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51f18-105">DESCRIPTION</span></span>
<span data-ttu-id="51f18-106">O cmdlet **Get-AzureRmSqlServer** retorna informações sobre um ou mais servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="51f18-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="51f18-107">Especifique o nome de um servidor para ver informações somente para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="51f18-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="51f18-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51f18-108">EXAMPLES</span></span>

### <span data-ttu-id="51f18-109">Exemplo 1: obter todas as instâncias do SQL Server atribuídas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="51f18-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="51f18-110">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure atribuídos à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51f18-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="51f18-111">Exemplo 2: obter informações sobre um servidor de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="51f18-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="51f18-112">Esse comando obtém informações sobre o servidor do banco de dados SQL do Azure chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="51f18-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="51f18-113">Exemplo 3: obter todas as instâncias do SQL Server na assinatura</span><span class="sxs-lookup"><span data-stu-id="51f18-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
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

<span data-ttu-id="51f18-114">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="51f18-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="51f18-115">OS</span><span class="sxs-lookup"><span data-stu-id="51f18-115">PARAMETERS</span></span>

### <span data-ttu-id="51f18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f18-116">-DefaultProfile</span></span>
<span data-ttu-id="51f18-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="51f18-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f18-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f18-118">-ResourceGroupName</span></span>
<span data-ttu-id="51f18-119">Especifica o nome do grupo de recursos ao qual os servidores são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="51f18-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f18-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="51f18-120">-ServerName</span></span>
<span data-ttu-id="51f18-121">Especifica o nome do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="51f18-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f18-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51f18-122">-Confirm</span></span>
<span data-ttu-id="51f18-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f18-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f18-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f18-124">-WhatIf</span></span>
<span data-ttu-id="51f18-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51f18-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51f18-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51f18-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f18-127">CommonParameters</span></span>
<span data-ttu-id="51f18-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f18-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f18-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f18-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51f18-130">INPUTS</span></span>

### <span data-ttu-id="51f18-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51f18-131">None</span></span>
<span data-ttu-id="51f18-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="51f18-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51f18-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51f18-133">OUTPUTS</span></span>

### <span data-ttu-id="51f18-134">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="51f18-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="51f18-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51f18-135">NOTES</span></span>

## <span data-ttu-id="51f18-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51f18-136">RELATED LINKS</span></span>

[<span data-ttu-id="51f18-137">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="51f18-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="51f18-138">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="51f18-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="51f18-139">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="51f18-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="51f18-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="51f18-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


