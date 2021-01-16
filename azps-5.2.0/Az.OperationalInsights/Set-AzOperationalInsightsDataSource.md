---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264352"
---
# <span data-ttu-id="7e23c-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7e23c-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="7e23c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e23c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e23c-103">Atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7e23c-103">Updates a data source.</span></span>

## <span data-ttu-id="7e23c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e23c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e23c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e23c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e23c-106">O cmdlet **set-AzOperationalInsightsDataSource** atualiza uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7e23c-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="7e23c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e23c-107">EXAMPLES</span></span>

## <span data-ttu-id="7e23c-108">OS</span><span class="sxs-lookup"><span data-stu-id="7e23c-108">PARAMETERS</span></span>

### <span data-ttu-id="7e23c-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="7e23c-109">-DataSource</span></span>
<span data-ttu-id="7e23c-110">Especifica a fonte de dados que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="7e23c-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7e23c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e23c-111">-DefaultProfile</span></span>
<span data-ttu-id="7e23c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7e23c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e23c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e23c-113">CommonParameters</span></span>
<span data-ttu-id="7e23c-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e23c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e23c-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e23c-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e23c-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e23c-116">INPUTS</span></span>

### <span data-ttu-id="7e23c-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7e23c-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7e23c-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e23c-118">OUTPUTS</span></span>

### <span data-ttu-id="7e23c-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7e23c-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7e23c-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e23c-120">NOTES</span></span>
* <span data-ttu-id="7e23c-121">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="7e23c-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7e23c-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e23c-122">RELATED LINKS</span></span>

[<span data-ttu-id="7e23c-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7e23c-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="7e23c-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7e23c-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


