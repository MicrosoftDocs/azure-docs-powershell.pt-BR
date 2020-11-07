---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: 203044deb41ae21591b33ea6e306bcd98905e540
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772184"
---
# <span data-ttu-id="50851-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="50851-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="50851-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50851-102">SYNOPSIS</span></span>
<span data-ttu-id="50851-103">Cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="50851-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="50851-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50851-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50851-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50851-105">DESCRIPTION</span></span>
<span data-ttu-id="50851-106">O cmdlet **New-AzMetricFilter** cria um filtro de dimensão métrica que pode ser usado para consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="50851-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="50851-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50851-107">EXAMPLES</span></span>

### <span data-ttu-id="50851-108">Exemplo 1: criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="50851-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="50851-109">Esse comando cria o filtro de dimensão métrica do formato "City eq" Seattle ' ou City eq ' New York ' ".</span><span class="sxs-lookup"><span data-stu-id="50851-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="50851-110">OS</span><span class="sxs-lookup"><span data-stu-id="50851-110">PARAMETERS</span></span>

### <span data-ttu-id="50851-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50851-111">-DefaultProfile</span></span>
<span data-ttu-id="50851-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50851-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50851-113">-Dimensão</span><span class="sxs-lookup"><span data-stu-id="50851-113">-Dimension</span></span>
<span data-ttu-id="50851-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="50851-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="50851-115">-Operador</span><span class="sxs-lookup"><span data-stu-id="50851-115">-Operator</span></span>
<span data-ttu-id="50851-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="50851-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="50851-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="50851-117">-Value</span></span>
<span data-ttu-id="50851-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="50851-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="50851-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50851-119">CommonParameters</span></span>
<span data-ttu-id="50851-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50851-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50851-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50851-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50851-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50851-122">INPUTS</span></span>

### <span data-ttu-id="50851-123">System. String</span><span class="sxs-lookup"><span data-stu-id="50851-123">System.String</span></span>

### <span data-ttu-id="50851-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="50851-124">System.String[]</span></span>

## <span data-ttu-id="50851-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50851-125">OUTPUTS</span></span>

### <span data-ttu-id="50851-126">System. String</span><span class="sxs-lookup"><span data-stu-id="50851-126">System.String</span></span>

## <span data-ttu-id="50851-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50851-127">NOTES</span></span>

## <span data-ttu-id="50851-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50851-128">RELATED LINKS</span></span>

<span data-ttu-id="50851-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="50851-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

