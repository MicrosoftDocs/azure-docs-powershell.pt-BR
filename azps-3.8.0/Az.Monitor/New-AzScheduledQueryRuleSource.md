---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0fe5684805dfc3047abb39040d80eb8a388cf5a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940383"
---
# <span data-ttu-id="d47e5-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d47e5-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="d47e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d47e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d47e5-103">Cria um objeto do tipo origem</span><span class="sxs-lookup"><span data-stu-id="d47e5-103">Creates an object of type Source</span></span>

## <span data-ttu-id="d47e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d47e5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d47e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d47e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d47e5-106">Cria um objeto do tipo Source.</span><span class="sxs-lookup"><span data-stu-id="d47e5-106">Creates an object of type Source.</span></span>
<span data-ttu-id="d47e5-107">Esse objeto deve ser passado para o comando que cria a regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="d47e5-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="d47e5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d47e5-108">EXAMPLES</span></span>

### <span data-ttu-id="d47e5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d47e5-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="d47e5-110">OS</span><span class="sxs-lookup"><span data-stu-id="d47e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d47e5-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="d47e5-111">-AuthorizedResource</span></span>
<span data-ttu-id="d47e5-112">A lista de recursos autorizados para este alerta</span><span class="sxs-lookup"><span data-stu-id="d47e5-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="d47e5-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="d47e5-113">-DataSourceId</span></span>
<span data-ttu-id="d47e5-114">A fonte de dados na qual este alerta é criado</span><span class="sxs-lookup"><span data-stu-id="d47e5-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="d47e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d47e5-115">-DefaultProfile</span></span>
<span data-ttu-id="d47e5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d47e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d47e5-117">-Consulta</span><span class="sxs-lookup"><span data-stu-id="d47e5-117">-Query</span></span>
<span data-ttu-id="d47e5-118">A consulta de alerta</span><span class="sxs-lookup"><span data-stu-id="d47e5-118">The alert query</span></span>

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

### <span data-ttu-id="d47e5-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="d47e5-119">-QueryType</span></span>
<span data-ttu-id="d47e5-120">Tipo de consulta-valores com suporte atualmente: ResultCount</span><span class="sxs-lookup"><span data-stu-id="d47e5-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="d47e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d47e5-121">CommonParameters</span></span>
<span data-ttu-id="d47e5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d47e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d47e5-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d47e5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d47e5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d47e5-124">INPUTS</span></span>

### <span data-ttu-id="d47e5-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d47e5-125">None</span></span>

## <span data-ttu-id="d47e5-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d47e5-126">OUTPUTS</span></span>

### <span data-ttu-id="d47e5-127">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d47e5-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="d47e5-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d47e5-128">NOTES</span></span>

## <span data-ttu-id="d47e5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d47e5-129">RELATED LINKS</span></span>
