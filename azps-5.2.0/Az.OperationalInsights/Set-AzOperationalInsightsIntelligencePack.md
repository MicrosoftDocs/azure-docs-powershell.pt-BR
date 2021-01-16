---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258970"
---
# <span data-ttu-id="ff4eb-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ff4eb-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="ff4eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4eb-103">Habilita ou desabilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="ff4eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff4eb-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff4eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="ff4eb-106">O cmdlet **set-AzOperationalInsightsIntelligencePack** habilita o pacote de inteligência especificado se *habilitado* for definido como $true e desabilitado se *habilitado* for definido como $false.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="ff4eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff4eb-107">EXAMPLES</span></span>

### <span data-ttu-id="ff4eb-108">Exemplo 1: configurar pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="ff4eb-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="ff4eb-109">Esse comando habilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="ff4eb-110">OS</span><span class="sxs-lookup"><span data-stu-id="ff4eb-110">PARAMETERS</span></span>

### <span data-ttu-id="ff4eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4eb-111">-DefaultProfile</span></span>
<span data-ttu-id="ff4eb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff4eb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff4eb-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="ff4eb-113">-Enabled</span></span>
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

### <span data-ttu-id="ff4eb-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="ff4eb-114">-IntelligencePackName</span></span>
<span data-ttu-id="ff4eb-115">Especifica o nome do pacote de inteligência.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="ff4eb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4eb-116">-ResourceGroupName</span></span>
<span data-ttu-id="ff4eb-117">Especifica o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ff4eb-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="ff4eb-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff4eb-118">-WorkspaceName</span></span>
<span data-ttu-id="ff4eb-119">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="ff4eb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4eb-120">CommonParameters</span></span>
<span data-ttu-id="ff4eb-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4eb-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4eb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4eb-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff4eb-123">INPUTS</span></span>

### <span data-ttu-id="ff4eb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ff4eb-124">System.String</span></span>

### <span data-ttu-id="ff4eb-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff4eb-125">System.Boolean</span></span>

## <span data-ttu-id="ff4eb-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff4eb-126">OUTPUTS</span></span>

### <span data-ttu-id="ff4eb-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ff4eb-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="ff4eb-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff4eb-128">NOTES</span></span>

## <span data-ttu-id="ff4eb-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff4eb-129">RELATED LINKS</span></span>

[<span data-ttu-id="ff4eb-130">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="ff4eb-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


