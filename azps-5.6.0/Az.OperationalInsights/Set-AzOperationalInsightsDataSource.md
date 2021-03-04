---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4156bc414105d6d104e8315d83f92f0fb6e19ab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890200"
---
# <span data-ttu-id="c2778-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c2778-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="c2778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2778-102">SYNOPSIS</span></span>
<span data-ttu-id="c2778-103">Atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="c2778-103">Updates a data source.</span></span>

## <span data-ttu-id="c2778-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c2778-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2778-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c2778-105">DESCRIPTION</span></span>
<span data-ttu-id="c2778-106">O cmdlet **Set-AzOperationalInsightsDataSource** atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="c2778-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="c2778-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2778-107">EXAMPLES</span></span>

## <span data-ttu-id="c2778-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c2778-108">PARAMETERS</span></span>

### <span data-ttu-id="c2778-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="c2778-109">-DataSource</span></span>
<span data-ttu-id="c2778-110">Especifica a fonte de dados que esse cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="c2778-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2778-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2778-111">-DefaultProfile</span></span>
<span data-ttu-id="c2778-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c2778-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2778-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2778-113">CommonParameters</span></span>
<span data-ttu-id="c2778-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2778-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2778-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2778-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2778-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2778-116">INPUTS</span></span>

### <span data-ttu-id="c2778-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c2778-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c2778-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c2778-118">OUTPUTS</span></span>

### <span data-ttu-id="c2778-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c2778-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c2778-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="c2778-120">NOTES</span></span>
* <span data-ttu-id="c2778-121">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="c2778-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c2778-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2778-122">RELATED LINKS</span></span>

[<span data-ttu-id="c2778-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c2778-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="c2778-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c2778-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


