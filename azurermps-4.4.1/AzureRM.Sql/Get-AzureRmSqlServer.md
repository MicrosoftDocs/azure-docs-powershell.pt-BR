---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432995"
---
# <span data-ttu-id="b16a5-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b16a5-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="b16a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b16a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b16a5-103">Retorna informações sobre os servidores de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b16a5-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b16a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b16a5-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b16a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b16a5-105">DESCRIPTION</span></span>
<span data-ttu-id="b16a5-106">O cmdlet **Get-AzureRmSqlServer** retorna informações sobre um ou mais servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b16a5-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="b16a5-107">Especifique o nome de um servidor para ver informações somente para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="b16a5-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="b16a5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b16a5-108">EXAMPLES</span></span>

### <span data-ttu-id="b16a5-109">Exemplo 1: obter todas as instâncias do SQL Server atribuídas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b16a5-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b16a5-110">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure atribuídos à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b16a5-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b16a5-111">Exemplo 2: obter informações sobre um servidor de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b16a5-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b16a5-112">Esse comando obtém informações sobre o servidor do banco de dados SQL do Azure chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="b16a5-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="b16a5-113">Exemplo 3: obter todas as instâncias do SQL Server na assinatura</span><span class="sxs-lookup"><span data-stu-id="b16a5-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b16a5-114">Esse comando obtém informações sobre todos os servidores de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b16a5-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="b16a5-115">OS</span><span class="sxs-lookup"><span data-stu-id="b16a5-115">PARAMETERS</span></span>

### <span data-ttu-id="b16a5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16a5-116">-ResourceGroupName</span></span>
<span data-ttu-id="b16a5-117">Especifica o nome do grupo de recursos ao qual os servidores são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="b16a5-117">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="b16a5-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b16a5-118">-ServerName</span></span>
<span data-ttu-id="b16a5-119">Especifica o nome do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b16a5-119">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b16a5-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b16a5-120">-Confirm</span></span>
<span data-ttu-id="b16a5-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b16a5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b16a5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16a5-122">-WhatIf</span></span>
<span data-ttu-id="b16a5-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b16a5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16a5-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b16a5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b16a5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16a5-125">-DefaultProfile</span></span>
<span data-ttu-id="b16a5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b16a5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16a5-127">CommonParameters</span></span>
<span data-ttu-id="b16a5-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16a5-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b16a5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16a5-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b16a5-130">INPUTS</span></span>

## <span data-ttu-id="b16a5-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b16a5-131">OUTPUTS</span></span>

### <span data-ttu-id="b16a5-132">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b16a5-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b16a5-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b16a5-133">NOTES</span></span>

## <span data-ttu-id="b16a5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b16a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="b16a5-135">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b16a5-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="b16a5-136">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b16a5-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="b16a5-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b16a5-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="b16a5-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b16a5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


