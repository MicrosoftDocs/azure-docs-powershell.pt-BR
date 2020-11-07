---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0679f4281d9528a7124f4a9a5235d47dd8af107c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775697"
---
# <span data-ttu-id="26e44-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="26e44-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="26e44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26e44-102">SYNOPSIS</span></span>
<span data-ttu-id="26e44-103">Cria um objeto do tipo origem</span><span class="sxs-lookup"><span data-stu-id="26e44-103">Creates an object of type Source</span></span>

## <span data-ttu-id="26e44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26e44-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26e44-105">DESCRIPTION</span></span>
<span data-ttu-id="26e44-106">Cria um objeto do tipo Source.</span><span class="sxs-lookup"><span data-stu-id="26e44-106">Creates an object of type Source.</span></span>
<span data-ttu-id="26e44-107">Esse objeto deve ser passado para o comando que cria a regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="26e44-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="26e44-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26e44-108">EXAMPLES</span></span>

### <span data-ttu-id="26e44-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26e44-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="26e44-110">OS</span><span class="sxs-lookup"><span data-stu-id="26e44-110">PARAMETERS</span></span>

### <span data-ttu-id="26e44-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="26e44-111">-AuthorizedResource</span></span>
<span data-ttu-id="26e44-112">A lista de recursos autorizados para este alerta</span><span class="sxs-lookup"><span data-stu-id="26e44-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e44-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="26e44-113">-DataSourceId</span></span>
<span data-ttu-id="26e44-114">A fonte de dados na qual este alerta é criado</span><span class="sxs-lookup"><span data-stu-id="26e44-114">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e44-115">-DefaultProfile</span></span>
<span data-ttu-id="26e44-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26e44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e44-117">-Consulta</span><span class="sxs-lookup"><span data-stu-id="26e44-117">-Query</span></span>
<span data-ttu-id="26e44-118">A consulta de alerta</span><span class="sxs-lookup"><span data-stu-id="26e44-118">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e44-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="26e44-119">-QueryType</span></span>
<span data-ttu-id="26e44-120">Tipo de consulta-valores com suporte atualmente: ResultCount</span><span class="sxs-lookup"><span data-stu-id="26e44-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e44-121">CommonParameters</span></span>
<span data-ttu-id="26e44-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e44-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26e44-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e44-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26e44-124">INPUTS</span></span>

### <span data-ttu-id="26e44-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="26e44-125">None</span></span>

## <span data-ttu-id="26e44-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26e44-126">OUTPUTS</span></span>

### <span data-ttu-id="26e44-127">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="26e44-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="26e44-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26e44-128">NOTES</span></span>

## <span data-ttu-id="26e44-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26e44-129">RELATED LINKS</span></span>
