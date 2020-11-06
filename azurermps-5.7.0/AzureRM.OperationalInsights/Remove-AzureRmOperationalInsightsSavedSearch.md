---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: e66ca332d2fd59faa64e4360d00af714cfa28475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426678"
---
# <span data-ttu-id="ff895-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ff895-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ff895-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff895-102">SYNOPSIS</span></span>
<span data-ttu-id="ff895-103">Remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff895-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff895-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff895-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff895-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff895-105">DESCRIPTION</span></span>
<span data-ttu-id="ff895-106">O cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff895-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ff895-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff895-107">EXAMPLES</span></span>

### <span data-ttu-id="ff895-108">Exemplo 1: remover uma pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="ff895-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="ff895-109">Esse comando Remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff895-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ff895-110">OS</span><span class="sxs-lookup"><span data-stu-id="ff895-110">PARAMETERS</span></span>

### <span data-ttu-id="ff895-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff895-111">-DefaultProfile</span></span>
<span data-ttu-id="ff895-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff895-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff895-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff895-113">-ResourceGroupName</span></span>
<span data-ttu-id="ff895-114">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff895-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ff895-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ff895-115">-SavedSearchId</span></span>
<span data-ttu-id="ff895-116">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="ff895-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="ff895-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff895-117">-WorkspaceName</span></span>
<span data-ttu-id="ff895-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff895-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ff895-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff895-119">-Confirm</span></span>
<span data-ttu-id="ff895-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff895-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff895-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff895-121">-WhatIf</span></span>
<span data-ttu-id="ff895-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff895-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff895-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff895-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff895-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff895-124">CommonParameters</span></span>
<span data-ttu-id="ff895-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff895-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff895-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff895-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff895-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff895-127">INPUTS</span></span>

### <span data-ttu-id="ff895-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff895-128">None</span></span>
<span data-ttu-id="ff895-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ff895-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff895-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff895-130">OUTPUTS</span></span>

## <span data-ttu-id="ff895-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff895-131">NOTES</span></span>

## <span data-ttu-id="ff895-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff895-132">RELATED LINKS</span></span>

[<span data-ttu-id="ff895-133">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="ff895-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


