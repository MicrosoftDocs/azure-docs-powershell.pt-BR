---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: a7fdb0824d464f1704f46a8e8fe19705b2b160fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893265"
---
# <span data-ttu-id="e8d7b-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="e8d7b-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="e8d7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d7b-103">Cria um filtro de dimensão métrica que pode ser usado para métricas de consulta.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="e8d7b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8d7b-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8d7b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d7b-106">O cmdlet **New-AzMetricFilter** cria um filtro de dimensão métrica que pode ser usado para métricas de consulta.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="e8d7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d7b-108">Exemplo 1: Criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="e8d7b-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="e8d7b-109">Este comando cria um filtro de dimensão métrica do formato "City eq 'Seattle' ou City eq 'New York'".</span><span class="sxs-lookup"><span data-stu-id="e8d7b-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="e8d7b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="e8d7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d7b-111">-DefaultProfile</span></span>
<span data-ttu-id="e8d7b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8d7b-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="e8d7b-113">-Dimension</span></span>
<span data-ttu-id="e8d7b-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="e8d7b-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="e8d7b-115">-Operator</span></span>
<span data-ttu-id="e8d7b-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="e8d7b-117">-Value</span><span class="sxs-lookup"><span data-stu-id="e8d7b-117">-Value</span></span>
<span data-ttu-id="e8d7b-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="e8d7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d7b-119">CommonParameters</span></span>
<span data-ttu-id="e8d7b-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d7b-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8d7b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d7b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8d7b-122">INPUTS</span></span>

### <span data-ttu-id="e8d7b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e8d7b-123">System.String</span></span>

### <span data-ttu-id="e8d7b-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e8d7b-124">System.String[]</span></span>

## <span data-ttu-id="e8d7b-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8d7b-125">OUTPUTS</span></span>

### <span data-ttu-id="e8d7b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e8d7b-126">System.String</span></span>

## <span data-ttu-id="e8d7b-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8d7b-127">NOTES</span></span>

## <span data-ttu-id="e8d7b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8d7b-128">RELATED LINKS</span></span>

<span data-ttu-id="e8d7b-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="e8d7b-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

