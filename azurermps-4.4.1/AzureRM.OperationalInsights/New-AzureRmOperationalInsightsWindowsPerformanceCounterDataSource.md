---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: dfdea6498ac7f553dafeea186a8b60f157cbd904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602428"
---
# <span data-ttu-id="936a9-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="936a9-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="936a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="936a9-102">SYNOPSIS</span></span>
<span data-ttu-id="936a9-103">Adiciona a fonte de dados de contador de desempenho do Windows para computadores conectados que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="936a9-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="936a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="936a9-104">SYNTAX</span></span>

### <span data-ttu-id="936a9-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="936a9-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="936a9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="936a9-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="936a9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="936a9-107">DESCRIPTION</span></span>
<span data-ttu-id="936a9-108">O cmdlet **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** adiciona uma fonte de dados de contador de desempenho do Windows para computadores conectados que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="936a9-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="936a9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="936a9-109">EXAMPLES</span></span>

## <span data-ttu-id="936a9-110">OS</span><span class="sxs-lookup"><span data-stu-id="936a9-110">PARAMETERS</span></span>

### <span data-ttu-id="936a9-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="936a9-111">-CounterName</span></span>
<span data-ttu-id="936a9-112">Especifica o nome de um contador.</span><span class="sxs-lookup"><span data-stu-id="936a9-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="936a9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="936a9-113">-Force</span></span>
<span data-ttu-id="936a9-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="936a9-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="936a9-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="936a9-115">-InstanceName</span></span>
<span data-ttu-id="936a9-116">Especifica um nome de instância.</span><span class="sxs-lookup"><span data-stu-id="936a9-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="936a9-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="936a9-117">-IntervalSeconds</span></span>
<span data-ttu-id="936a9-118">Especifica o intervalo da coleção.</span><span class="sxs-lookup"><span data-stu-id="936a9-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="936a9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="936a9-119">-Name</span></span>
<span data-ttu-id="936a9-120">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="936a9-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="936a9-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="936a9-121">-ObjectName</span></span>
<span data-ttu-id="936a9-122">Especifica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="936a9-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="936a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="936a9-124">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="936a9-124">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="936a9-125">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="936a9-125">-UseLegacyCollector</span></span>
<span data-ttu-id="936a9-126">Use o coletor herdado ou o coletor padrão.</span><span class="sxs-lookup"><span data-stu-id="936a9-126">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="936a9-127">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="936a9-127">-Workspace</span></span>
<span data-ttu-id="936a9-128">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="936a9-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="936a9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="936a9-129">-WorkspaceName</span></span>
<span data-ttu-id="936a9-130">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="936a9-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="936a9-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="936a9-131">-Confirm</span></span>
<span data-ttu-id="936a9-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="936a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="936a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="936a9-133">-WhatIf</span></span>
<span data-ttu-id="936a9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="936a9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="936a9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="936a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="936a9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936a9-136">-DefaultProfile</span></span>
<span data-ttu-id="936a9-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="936a9-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="936a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936a9-138">CommonParameters</span></span>
<span data-ttu-id="936a9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936a9-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936a9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="936a9-141">INPUTS</span></span>

### <span data-ttu-id="936a9-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="936a9-142">PSWorkspace</span></span>
<span data-ttu-id="936a9-143">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="936a9-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="936a9-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="936a9-144">OUTPUTS</span></span>

### <span data-ttu-id="936a9-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="936a9-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="936a9-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="936a9-146">NOTES</span></span>

## <span data-ttu-id="936a9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="936a9-147">RELATED LINKS</span></span>

