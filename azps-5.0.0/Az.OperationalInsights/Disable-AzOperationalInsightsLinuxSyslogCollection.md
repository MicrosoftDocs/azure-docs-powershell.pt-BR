---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284218"
---
# <span data-ttu-id="acebb-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="acebb-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="acebb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acebb-102">SYNOPSIS</span></span>
<span data-ttu-id="acebb-103">Interrompe a coleta de dados de syslog de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="acebb-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="acebb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acebb-104">SYNTAX</span></span>

### <span data-ttu-id="acebb-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="acebb-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acebb-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="acebb-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acebb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acebb-107">DESCRIPTION</span></span>
<span data-ttu-id="acebb-108">O cmdlet **Disable-AzOperationalInsightsLinuxSyslogCollection** interrompe a coleta de dados de syslog de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="acebb-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="acebb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acebb-109">EXAMPLES</span></span>

## <span data-ttu-id="acebb-110">OS</span><span class="sxs-lookup"><span data-stu-id="acebb-110">PARAMETERS</span></span>

### <span data-ttu-id="acebb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acebb-111">-DefaultProfile</span></span>
<span data-ttu-id="acebb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="acebb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acebb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acebb-113">-ResourceGroupName</span></span>
<span data-ttu-id="acebb-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="acebb-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="acebb-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="acebb-115">-Workspace</span></span>
<span data-ttu-id="acebb-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="acebb-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="acebb-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="acebb-117">-WorkspaceName</span></span>
<span data-ttu-id="acebb-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="acebb-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="acebb-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="acebb-119">-Confirm</span></span>
<span data-ttu-id="acebb-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acebb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acebb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acebb-121">-WhatIf</span></span>
<span data-ttu-id="acebb-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="acebb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acebb-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acebb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acebb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acebb-124">CommonParameters</span></span>
<span data-ttu-id="acebb-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acebb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acebb-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acebb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acebb-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acebb-127">INPUTS</span></span>

### <span data-ttu-id="acebb-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="acebb-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="acebb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="acebb-129">System.String</span></span>

## <span data-ttu-id="acebb-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acebb-130">OUTPUTS</span></span>

### <span data-ttu-id="acebb-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="acebb-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="acebb-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acebb-132">NOTES</span></span>
* <span data-ttu-id="acebb-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="acebb-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="acebb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acebb-134">RELATED LINKS</span></span>

[<span data-ttu-id="acebb-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="acebb-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="acebb-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="acebb-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


