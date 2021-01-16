---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259752"
---
# <span data-ttu-id="84616-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="84616-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="84616-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84616-102">SYNOPSIS</span></span>
<span data-ttu-id="84616-103">Inicia a coleta de logs do IIS de computadores em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84616-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="84616-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84616-104">SYNTAX</span></span>

### <span data-ttu-id="84616-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="84616-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84616-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="84616-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84616-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84616-107">DESCRIPTION</span></span>
<span data-ttu-id="84616-108">O cmdlet **Enable-AzOperationalInsightsIISLogCollection** inicia a coleta de logs dos serviços de informações da Internet (IIS) em computadores conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84616-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="84616-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84616-109">EXAMPLES</span></span>

## <span data-ttu-id="84616-110">OS</span><span class="sxs-lookup"><span data-stu-id="84616-110">PARAMETERS</span></span>

### <span data-ttu-id="84616-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84616-111">-DefaultProfile</span></span>
<span data-ttu-id="84616-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="84616-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84616-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84616-113">-ResourceGroupName</span></span>
<span data-ttu-id="84616-114">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="84616-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="84616-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="84616-115">-Workspace</span></span>
<span data-ttu-id="84616-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="84616-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="84616-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84616-117">-WorkspaceName</span></span>
<span data-ttu-id="84616-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="84616-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="84616-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84616-119">-Confirm</span></span>
<span data-ttu-id="84616-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84616-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84616-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84616-121">-WhatIf</span></span>
<span data-ttu-id="84616-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84616-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84616-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84616-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84616-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84616-124">CommonParameters</span></span>
<span data-ttu-id="84616-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84616-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84616-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84616-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84616-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84616-127">INPUTS</span></span>

### <span data-ttu-id="84616-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="84616-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="84616-129">System. String</span><span class="sxs-lookup"><span data-stu-id="84616-129">System.String</span></span>

## <span data-ttu-id="84616-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84616-130">OUTPUTS</span></span>

### <span data-ttu-id="84616-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="84616-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="84616-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84616-132">NOTES</span></span>

## <span data-ttu-id="84616-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84616-133">RELATED LINKS</span></span>

[<span data-ttu-id="84616-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="84616-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


