---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124797"
---
# <span data-ttu-id="7e596-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="7e596-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="7e596-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e596-102">SYNOPSIS</span></span>
<span data-ttu-id="7e596-103">Cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="7e596-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="7e596-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e596-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e596-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e596-105">DESCRIPTION</span></span>
<span data-ttu-id="7e596-106">O cmdlet **New-AzMetricFilter** cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="7e596-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="7e596-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e596-107">EXAMPLES</span></span>

### <span data-ttu-id="7e596-108">Exemplo 1: criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="7e596-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="7e596-109">Esse comando cria o filtro de dimensão métrica do formato "City eq" Seattle ' ou City eq ' New York ' ".</span><span class="sxs-lookup"><span data-stu-id="7e596-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="7e596-110">OS</span><span class="sxs-lookup"><span data-stu-id="7e596-110">PARAMETERS</span></span>

### <span data-ttu-id="7e596-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e596-111">-DefaultProfile</span></span>
<span data-ttu-id="7e596-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e596-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e596-113">-Dimensão</span><span class="sxs-lookup"><span data-stu-id="7e596-113">-Dimension</span></span>
<span data-ttu-id="7e596-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="7e596-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="7e596-115">-Operador</span><span class="sxs-lookup"><span data-stu-id="7e596-115">-Operator</span></span>
<span data-ttu-id="7e596-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="7e596-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="7e596-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="7e596-117">-Value</span></span>
<span data-ttu-id="7e596-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="7e596-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="7e596-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e596-119">CommonParameters</span></span>
<span data-ttu-id="7e596-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e596-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e596-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e596-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e596-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e596-122">INPUTS</span></span>

### <span data-ttu-id="7e596-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7e596-123">System.String</span></span>

### <span data-ttu-id="7e596-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="7e596-124">System.String[]</span></span>

## <span data-ttu-id="7e596-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e596-125">OUTPUTS</span></span>

### <span data-ttu-id="7e596-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7e596-126">System.String</span></span>

## <span data-ttu-id="7e596-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e596-127">NOTES</span></span>

## <span data-ttu-id="7e596-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e596-128">RELATED LINKS</span></span>

<span data-ttu-id="7e596-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7e596-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

