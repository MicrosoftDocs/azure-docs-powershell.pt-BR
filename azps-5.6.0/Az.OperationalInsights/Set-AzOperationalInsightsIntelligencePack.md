---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: ee65492adc8c2756a2d19871e4c673668d471c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890199"
---
# <span data-ttu-id="65dad-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="65dad-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="65dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65dad-102">SYNOPSIS</span></span>
<span data-ttu-id="65dad-103">Habilita ou desabilita o Intelligence Pack especificado.</span><span class="sxs-lookup"><span data-stu-id="65dad-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="65dad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65dad-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65dad-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65dad-105">DESCRIPTION</span></span>
<span data-ttu-id="65dad-106">O cmdlet **Set-AzOperationalInsightsIntelligencePack** habilita o  Pacote de Inteligência especificado se Habilitado estiver definido como $True e o desabilitará se *Habilitado* estiver definido como $False.</span><span class="sxs-lookup"><span data-stu-id="65dad-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="65dad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65dad-107">EXAMPLES</span></span>

### <span data-ttu-id="65dad-108">Exemplo 1: Definir Pacotes de Inteligência</span><span class="sxs-lookup"><span data-stu-id="65dad-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="65dad-109">Este comando habilita o Intelligence Pack especificado.</span><span class="sxs-lookup"><span data-stu-id="65dad-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="65dad-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65dad-110">PARAMETERS</span></span>

### <span data-ttu-id="65dad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65dad-111">-DefaultProfile</span></span>
<span data-ttu-id="65dad-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="65dad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65dad-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="65dad-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dad-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="65dad-114">-IntelligencePackName</span></span>
<span data-ttu-id="65dad-115">Especifica o nome do Pacote de Inteligência.</span><span class="sxs-lookup"><span data-stu-id="65dad-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dad-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65dad-116">-ResourceGroupName</span></span>
<span data-ttu-id="65dad-117">Especifica o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="65dad-117">Specifies the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dad-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65dad-118">-WorkspaceName</span></span>
<span data-ttu-id="65dad-119">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="65dad-119">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dad-120">CommonParameters</span></span>
<span data-ttu-id="65dad-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65dad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dad-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65dad-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dad-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65dad-123">INPUTS</span></span>

### <span data-ttu-id="65dad-124">System.String</span><span class="sxs-lookup"><span data-stu-id="65dad-124">System.String</span></span>

### <span data-ttu-id="65dad-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65dad-125">System.Boolean</span></span>

## <span data-ttu-id="65dad-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65dad-126">OUTPUTS</span></span>

### <span data-ttu-id="65dad-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="65dad-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="65dad-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="65dad-128">NOTES</span></span>

## <span data-ttu-id="65dad-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65dad-129">RELATED LINKS</span></span>

[<span data-ttu-id="65dad-130">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="65dad-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


