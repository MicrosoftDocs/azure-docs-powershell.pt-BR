---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772874"
---
# <span data-ttu-id="1dbf4-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1dbf4-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="1dbf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dbf4-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbf4-103">Atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="1dbf4-103">Updates a data source.</span></span>

## <span data-ttu-id="1dbf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dbf4-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbf4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dbf4-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbf4-106">O cmdlet **set-AzOperationalInsightsDataSource** atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="1dbf4-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="1dbf4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dbf4-107">EXAMPLES</span></span>

## <span data-ttu-id="1dbf4-108">OS</span><span class="sxs-lookup"><span data-stu-id="1dbf4-108">PARAMETERS</span></span>

### <span data-ttu-id="1dbf4-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="1dbf4-109">-DataSource</span></span>
<span data-ttu-id="1dbf4-110">Especifica a fonte de dados que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="1dbf4-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1dbf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbf4-111">-DefaultProfile</span></span>
<span data-ttu-id="1dbf4-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1dbf4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dbf4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbf4-113">CommonParameters</span></span>
<span data-ttu-id="1dbf4-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbf4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbf4-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbf4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbf4-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dbf4-116">INPUTS</span></span>

### <span data-ttu-id="1dbf4-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1dbf4-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1dbf4-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dbf4-118">OUTPUTS</span></span>

### <span data-ttu-id="1dbf4-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1dbf4-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1dbf4-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dbf4-120">NOTES</span></span>
* <span data-ttu-id="1dbf4-121">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="1dbf4-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="1dbf4-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dbf4-122">RELATED LINKS</span></span>

[<span data-ttu-id="1dbf4-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1dbf4-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="1dbf4-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1dbf4-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


