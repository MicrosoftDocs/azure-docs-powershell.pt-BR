---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433123"
---
# <span data-ttu-id="39af4-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="39af4-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="39af4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39af4-102">SYNOPSIS</span></span>
<span data-ttu-id="39af4-103">Obtém as métricas de uso de um recurso.</span><span class="sxs-lookup"><span data-stu-id="39af4-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39af4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39af4-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39af4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39af4-105">DESCRIPTION</span></span>
<span data-ttu-id="39af4-106">O cmdlet **Get-AzureRmUsage** Obtém as métricas de uso para um recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="39af4-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="39af4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39af4-107">EXAMPLES</span></span>

### <span data-ttu-id="39af4-108">Exemplo 1: obter métricas de uso por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="39af4-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="39af4-109">Esse comando obtém as métricas de uso do site especificado.</span><span class="sxs-lookup"><span data-stu-id="39af4-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="39af4-110">OS</span><span class="sxs-lookup"><span data-stu-id="39af4-110">PARAMETERS</span></span>

### <span data-ttu-id="39af4-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="39af4-111">-ApiVersion</span></span>
<span data-ttu-id="39af4-112">Especifica uma cadeia de caracteres de versão da API, por exemplo, 2014-04-01, que é aceita pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="39af4-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39af4-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="39af4-113">-EndTime</span></span>
<span data-ttu-id="39af4-114">Especifica a última data e hora para pesquisar.</span><span class="sxs-lookup"><span data-stu-id="39af4-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="39af4-115">Você pode usar o cmdlet Get-Date para obter um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="39af4-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39af4-116">-Metricnames</span><span class="sxs-lookup"><span data-stu-id="39af4-116">-MetricNames</span></span>
<span data-ttu-id="39af4-117">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="39af4-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39af4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39af4-118">-ResourceId</span></span>
<span data-ttu-id="39af4-119">Especifica a ID do recurso para a métrica.</span><span class="sxs-lookup"><span data-stu-id="39af4-119">Specifies the ID of the resource for the metric.</span></span>

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

### <span data-ttu-id="39af4-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="39af4-120">-StartTime</span></span>
<span data-ttu-id="39af4-121">Especifica a hora e a data mais antigas a serem pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="39af4-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="39af4-122">Você pode usar o cmdlet Get-Date para obter um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="39af4-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39af4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39af4-123">-DefaultProfile</span></span>
<span data-ttu-id="39af4-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39af4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39af4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39af4-125">CommonParameters</span></span>
<span data-ttu-id="39af4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39af4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39af4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39af4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39af4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39af4-128">INPUTS</span></span>

## <span data-ttu-id="39af4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39af4-129">OUTPUTS</span></span>

### <span data-ttu-id="39af4-130">Microsoft. Azure. Commands. insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="39af4-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="39af4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39af4-131">NOTES</span></span>

## <span data-ttu-id="39af4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39af4-132">RELATED LINKS</span></span>

[<span data-ttu-id="39af4-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="39af4-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


