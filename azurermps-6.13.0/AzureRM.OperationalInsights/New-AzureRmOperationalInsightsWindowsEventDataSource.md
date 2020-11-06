---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5f3200459cbcca9806a1a7185798889b3457760d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431317"
---
# <span data-ttu-id="3a15e-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="3a15e-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="3a15e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a15e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a15e-103">Coleta logs de eventos de computadores que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="3a15e-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a15e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a15e-104">SYNTAX</span></span>

### <span data-ttu-id="3a15e-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a15e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a15e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a15e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a15e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a15e-107">DESCRIPTION</span></span>
<span data-ttu-id="3a15e-108">O cmdlet **New-AzureRmOperationalInsightsWindowsEventDataSource** adiciona uma fonte de dados que coleta logs de eventos do Windows de computadores conectados que executam o sistema operacional Windows em insights operacionais do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a15e-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="3a15e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a15e-109">EXAMPLES</span></span>

## <span data-ttu-id="3a15e-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a15e-110">PARAMETERS</span></span>

### <span data-ttu-id="3a15e-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="3a15e-111">-CollectErrors</span></span>
<span data-ttu-id="3a15e-112">Indica que as insights operacionais coletam mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="3a15e-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="3a15e-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="3a15e-113">-CollectInformation</span></span>
<span data-ttu-id="3a15e-114">Indica que as insights operacionais coletam mensagens de informações.</span><span class="sxs-lookup"><span data-stu-id="3a15e-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="3a15e-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="3a15e-115">-CollectWarnings</span></span>
<span data-ttu-id="3a15e-116">Indica que as insights operacionais coletam mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="3a15e-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="3a15e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a15e-117">-DefaultProfile</span></span>
<span data-ttu-id="3a15e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3a15e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a15e-119">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="3a15e-119">-EventLogName</span></span>
<span data-ttu-id="3a15e-120">Especifica o nome do log de eventos.</span><span class="sxs-lookup"><span data-stu-id="3a15e-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="3a15e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3a15e-121">-Force</span></span>
<span data-ttu-id="3a15e-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a15e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a15e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a15e-123">-Name</span></span>
<span data-ttu-id="3a15e-124">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3a15e-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3a15e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a15e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a15e-126">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="3a15e-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3a15e-127">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3a15e-127">-Workspace</span></span>
<span data-ttu-id="3a15e-128">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="3a15e-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3a15e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a15e-129">-WorkspaceName</span></span>
<span data-ttu-id="3a15e-130">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="3a15e-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3a15e-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a15e-131">-Confirm</span></span>
<span data-ttu-id="3a15e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a15e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a15e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a15e-133">-WhatIf</span></span>
<span data-ttu-id="3a15e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a15e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a15e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a15e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a15e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a15e-136">CommonParameters</span></span>
<span data-ttu-id="3a15e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a15e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a15e-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a15e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a15e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a15e-139">INPUTS</span></span>

### <span data-ttu-id="3a15e-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a15e-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="3a15e-141">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a15e-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="3a15e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3a15e-142">System.String</span></span>

## <span data-ttu-id="3a15e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a15e-143">OUTPUTS</span></span>

### <span data-ttu-id="3a15e-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3a15e-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3a15e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a15e-145">NOTES</span></span>

## <span data-ttu-id="3a15e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a15e-146">RELATED LINKS</span></span>
