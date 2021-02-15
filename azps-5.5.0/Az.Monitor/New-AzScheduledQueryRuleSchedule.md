---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117515"
---
# <span data-ttu-id="a08f8-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a08f8-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="a08f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a08f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a08f8-103">Cria um objeto do tipo Agenda</span><span class="sxs-lookup"><span data-stu-id="a08f8-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="a08f8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a08f8-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a08f8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a08f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a08f8-106">Cria um objeto do tipo Agenda.</span><span class="sxs-lookup"><span data-stu-id="a08f8-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="a08f8-107">Esse objeto deve ser passado para o comando que cria a Regra de Alerta de Log.</span><span class="sxs-lookup"><span data-stu-id="a08f8-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="a08f8-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a08f8-108">EXAMPLES</span></span>

### <span data-ttu-id="a08f8-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a08f8-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="a08f8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a08f8-110">PARAMETERS</span></span>

### <span data-ttu-id="a08f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08f8-111">-DefaultProfile</span></span>
<span data-ttu-id="a08f8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a08f8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08f8-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a08f8-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="a08f8-114">A frequência de alerta</span><span class="sxs-lookup"><span data-stu-id="a08f8-114">The alert frequency</span></span>

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

### <span data-ttu-id="a08f8-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="a08f8-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="a08f8-116">A janela de tempo de alerta</span><span class="sxs-lookup"><span data-stu-id="a08f8-116">The alert time window</span></span>

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

### <span data-ttu-id="a08f8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08f8-117">CommonParameters</span></span>
<span data-ttu-id="a08f8-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a08f8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08f8-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a08f8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08f8-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="a08f8-120">INPUTS</span></span>

### <span data-ttu-id="a08f8-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a08f8-121">None</span></span>

## <span data-ttu-id="a08f8-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="a08f8-122">OUTPUTS</span></span>

### <span data-ttu-id="a08f8-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a08f8-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="a08f8-124">Notas</span><span class="sxs-lookup"><span data-stu-id="a08f8-124">NOTES</span></span>

## <span data-ttu-id="a08f8-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a08f8-125">RELATED LINKS</span></span>
