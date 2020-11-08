---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125365"
---
# <span data-ttu-id="deefe-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="deefe-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="deefe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deefe-102">SYNOPSIS</span></span>
<span data-ttu-id="deefe-103">Obtém objetivos de serviço para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="deefe-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="deefe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deefe-104">SYNTAX</span></span>

### <span data-ttu-id="deefe-105">ByLocation (padrão)</span><span class="sxs-lookup"><span data-stu-id="deefe-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deefe-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="deefe-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deefe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deefe-107">DESCRIPTION</span></span>
<span data-ttu-id="deefe-108">O cmdlet **Get-AzSqlServerServiceObjective** Obtém os objetivos de serviço disponíveis para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="deefe-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="deefe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deefe-109">EXAMPLES</span></span>

### <span data-ttu-id="deefe-110">Exemplo 1: obter objetivos de serviço</span><span class="sxs-lookup"><span data-stu-id="deefe-110">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="deefe-111">Esse comando obtém os objetivos de serviço do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="deefe-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="deefe-112">Exemplo 2: obter objetivos de serviço usando filtragem</span><span class="sxs-lookup"><span data-stu-id="deefe-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="deefe-113">Esse comando obtém os objetivos de serviço do servidor chamado Server01 que começam com "System".</span><span class="sxs-lookup"><span data-stu-id="deefe-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="deefe-114">Exemplo 3: obter os objetivos de serviço para um local</span><span class="sxs-lookup"><span data-stu-id="deefe-114">Example 3: Get service objectives for a location</span></span>
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

<span data-ttu-id="deefe-115">Esse comando obtém os objetivos do serviço para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="deefe-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="deefe-116">OS</span><span class="sxs-lookup"><span data-stu-id="deefe-116">PARAMETERS</span></span>

### <span data-ttu-id="deefe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deefe-117">-DefaultProfile</span></span>
<span data-ttu-id="deefe-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="deefe-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deefe-119">-Local</span><span class="sxs-lookup"><span data-stu-id="deefe-119">-Location</span></span>
<span data-ttu-id="deefe-120">O nome do local para o qual obter os objetivos do serviço.</span><span class="sxs-lookup"><span data-stu-id="deefe-120">The name of the Location for which to get the service objectives.</span></span>

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

### <span data-ttu-id="deefe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deefe-121">-ResourceGroupName</span></span>
<span data-ttu-id="deefe-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="deefe-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="deefe-123">Este cmdlet obtém objetivos de serviço para um servidor de banco de dados SQL atribuído a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="deefe-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="deefe-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="deefe-124">-ServerName</span></span>
<span data-ttu-id="deefe-125">Especifica o nome de um servidor de banco de dados SQL do SQL Database.</span><span class="sxs-lookup"><span data-stu-id="deefe-125">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="deefe-126">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="deefe-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="deefe-127">Especifica o nome de um objetivo de serviço para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="deefe-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="deefe-128">Os valores aceitáveis para esse parâmetro são: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="deefe-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="deefe-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="deefe-129">-Confirm</span></span>
<span data-ttu-id="deefe-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deefe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deefe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deefe-131">-WhatIf</span></span>
<span data-ttu-id="deefe-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="deefe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deefe-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="deefe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deefe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deefe-134">CommonParameters</span></span>
<span data-ttu-id="deefe-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deefe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deefe-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deefe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deefe-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deefe-137">INPUTS</span></span>

### <span data-ttu-id="deefe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="deefe-138">System.String</span></span>

## <span data-ttu-id="deefe-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deefe-139">OUTPUTS</span></span>

### <span data-ttu-id="deefe-140">Microsoft. Azure. Commands. Sql. userobjectal. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="deefe-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="deefe-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deefe-141">NOTES</span></span>

## <span data-ttu-id="deefe-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deefe-142">RELATED LINKS</span></span>

[<span data-ttu-id="deefe-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="deefe-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


