---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602204"
---
# <span data-ttu-id="430e1-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="430e1-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="430e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="430e1-102">SYNOPSIS</span></span>
<span data-ttu-id="430e1-103">Habilita ou desabilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="430e1-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="430e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="430e1-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="430e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="430e1-105">DESCRIPTION</span></span>
<span data-ttu-id="430e1-106">O cmdlet **set-AzureRmOperationalInsightsIntelligencePack** habilita o pacote de inteligência especificado se *habilitado* for definido como $true e desabilitado se *habilitado* for definido como $false.</span><span class="sxs-lookup"><span data-stu-id="430e1-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="430e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="430e1-107">EXAMPLES</span></span>

### <span data-ttu-id="430e1-108">Exemplo 1: configurar pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="430e1-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="430e1-109">Esse comando habilita o pacote de inteligência especificado.</span><span class="sxs-lookup"><span data-stu-id="430e1-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="430e1-110">OS</span><span class="sxs-lookup"><span data-stu-id="430e1-110">PARAMETERS</span></span>

### <span data-ttu-id="430e1-111">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="430e1-111">-Enabled</span></span>
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

### <span data-ttu-id="430e1-112">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="430e1-112">-IntelligencePackName</span></span>
<span data-ttu-id="430e1-113">Especifica o nome do pacote de inteligência.</span><span class="sxs-lookup"><span data-stu-id="430e1-113">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="430e1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="430e1-114">-ResourceGroupName</span></span>
<span data-ttu-id="430e1-115">Especifica o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="430e1-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="430e1-116">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="430e1-116">-WorkspaceName</span></span>
<span data-ttu-id="430e1-117">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="430e1-117">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="430e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="430e1-118">-DefaultProfile</span></span>
<span data-ttu-id="430e1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="430e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="430e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430e1-120">CommonParameters</span></span>
<span data-ttu-id="430e1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="430e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430e1-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430e1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430e1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="430e1-123">INPUTS</span></span>

## <span data-ttu-id="430e1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="430e1-124">OUTPUTS</span></span>

## <span data-ttu-id="430e1-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="430e1-125">NOTES</span></span>

## <span data-ttu-id="430e1-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="430e1-126">RELATED LINKS</span></span>

[<span data-ttu-id="430e1-127">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="430e1-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


