---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944525"
---
# <span data-ttu-id="49bbc-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="49bbc-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="49bbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="49bbc-103">Atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="49bbc-103">Updates a data source.</span></span>

## <span data-ttu-id="49bbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49bbc-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49bbc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="49bbc-106">O cmdlet **set-AzOperationalInsightsDataSource** atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="49bbc-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="49bbc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49bbc-107">EXAMPLES</span></span>

## <span data-ttu-id="49bbc-108">OS</span><span class="sxs-lookup"><span data-stu-id="49bbc-108">PARAMETERS</span></span>

### <span data-ttu-id="49bbc-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="49bbc-109">-DataSource</span></span>
<span data-ttu-id="49bbc-110">Especifica a fonte de dados que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="49bbc-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="49bbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bbc-111">-DefaultProfile</span></span>
<span data-ttu-id="49bbc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49bbc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49bbc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bbc-113">CommonParameters</span></span>
<span data-ttu-id="49bbc-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bbc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bbc-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49bbc-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bbc-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49bbc-116">INPUTS</span></span>

### <span data-ttu-id="49bbc-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="49bbc-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="49bbc-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49bbc-118">OUTPUTS</span></span>

### <span data-ttu-id="49bbc-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="49bbc-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="49bbc-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49bbc-120">NOTES</span></span>
* <span data-ttu-id="49bbc-121">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="49bbc-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="49bbc-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49bbc-122">RELATED LINKS</span></span>

[<span data-ttu-id="49bbc-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="49bbc-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="49bbc-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="49bbc-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


