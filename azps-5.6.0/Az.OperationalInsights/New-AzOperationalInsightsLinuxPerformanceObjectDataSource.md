---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 7a6914d6259cafaedff68b28e8691311245ef6f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890226"
---
# <span data-ttu-id="f1a1c-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="f1a1c-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="f1a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a1c-103">Adiciona contadores de desempenho a todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="f1a1c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f1a1c-104">SYNTAX</span></span>

### <span data-ttu-id="f1a1c-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1a1c-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a1c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f1a1c-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a1c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f1a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="f1a1c-108">O cmdlet **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** adiciona contadores de desempenho dos quais o Insights Operacionais do Azure coleta dados para todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="f1a1c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-109">EXAMPLES</span></span>

## <span data-ttu-id="f1a1c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="f1a1c-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="f1a1c-111">-CounterNames</span></span>
<span data-ttu-id="f1a1c-112">Especifica uma matriz de nomes de contadores.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="f1a1c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f1a1c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1a1c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1a1c-115">-Force</span></span>
<span data-ttu-id="f1a1c-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f1a1c-117">-InstanceName</span></span>
<span data-ttu-id="f1a1c-118">Especifica um nome de instância.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f1a1c-119">-IntervalSeconds</span></span>
<span data-ttu-id="f1a1c-120">Especifica o intervalo de coleção.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1a1c-121">-Name</span></span>
<span data-ttu-id="f1a1c-122">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-122">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="f1a1c-123">-ObjectName</span></span>
<span data-ttu-id="f1a1c-124">Especifica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-124">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f1a1c-126">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-126">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-127">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f1a1c-127">-Workspace</span></span>
<span data-ttu-id="f1a1c-128">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1a1c-129">-WorkspaceName</span></span>
<span data-ttu-id="f1a1c-130">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1a1c-131">-Confirm</span></span>
<span data-ttu-id="f1a1c-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a1c-133">-WhatIf</span></span>
<span data-ttu-id="f1a1c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a1c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a1c-136">CommonParameters</span></span>
<span data-ttu-id="f1a1c-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a1c-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a1c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a1c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-139">INPUTS</span></span>

### <span data-ttu-id="f1a1c-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1a1c-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f1a1c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a1c-141">System.String</span></span>

### <span data-ttu-id="f1a1c-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f1a1c-142">System.String[]</span></span>

### <span data-ttu-id="f1a1c-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f1a1c-143">System.Int32</span></span>

## <span data-ttu-id="f1a1c-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-144">OUTPUTS</span></span>

### <span data-ttu-id="f1a1c-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f1a1c-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f1a1c-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="f1a1c-146">NOTES</span></span>

## <span data-ttu-id="f1a1c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-147">RELATED LINKS</span></span>

[<span data-ttu-id="f1a1c-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f1a1c-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="f1a1c-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f1a1c-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


