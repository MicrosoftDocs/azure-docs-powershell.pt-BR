---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5bf4f178ee3343b5100dad87836c3215fba4cfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433194"
---
# <span data-ttu-id="65ad9-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="65ad9-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="65ad9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="65ad9-103">Atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="65ad9-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ad9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65ad9-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ad9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="65ad9-106">O cmdlet **set-AzureRmOperationalInsightsDataSource** atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="65ad9-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="65ad9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65ad9-107">EXAMPLES</span></span>

## <span data-ttu-id="65ad9-108">OS</span><span class="sxs-lookup"><span data-stu-id="65ad9-108">PARAMETERS</span></span>

### <span data-ttu-id="65ad9-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="65ad9-109">-DataSource</span></span>
<span data-ttu-id="65ad9-110">Especifica a fonte de dados que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="65ad9-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="65ad9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ad9-111">-DefaultProfile</span></span>
<span data-ttu-id="65ad9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="65ad9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65ad9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ad9-113">CommonParameters</span></span>
<span data-ttu-id="65ad9-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ad9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ad9-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ad9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ad9-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65ad9-116">INPUTS</span></span>

### <span data-ttu-id="65ad9-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="65ad9-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>
<span data-ttu-id="65ad9-118">Parâmetros: DataSource (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65ad9-118">Parameters: DataSource (ByValue)</span></span>

## <span data-ttu-id="65ad9-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65ad9-119">OUTPUTS</span></span>

### <span data-ttu-id="65ad9-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="65ad9-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="65ad9-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65ad9-121">NOTES</span></span>
* <span data-ttu-id="65ad9-122">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="65ad9-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="65ad9-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65ad9-123">RELATED LINKS</span></span>

[<span data-ttu-id="65ad9-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="65ad9-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="65ad9-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="65ad9-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


