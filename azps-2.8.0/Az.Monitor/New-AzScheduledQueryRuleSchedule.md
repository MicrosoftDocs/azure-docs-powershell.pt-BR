---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 2043a2cf31354c7fc14b1b03794dff6f82af67b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772176"
---
# <span data-ttu-id="090ae-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="090ae-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="090ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="090ae-102">SYNOPSIS</span></span>
<span data-ttu-id="090ae-103">Cria um objeto do tipo cronograma</span><span class="sxs-lookup"><span data-stu-id="090ae-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="090ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="090ae-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="090ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="090ae-105">DESCRIPTION</span></span>
<span data-ttu-id="090ae-106">Cria um objeto do tipo cronograma.</span><span class="sxs-lookup"><span data-stu-id="090ae-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="090ae-107">Esse objeto deve ser passado para o comando que cria a regra de alerta de log.</span><span class="sxs-lookup"><span data-stu-id="090ae-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="090ae-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="090ae-108">EXAMPLES</span></span>

### <span data-ttu-id="090ae-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="090ae-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="090ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="090ae-110">PARAMETERS</span></span>

### <span data-ttu-id="090ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090ae-111">-DefaultProfile</span></span>
<span data-ttu-id="090ae-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="090ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="090ae-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="090ae-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="090ae-114">A frequência do alerta</span><span class="sxs-lookup"><span data-stu-id="090ae-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090ae-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="090ae-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="090ae-116">A janela de tempo de alerta</span><span class="sxs-lookup"><span data-stu-id="090ae-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090ae-117">CommonParameters</span></span>
<span data-ttu-id="090ae-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="090ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090ae-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="090ae-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090ae-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="090ae-120">INPUTS</span></span>

### <span data-ttu-id="090ae-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="090ae-121">None</span></span>

## <span data-ttu-id="090ae-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="090ae-122">OUTPUTS</span></span>

### <span data-ttu-id="090ae-123">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="090ae-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="090ae-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="090ae-124">NOTES</span></span>

## <span data-ttu-id="090ae-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="090ae-125">RELATED LINKS</span></span>
