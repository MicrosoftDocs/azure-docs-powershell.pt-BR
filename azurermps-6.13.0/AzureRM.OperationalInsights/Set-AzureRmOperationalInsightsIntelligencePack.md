---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 0e8335476fc1cb511aaddb5294ea508832a04003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428426"
---
# <span data-ttu-id="ca57d-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ca57d-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="ca57d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca57d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca57d-103">Habilita ou desabilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="ca57d-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca57d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca57d-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca57d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca57d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca57d-106">O cmdlet **set-AzureRmOperationalInsightsIntelligencePack** habilita o pacote de inteligência especificado se *habilitado* for definido como $true e desabilitado se *habilitado* for definido como $false.</span><span class="sxs-lookup"><span data-stu-id="ca57d-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="ca57d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca57d-107">EXAMPLES</span></span>

### <span data-ttu-id="ca57d-108">Exemplo 1: configurar pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="ca57d-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="ca57d-109">Esse comando habilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="ca57d-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="ca57d-110">OS</span><span class="sxs-lookup"><span data-stu-id="ca57d-110">PARAMETERS</span></span>

### <span data-ttu-id="ca57d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca57d-111">-DefaultProfile</span></span>
<span data-ttu-id="ca57d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca57d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca57d-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="ca57d-113">-Enabled</span></span>
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

### <span data-ttu-id="ca57d-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="ca57d-114">-IntelligencePackName</span></span>
<span data-ttu-id="ca57d-115">Especifica o nome do pacote de inteligência.</span><span class="sxs-lookup"><span data-stu-id="ca57d-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="ca57d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca57d-116">-ResourceGroupName</span></span>
<span data-ttu-id="ca57d-117">Especifica o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ca57d-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="ca57d-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ca57d-118">-WorkspaceName</span></span>
<span data-ttu-id="ca57d-119">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca57d-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="ca57d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca57d-120">CommonParameters</span></span>
<span data-ttu-id="ca57d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca57d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca57d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca57d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca57d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca57d-123">INPUTS</span></span>

### <span data-ttu-id="ca57d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ca57d-124">System.String</span></span>

### <span data-ttu-id="ca57d-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca57d-125">System.Boolean</span></span>

## <span data-ttu-id="ca57d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca57d-126">OUTPUTS</span></span>

### <span data-ttu-id="ca57d-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ca57d-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="ca57d-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca57d-128">NOTES</span></span>

## <span data-ttu-id="ca57d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca57d-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca57d-130">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="ca57d-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


