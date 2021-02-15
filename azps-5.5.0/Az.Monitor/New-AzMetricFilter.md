---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114245"
---
# <span data-ttu-id="963fa-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="963fa-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="963fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="963fa-102">SYNOPSIS</span></span>
<span data-ttu-id="963fa-103">Cria um filtro de dimensão métrica que pode ser usado para métricas de consulta.</span><span class="sxs-lookup"><span data-stu-id="963fa-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="963fa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="963fa-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="963fa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="963fa-105">DESCRIPTION</span></span>
<span data-ttu-id="963fa-106">O **cmdlet New-AzMetricFilter** cria um filtro de dimensão métrica que pode ser usado para métricas de consulta.</span><span class="sxs-lookup"><span data-stu-id="963fa-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="963fa-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="963fa-107">EXAMPLES</span></span>

### <span data-ttu-id="963fa-108">Exemplo 1: Criar um filtro de dimensão métrica</span><span class="sxs-lookup"><span data-stu-id="963fa-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="963fa-109">Este comando cria um filtro de dimensão métrica do formato "Cidade eq 'Seattle' ou City eq 'New York'".</span><span class="sxs-lookup"><span data-stu-id="963fa-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="963fa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="963fa-110">PARAMETERS</span></span>

### <span data-ttu-id="963fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963fa-111">-DefaultProfile</span></span>
<span data-ttu-id="963fa-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="963fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963fa-113">-Dimensão</span><span class="sxs-lookup"><span data-stu-id="963fa-113">-Dimension</span></span>
<span data-ttu-id="963fa-114">O nome da dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="963fa-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="963fa-115">-Operador</span><span class="sxs-lookup"><span data-stu-id="963fa-115">-Operator</span></span>
<span data-ttu-id="963fa-116">Especifica o operador usado para selecionar a dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="963fa-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="963fa-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="963fa-117">-Value</span></span>
<span data-ttu-id="963fa-118">Especifica a matriz de valores de dimensão métrica.</span><span class="sxs-lookup"><span data-stu-id="963fa-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="963fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963fa-119">CommonParameters</span></span>
<span data-ttu-id="963fa-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963fa-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="963fa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963fa-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="963fa-122">INPUTS</span></span>

### <span data-ttu-id="963fa-123">System.String</span><span class="sxs-lookup"><span data-stu-id="963fa-123">System.String</span></span>

### <span data-ttu-id="963fa-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="963fa-124">System.String[]</span></span>

## <span data-ttu-id="963fa-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="963fa-125">OUTPUTS</span></span>

### <span data-ttu-id="963fa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="963fa-126">System.String</span></span>

## <span data-ttu-id="963fa-127">Notas</span><span class="sxs-lookup"><span data-stu-id="963fa-127">NOTES</span></span>

## <span data-ttu-id="963fa-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="963fa-128">RELATED LINKS</span></span>

<span data-ttu-id="963fa-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="963fa-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

