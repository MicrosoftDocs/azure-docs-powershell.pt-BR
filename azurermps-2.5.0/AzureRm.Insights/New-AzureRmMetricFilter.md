---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785767"
---
# <span data-ttu-id="c416e-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="c416e-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="c416e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c416e-102">SYNOPSIS</span></span>
<span data-ttu-id="c416e-103">Cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="c416e-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c416e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c416e-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c416e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c416e-105">DESCRIPTION</span></span>
<span data-ttu-id="c416e-106">O cmdlet **New-AzureRmMetricFilter** cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="c416e-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="c416e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c416e-107">EXAMPLES</span></span>

### <span data-ttu-id="c416e-108">Exemplo 1: criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="c416e-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="c416e-109">Esse comando cria o filtro de dimensão métrica do formato "City eq" Seattle ' ou City eq ' New York ' ".</span><span class="sxs-lookup"><span data-stu-id="c416e-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="c416e-110">OS</span><span class="sxs-lookup"><span data-stu-id="c416e-110">PARAMETERS</span></span>

### <span data-ttu-id="c416e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c416e-111">-DefaultProfile</span></span>
<span data-ttu-id="c416e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c416e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c416e-113">-Dimensão</span><span class="sxs-lookup"><span data-stu-id="c416e-113">-Dimension</span></span>
<span data-ttu-id="c416e-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="c416e-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="c416e-115">-Operador</span><span class="sxs-lookup"><span data-stu-id="c416e-115">-Operator</span></span>
<span data-ttu-id="c416e-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="c416e-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="c416e-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="c416e-117">-Value</span></span>
<span data-ttu-id="c416e-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="c416e-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="c416e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c416e-119">CommonParameters</span></span>
<span data-ttu-id="c416e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c416e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c416e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c416e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c416e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c416e-122">INPUTS</span></span>

### <span data-ttu-id="c416e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c416e-123">System.String</span></span>

### <span data-ttu-id="c416e-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="c416e-124">System.String[]</span></span>

## <span data-ttu-id="c416e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c416e-125">OUTPUTS</span></span>

### <span data-ttu-id="c416e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c416e-126">System.String</span></span>

## <span data-ttu-id="c416e-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c416e-127">NOTES</span></span>

## <span data-ttu-id="c416e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c416e-128">RELATED LINKS</span></span>

<span data-ttu-id="c416e-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="c416e-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

