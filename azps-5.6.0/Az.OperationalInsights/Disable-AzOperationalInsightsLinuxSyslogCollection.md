---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 7593ad23952b9920fdd7e7fa9d75e22e9fe65059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891322"
---
# <span data-ttu-id="3ca0d-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="3ca0d-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="3ca0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca0d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca0d-103">Interrompe a coleta de dados de syslog de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="3ca0d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ca0d-104">SYNTAX</span></span>

### <span data-ttu-id="3ca0d-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ca0d-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3ca0d-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca0d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ca0d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ca0d-108">O cmdlet **Disable-AzOperationalInsightsLinuxSyslogCollection** interrompe a coleção de dados de syslog de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="3ca0d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ca0d-109">EXAMPLES</span></span>

## <span data-ttu-id="3ca0d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ca0d-110">PARAMETERS</span></span>

### <span data-ttu-id="3ca0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-111">-DefaultProfile</span></span>
<span data-ttu-id="3ca0d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3ca0d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ca0d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca0d-113">-ResourceGroupName</span></span>
<span data-ttu-id="3ca0d-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="3ca0d-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="3ca0d-115">-Workspace</span></span>
<span data-ttu-id="3ca0d-116">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ca0d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ca0d-117">-WorkspaceName</span></span>
<span data-ttu-id="3ca0d-118">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ca0d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ca0d-119">-Confirm</span></span>
<span data-ttu-id="3ca0d-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca0d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca0d-121">-WhatIf</span></span>
<span data-ttu-id="3ca0d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca0d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca0d-124">CommonParameters</span></span>
<span data-ttu-id="3ca0d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca0d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca0d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca0d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ca0d-127">INPUTS</span></span>

### <span data-ttu-id="3ca0d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ca0d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3ca0d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3ca0d-129">System.String</span></span>

## <span data-ttu-id="3ca0d-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ca0d-130">OUTPUTS</span></span>

### <span data-ttu-id="3ca0d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3ca0d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3ca0d-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ca0d-132">NOTES</span></span>
* <span data-ttu-id="3ca0d-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="3ca0d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3ca0d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ca0d-134">RELATED LINKS</span></span>

[<span data-ttu-id="3ca0d-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="3ca0d-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="3ca0d-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="3ca0d-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


