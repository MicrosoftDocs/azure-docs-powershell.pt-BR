---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114302"
---
# <span data-ttu-id="c3042-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="c3042-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="c3042-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3042-102">SYNOPSIS</span></span>
<span data-ttu-id="c3042-103">Adiciona a fonte de dados de contador de desempenho do Windows para computadores conectados que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="c3042-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="c3042-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3042-104">SYNTAX</span></span>

### <span data-ttu-id="c3042-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3042-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3042-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c3042-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3042-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3042-107">DESCRIPTION</span></span>
<span data-ttu-id="c3042-108">O cmdlet **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** adiciona uma fonte de dados de contador de desempenho do Windows para computadores conectados que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="c3042-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="c3042-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3042-109">EXAMPLES</span></span>

## <span data-ttu-id="c3042-110">OS</span><span class="sxs-lookup"><span data-stu-id="c3042-110">PARAMETERS</span></span>

### <span data-ttu-id="c3042-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="c3042-111">-CounterName</span></span>
<span data-ttu-id="c3042-112">Especifica o nome de um contador.</span><span class="sxs-lookup"><span data-stu-id="c3042-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3042-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3042-113">-DefaultProfile</span></span>
<span data-ttu-id="c3042-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3042-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3042-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3042-115">-Force</span></span>
<span data-ttu-id="c3042-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3042-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3042-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c3042-117">-InstanceName</span></span>
<span data-ttu-id="c3042-118">Especifica um nome de instância.</span><span class="sxs-lookup"><span data-stu-id="c3042-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="c3042-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c3042-119">-IntervalSeconds</span></span>
<span data-ttu-id="c3042-120">Especifica o intervalo da coleção.</span><span class="sxs-lookup"><span data-stu-id="c3042-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="c3042-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3042-121">-Name</span></span>
<span data-ttu-id="c3042-122">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="c3042-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="c3042-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="c3042-123">-ObjectName</span></span>
<span data-ttu-id="c3042-124">Especifica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="c3042-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="c3042-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3042-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3042-126">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="c3042-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="c3042-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="c3042-127">-UseLegacyCollector</span></span>
<span data-ttu-id="c3042-128">Use o coletor herdado ou o coletor padrão.</span><span class="sxs-lookup"><span data-stu-id="c3042-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="c3042-129">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c3042-129">-Workspace</span></span>
<span data-ttu-id="c3042-130">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="c3042-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c3042-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3042-131">-WorkspaceName</span></span>
<span data-ttu-id="c3042-132">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="c3042-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c3042-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3042-133">-Confirm</span></span>
<span data-ttu-id="c3042-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3042-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3042-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3042-135">-WhatIf</span></span>
<span data-ttu-id="c3042-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3042-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3042-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3042-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3042-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3042-138">CommonParameters</span></span>
<span data-ttu-id="c3042-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3042-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3042-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3042-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3042-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3042-141">INPUTS</span></span>

### <span data-ttu-id="c3042-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c3042-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c3042-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c3042-143">System.String</span></span>

### <span data-ttu-id="c3042-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c3042-144">System.Int32</span></span>

## <span data-ttu-id="c3042-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3042-145">OUTPUTS</span></span>

### <span data-ttu-id="c3042-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c3042-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c3042-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3042-147">NOTES</span></span>

## <span data-ttu-id="c3042-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3042-148">RELATED LINKS</span></span>
