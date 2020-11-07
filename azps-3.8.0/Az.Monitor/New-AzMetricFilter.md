---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940396"
---
# <span data-ttu-id="c9b76-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="c9b76-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="c9b76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9b76-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b76-103">Cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="c9b76-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="c9b76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9b76-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9b76-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9b76-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b76-106">O cmdlet **New-AzMetricFilter** cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="c9b76-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="c9b76-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9b76-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b76-108">Exemplo 1: criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="c9b76-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="c9b76-109">Esse comando cria o filtro de dimensão métrica do formato "City eq" Seattle ' ou City eq ' New York ' ".</span><span class="sxs-lookup"><span data-stu-id="c9b76-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="c9b76-110">OS</span><span class="sxs-lookup"><span data-stu-id="c9b76-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b76-111">-DefaultProfile</span></span>
<span data-ttu-id="c9b76-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b76-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b76-113">-Dimensão</span><span class="sxs-lookup"><span data-stu-id="c9b76-113">-Dimension</span></span>
<span data-ttu-id="c9b76-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="c9b76-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="c9b76-115">-Operador</span><span class="sxs-lookup"><span data-stu-id="c9b76-115">-Operator</span></span>
<span data-ttu-id="c9b76-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="c9b76-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="c9b76-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="c9b76-117">-Value</span></span>
<span data-ttu-id="c9b76-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="c9b76-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="c9b76-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b76-119">CommonParameters</span></span>
<span data-ttu-id="c9b76-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b76-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b76-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9b76-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b76-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9b76-122">INPUTS</span></span>

### <span data-ttu-id="c9b76-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b76-123">System.String</span></span>

### <span data-ttu-id="c9b76-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="c9b76-124">System.String[]</span></span>

## <span data-ttu-id="c9b76-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9b76-125">OUTPUTS</span></span>

### <span data-ttu-id="c9b76-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b76-126">System.String</span></span>

## <span data-ttu-id="c9b76-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9b76-127">NOTES</span></span>

## <span data-ttu-id="c9b76-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9b76-128">RELATED LINKS</span></span>

<span data-ttu-id="c9b76-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="c9b76-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

