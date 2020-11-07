---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777202"
---
# <span data-ttu-id="e421a-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="e421a-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="e421a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e421a-102">SYNOPSIS</span></span>
<span data-ttu-id="e421a-103">Inicia a coleta de logs do IIS de computadores em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e421a-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="e421a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e421a-104">SYNTAX</span></span>

### <span data-ttu-id="e421a-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e421a-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e421a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e421a-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e421a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e421a-107">DESCRIPTION</span></span>
<span data-ttu-id="e421a-108">O cmdlet **Enable-AzOperationalInsightsIISLogCollection** inicia a coleta de logs dos serviços de informações da Internet (IIS) em computadores conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e421a-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="e421a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e421a-109">EXAMPLES</span></span>

## <span data-ttu-id="e421a-110">OS</span><span class="sxs-lookup"><span data-stu-id="e421a-110">PARAMETERS</span></span>

### <span data-ttu-id="e421a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e421a-111">-DefaultProfile</span></span>
<span data-ttu-id="e421a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e421a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e421a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e421a-113">-ResourceGroupName</span></span>
<span data-ttu-id="e421a-114">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="e421a-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="e421a-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e421a-115">-Workspace</span></span>
<span data-ttu-id="e421a-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="e421a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e421a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e421a-117">-WorkspaceName</span></span>
<span data-ttu-id="e421a-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="e421a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e421a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e421a-119">-Confirm</span></span>
<span data-ttu-id="e421a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e421a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e421a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e421a-121">-WhatIf</span></span>
<span data-ttu-id="e421a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e421a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e421a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e421a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e421a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e421a-124">CommonParameters</span></span>
<span data-ttu-id="e421a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e421a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e421a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e421a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e421a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e421a-127">INPUTS</span></span>

### <span data-ttu-id="e421a-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e421a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e421a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e421a-129">System.String</span></span>

## <span data-ttu-id="e421a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e421a-130">OUTPUTS</span></span>

### <span data-ttu-id="e421a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e421a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e421a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e421a-132">NOTES</span></span>

## <span data-ttu-id="e421a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e421a-133">RELATED LINKS</span></span>

[<span data-ttu-id="e421a-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="e421a-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


