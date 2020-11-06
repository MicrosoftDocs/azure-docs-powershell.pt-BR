---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 6372abc324601761c07ec4c69d52db188172ba0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599846"
---
# <span data-ttu-id="8a499-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="8a499-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="8a499-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a499-102">SYNOPSIS</span></span>
<span data-ttu-id="8a499-103">Adiciona contadores de desempenho a todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8a499-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="8a499-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a499-104">SYNTAX</span></span>

### <span data-ttu-id="8a499-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a499-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a499-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8a499-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a499-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a499-107">DESCRIPTION</span></span>
<span data-ttu-id="8a499-108">O cmdlet **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** adiciona contadores de desempenho dos quais o Azure Operational insights coleta dados para todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8a499-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="8a499-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a499-109">EXAMPLES</span></span>

## <span data-ttu-id="8a499-110">OS</span><span class="sxs-lookup"><span data-stu-id="8a499-110">PARAMETERS</span></span>

### <span data-ttu-id="8a499-111">-Nomes prenomeados</span><span class="sxs-lookup"><span data-stu-id="8a499-111">-CounterNames</span></span>
<span data-ttu-id="8a499-112">Especifica uma matriz de nomes de contadores.</span><span class="sxs-lookup"><span data-stu-id="8a499-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="8a499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a499-113">-DefaultProfile</span></span>
<span data-ttu-id="8a499-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8a499-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a499-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a499-115">-Force</span></span>
<span data-ttu-id="8a499-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8a499-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a499-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8a499-117">-InstanceName</span></span>
<span data-ttu-id="8a499-118">Especifica um nome de instância.</span><span class="sxs-lookup"><span data-stu-id="8a499-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="8a499-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8a499-119">-IntervalSeconds</span></span>
<span data-ttu-id="8a499-120">Especifica o intervalo da coleção.</span><span class="sxs-lookup"><span data-stu-id="8a499-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="8a499-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a499-121">-Name</span></span>
<span data-ttu-id="8a499-122">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8a499-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="8a499-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="8a499-123">-ObjectName</span></span>
<span data-ttu-id="8a499-124">Especifica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8a499-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="8a499-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a499-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a499-126">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="8a499-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="8a499-127">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8a499-127">-Workspace</span></span>
<span data-ttu-id="8a499-128">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8a499-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8a499-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a499-129">-WorkspaceName</span></span>
<span data-ttu-id="8a499-130">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8a499-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8a499-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a499-131">-Confirm</span></span>
<span data-ttu-id="8a499-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a499-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a499-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a499-133">-WhatIf</span></span>
<span data-ttu-id="8a499-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a499-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a499-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a499-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a499-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a499-136">CommonParameters</span></span>
<span data-ttu-id="8a499-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a499-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a499-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a499-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a499-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a499-139">INPUTS</span></span>

### <span data-ttu-id="8a499-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8a499-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8a499-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8a499-141">System.String</span></span>

### <span data-ttu-id="8a499-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="8a499-142">System.String[]</span></span>

### <span data-ttu-id="8a499-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8a499-143">System.Int32</span></span>

## <span data-ttu-id="8a499-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a499-144">OUTPUTS</span></span>

### <span data-ttu-id="8a499-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8a499-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8a499-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a499-146">NOTES</span></span>

## <span data-ttu-id="8a499-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a499-147">RELATED LINKS</span></span>

[<span data-ttu-id="8a499-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8a499-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="8a499-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8a499-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


