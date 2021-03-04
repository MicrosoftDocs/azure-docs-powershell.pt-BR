---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 231b9250509ed463f7f9b2a2d9563dbb1e378ee0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888688"
---
# <span data-ttu-id="6ddc6-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6ddc6-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="6ddc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ddc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddc6-103">Cria um objeto do tipo Agenda</span><span class="sxs-lookup"><span data-stu-id="6ddc6-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="6ddc6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ddc6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ddc6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ddc6-105">DESCRIPTION</span></span>
<span data-ttu-id="6ddc6-106">Cria um objeto do tipo Agenda.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="6ddc6-107">Esse objeto deve ser passado para o comando que cria a Regra de Alerta de Log.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="6ddc6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ddc6-108">EXAMPLES</span></span>

### <span data-ttu-id="6ddc6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ddc6-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="6ddc6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ddc6-110">PARAMETERS</span></span>

### <span data-ttu-id="6ddc6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddc6-111">-DefaultProfile</span></span>
<span data-ttu-id="6ddc6-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ddc6-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="6ddc6-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="6ddc6-114">A frequência de alerta</span><span class="sxs-lookup"><span data-stu-id="6ddc6-114">The alert frequency</span></span>

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

### <span data-ttu-id="6ddc6-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="6ddc6-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="6ddc6-116">A janela de tempo de alerta</span><span class="sxs-lookup"><span data-stu-id="6ddc6-116">The alert time window</span></span>

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

### <span data-ttu-id="6ddc6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddc6-117">CommonParameters</span></span>
<span data-ttu-id="6ddc6-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddc6-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ddc6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddc6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ddc6-120">INPUTS</span></span>

### <span data-ttu-id="6ddc6-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6ddc6-121">None</span></span>

## <span data-ttu-id="6ddc6-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ddc6-122">OUTPUTS</span></span>

### <span data-ttu-id="6ddc6-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6ddc6-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="6ddc6-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ddc6-124">NOTES</span></span>

## <span data-ttu-id="6ddc6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ddc6-125">RELATED LINKS</span></span>
