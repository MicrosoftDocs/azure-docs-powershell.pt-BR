---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: 031b20aa24c66817d199be5d12049d52222d23b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887608"
---
# <span data-ttu-id="381d6-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="381d6-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="381d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="381d6-102">SYNOPSIS</span></span>
<span data-ttu-id="381d6-103">Obtém objetivos de serviço para um servidor de banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="381d6-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="381d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="381d6-104">SYNTAX</span></span>

### <span data-ttu-id="381d6-105">ByLocation (Padrão)</span><span class="sxs-lookup"><span data-stu-id="381d6-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381d6-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="381d6-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381d6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="381d6-107">DESCRIPTION</span></span>
<span data-ttu-id="381d6-108">O cmdlet **Get-AzSqlServerServiceObjective** obtém os objetivos de serviço disponíveis para um servidor de banco de dados do Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="381d6-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="381d6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="381d6-109">EXAMPLES</span></span>

### <span data-ttu-id="381d6-110">Exemplo 1: Obter objetivos de serviço</span><span class="sxs-lookup"><span data-stu-id="381d6-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="381d6-111">Este comando obtém os objetivos de serviço para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="381d6-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="381d6-112">Exemplo 2: Obter objetivos de serviço usando filtragem</span><span class="sxs-lookup"><span data-stu-id="381d6-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="381d6-113">Este comando obtém os objetivos de serviço do servidor chamado Server01 que começam com "System".</span><span class="sxs-lookup"><span data-stu-id="381d6-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="381d6-114">Exemplo 3: Obter objetivos de serviço para um local</span><span class="sxs-lookup"><span data-stu-id="381d6-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="381d6-115">Este comando obtém os objetivos de serviço de uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="381d6-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="381d6-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="381d6-116">PARAMETERS</span></span>

### <span data-ttu-id="381d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381d6-117">-DefaultProfile</span></span>
<span data-ttu-id="381d6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="381d6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="381d6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="381d6-119">-Location</span></span>
<span data-ttu-id="381d6-120">O nome do Local para o qual obter os objetivos do serviço.</span><span class="sxs-lookup"><span data-stu-id="381d6-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="381d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="381d6-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="381d6-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="381d6-123">Este cmdlet obtém objetivos de serviço para um servidor de banco de dados SQL atribuído a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="381d6-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381d6-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="381d6-124">-ServerName</span></span>
<span data-ttu-id="381d6-125">Especifica o nome de um servidor SQL Banco de Dados SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="381d6-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381d6-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="381d6-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="381d6-127">Especifica o nome de um objetivo de serviço para um servidor de banco de dados do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="381d6-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="381d6-128">Os valores aceitáveis para este parâmetro são: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="381d6-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="381d6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="381d6-129">-Confirm</span></span>
<span data-ttu-id="381d6-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="381d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381d6-131">-WhatIf</span></span>
<span data-ttu-id="381d6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="381d6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="381d6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="381d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="381d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381d6-134">CommonParameters</span></span>
<span data-ttu-id="381d6-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381d6-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="381d6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381d6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="381d6-137">INPUTS</span></span>

### <span data-ttu-id="381d6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="381d6-138">System.String</span></span>

## <span data-ttu-id="381d6-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="381d6-139">OUTPUTS</span></span>

### <span data-ttu-id="381d6-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="381d6-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="381d6-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="381d6-141">NOTES</span></span>

## <span data-ttu-id="381d6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="381d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="381d6-143">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="381d6-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


