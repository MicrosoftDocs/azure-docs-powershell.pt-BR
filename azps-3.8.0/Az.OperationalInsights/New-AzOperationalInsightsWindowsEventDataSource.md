---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944503"
---
# <span data-ttu-id="8fd4a-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8fd4a-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="8fd4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd4a-103">Coleta logs de eventos de computadores que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="8fd4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fd4a-104">SYNTAX</span></span>

### <span data-ttu-id="8fd4a-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8fd4a-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd4a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8fd4a-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd4a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fd4a-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd4a-108">O cmdlet **New-AzOperationalInsightsWindowsEventDataSource** adiciona uma fonte de dados que coleta logs de eventos do Windows de computadores conectados que executam o sistema operacional Windows em insights operacionais do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="8fd4a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fd4a-109">EXAMPLES</span></span>

### <span data-ttu-id="8fd4a-110">Exemplo 1: criar fonte de dados de evento do sistema Windows</span><span class="sxs-lookup"><span data-stu-id="8fd4a-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="8fd4a-111">OS</span><span class="sxs-lookup"><span data-stu-id="8fd4a-111">PARAMETERS</span></span>

### <span data-ttu-id="8fd4a-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="8fd4a-112">-CollectErrors</span></span>
<span data-ttu-id="8fd4a-113">Indica que as insights operacionais coletam mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="8fd4a-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="8fd4a-114">-CollectInformation</span></span>
<span data-ttu-id="8fd4a-115">Indica que as insights operacionais coletam mensagens de informações.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="8fd4a-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="8fd4a-116">-CollectWarnings</span></span>
<span data-ttu-id="8fd4a-117">Indica que as insights operacionais coletam mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="8fd4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd4a-118">-DefaultProfile</span></span>
<span data-ttu-id="8fd4a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8fd4a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fd4a-120">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="8fd4a-120">-EventLogName</span></span>
<span data-ttu-id="8fd4a-121">Especifica o nome do log de eventos.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="8fd4a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8fd4a-122">-Force</span></span>
<span data-ttu-id="8fd4a-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fd4a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fd4a-124">-Name</span></span>
<span data-ttu-id="8fd4a-125">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-125">Specifies a name for the data source.</span></span> <span data-ttu-id="8fd4a-126">O nome não é exposto no portal do Azure e qualquer cadeia de caracteres pode ser usada desde que seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="8fd4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="8fd4a-128">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="8fd4a-129">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8fd4a-129">-Workspace</span></span>
<span data-ttu-id="8fd4a-130">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8fd4a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8fd4a-131">-WorkspaceName</span></span>
<span data-ttu-id="8fd4a-132">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8fd4a-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8fd4a-133">-Confirm</span></span>
<span data-ttu-id="8fd4a-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd4a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd4a-135">-WhatIf</span></span>
<span data-ttu-id="8fd4a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd4a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd4a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd4a-138">CommonParameters</span></span>
<span data-ttu-id="8fd4a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd4a-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd4a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd4a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fd4a-141">INPUTS</span></span>

### <span data-ttu-id="8fd4a-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8fd4a-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8fd4a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd4a-143">System.String</span></span>

## <span data-ttu-id="8fd4a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fd4a-144">OUTPUTS</span></span>

### <span data-ttu-id="8fd4a-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8fd4a-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8fd4a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fd4a-146">NOTES</span></span>

## <span data-ttu-id="8fd4a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fd4a-147">RELATED LINKS</span></span>
