---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 13ce7a2410f8231d4c5194fbd57d41074d0ca892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427153"
---
# <span data-ttu-id="d8cc6-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="d8cc6-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="d8cc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cc6-103">Obtém objetivos de serviço para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8cc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8cc6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8cc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cc6-106">O cmdlet **Get-AzureRmSqlServerServiceObjective** Obtém os objetivos de serviço disponíveis para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="d8cc6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="d8cc6-108">Exemplo 1: obter objetivos de serviço</span><span class="sxs-lookup"><span data-stu-id="d8cc6-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="d8cc6-109">Esse comando obtém os objetivos de serviço do servidor chamado Server01 e o banco de dados chamado Database01.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="d8cc6-110">OS</span><span class="sxs-lookup"><span data-stu-id="d8cc6-110">PARAMETERS</span></span>

### <span data-ttu-id="d8cc6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8cc6-111">-DatabaseName</span></span>
<span data-ttu-id="d8cc6-112">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-112">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cc6-113">-DefaultProfile</span></span>
<span data-ttu-id="d8cc6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d8cc6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8cc6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cc6-115">-ResourceGroupName</span></span>
<span data-ttu-id="d8cc6-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8cc6-117">Este cmdlet obtém objetivos de serviço para um servidor de banco de dados SQL atribuído a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cc6-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d8cc6-118">-ServerName</span></span>
<span data-ttu-id="d8cc6-119">Especifica o nome de um servidor de banco de dados SQL do SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-119">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cc6-120">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="d8cc6-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="d8cc6-121">Especifica o nome de um objetivo de serviço para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="d8cc6-122">Os valores aceitáveis para esse parâmetro são: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cc6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8cc6-123">-Confirm</span></span>
<span data-ttu-id="d8cc6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8cc6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8cc6-125">-WhatIf</span></span>
<span data-ttu-id="d8cc6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8cc6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8cc6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cc6-128">CommonParameters</span></span>
<span data-ttu-id="d8cc6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cc6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cc6-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cc6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cc6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8cc6-131">INPUTS</span></span>

### <span data-ttu-id="d8cc6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8cc6-132">System.String</span></span>

## <span data-ttu-id="d8cc6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8cc6-133">OUTPUTS</span></span>

### <span data-ttu-id="d8cc6-134">Microsoft. Azure. Commands. Sql. userobjectal. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="d8cc6-134">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="d8cc6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8cc6-135">NOTES</span></span>

## <span data-ttu-id="d8cc6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8cc6-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8cc6-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d8cc6-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


