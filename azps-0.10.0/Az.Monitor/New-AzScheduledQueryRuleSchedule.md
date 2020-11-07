---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: e62c8861f370f9e7e7c5b31fea629f3f8e11aa32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775695"
---
# <span data-ttu-id="d2257-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d2257-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d2257-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2257-102">SYNOPSIS</span></span>
<span data-ttu-id="d2257-103">Cria um objeto do tipo cronograma</span><span class="sxs-lookup"><span data-stu-id="d2257-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="d2257-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2257-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2257-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2257-105">DESCRIPTION</span></span>
<span data-ttu-id="d2257-106">Cria um objeto do tipo cronograma.</span><span class="sxs-lookup"><span data-stu-id="d2257-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="d2257-107">Esse objeto deve ser passado para o comando que cria a regra de alerta de log.</span><span class="sxs-lookup"><span data-stu-id="d2257-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="d2257-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2257-108">EXAMPLES</span></span>

### <span data-ttu-id="d2257-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2257-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="d2257-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2257-110">PARAMETERS</span></span>

### <span data-ttu-id="d2257-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2257-111">-DefaultProfile</span></span>
<span data-ttu-id="d2257-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2257-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2257-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d2257-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="d2257-114">A frequência do alerta</span><span class="sxs-lookup"><span data-stu-id="d2257-114">The alert frequency</span></span>

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

### <span data-ttu-id="d2257-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="d2257-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="d2257-116">A janela de tempo de alerta</span><span class="sxs-lookup"><span data-stu-id="d2257-116">The alert time window</span></span>

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

### <span data-ttu-id="d2257-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2257-117">CommonParameters</span></span>
<span data-ttu-id="d2257-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2257-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2257-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2257-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2257-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2257-120">INPUTS</span></span>

### <span data-ttu-id="d2257-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d2257-121">None</span></span>

## <span data-ttu-id="d2257-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2257-122">OUTPUTS</span></span>

### <span data-ttu-id="d2257-123">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d2257-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d2257-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2257-124">NOTES</span></span>

## <span data-ttu-id="d2257-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2257-125">RELATED LINKS</span></span>
