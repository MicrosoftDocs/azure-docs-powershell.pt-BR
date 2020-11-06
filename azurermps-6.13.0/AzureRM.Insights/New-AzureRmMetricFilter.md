---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610904"
---
# <span data-ttu-id="b09ee-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="b09ee-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="b09ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b09ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b09ee-103">Cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="b09ee-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b09ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b09ee-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b09ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b09ee-105">DESCRIPTION</span></span>
<span data-ttu-id="b09ee-106">O cmdlet **New-AzureRmMetricFilter** cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="b09ee-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="b09ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b09ee-107">EXAMPLES</span></span>

### <span data-ttu-id="b09ee-108">Exemplo 1: criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="b09ee-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="b09ee-109">Esse comando cria o filtro de dimensão métrica do formato "City eq" Seattle ' ou City eq ' New York ' ".</span><span class="sxs-lookup"><span data-stu-id="b09ee-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="b09ee-110">OS</span><span class="sxs-lookup"><span data-stu-id="b09ee-110">PARAMETERS</span></span>

### <span data-ttu-id="b09ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09ee-111">-DefaultProfile</span></span>
<span data-ttu-id="b09ee-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b09ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b09ee-113">-Dimensão</span><span class="sxs-lookup"><span data-stu-id="b09ee-113">-Dimension</span></span>
<span data-ttu-id="b09ee-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="b09ee-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="b09ee-115">-Operador</span><span class="sxs-lookup"><span data-stu-id="b09ee-115">-Operator</span></span>
<span data-ttu-id="b09ee-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="b09ee-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b09ee-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="b09ee-117">-Value</span></span>
<span data-ttu-id="b09ee-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="b09ee-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b09ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09ee-119">CommonParameters</span></span>
<span data-ttu-id="b09ee-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b09ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09ee-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b09ee-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09ee-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b09ee-122">INPUTS</span></span>

### <span data-ttu-id="b09ee-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b09ee-123">System.String</span></span>

### <span data-ttu-id="b09ee-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="b09ee-124">System.String[]</span></span>

## <span data-ttu-id="b09ee-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b09ee-125">OUTPUTS</span></span>

### <span data-ttu-id="b09ee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b09ee-126">System.String</span></span>

## <span data-ttu-id="b09ee-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b09ee-127">NOTES</span></span>

## <span data-ttu-id="b09ee-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b09ee-128">RELATED LINKS</span></span>

<span data-ttu-id="b09ee-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="b09ee-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

