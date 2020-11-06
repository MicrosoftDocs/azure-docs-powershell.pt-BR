---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: c7a4a34e3969f209bcd6fcaae46ed93cd316aba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428133"
---
# <span data-ttu-id="23f7b-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="23f7b-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="23f7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="23f7b-103">Habilita ou desabilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="23f7b-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23f7b-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23f7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="23f7b-106">O cmdlet **set-AzureRmOperationalInsightsIntelligencePack** habilita o pacote de inteligência especificado se *habilitado* for definido como $true e desabilitado se *habilitado* for definido como $false.</span><span class="sxs-lookup"><span data-stu-id="23f7b-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="23f7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="23f7b-108">Exemplo 1: configurar pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="23f7b-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="23f7b-109">Esse comando habilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="23f7b-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="23f7b-110">OS</span><span class="sxs-lookup"><span data-stu-id="23f7b-110">PARAMETERS</span></span>

### <span data-ttu-id="23f7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f7b-111">-DefaultProfile</span></span>
<span data-ttu-id="23f7b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="23f7b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f7b-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="23f7b-113">-Enabled</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f7b-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="23f7b-114">-IntelligencePackName</span></span>
<span data-ttu-id="23f7b-115">Especifica o nome do pacote de inteligência.</span><span class="sxs-lookup"><span data-stu-id="23f7b-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f7b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f7b-116">-ResourceGroupName</span></span>
<span data-ttu-id="23f7b-117">Especifica o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="23f7b-117">Specifies the resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f7b-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23f7b-118">-WorkspaceName</span></span>
<span data-ttu-id="23f7b-119">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23f7b-119">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f7b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f7b-120">CommonParameters</span></span>
<span data-ttu-id="23f7b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f7b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f7b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f7b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f7b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23f7b-123">INPUTS</span></span>

### <span data-ttu-id="23f7b-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="23f7b-124">None</span></span>
<span data-ttu-id="23f7b-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="23f7b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23f7b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23f7b-126">OUTPUTS</span></span>

## <span data-ttu-id="23f7b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23f7b-127">NOTES</span></span>

## <span data-ttu-id="23f7b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23f7b-128">RELATED LINKS</span></span>

[<span data-ttu-id="23f7b-129">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="23f7b-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


