---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1a500f883b6896e91767f0f7d560ee28e4bfc9f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888112"
---
# <span data-ttu-id="83549-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83549-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="83549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83549-102">SYNOPSIS</span></span>
<span data-ttu-id="83549-103">Exclui uma função de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="83549-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="83549-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="83549-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83549-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="83549-105">DESCRIPTION</span></span>
<span data-ttu-id="83549-106">O cmdlet **Remove-AzStreamAnalyticsFunction** exclui uma função de forma assíncrona de um trabalho do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="83549-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="83549-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83549-107">EXAMPLES</span></span>

### <span data-ttu-id="83549-108">Exemplo 1: Remover uma função de Análise de Fluxo</span><span class="sxs-lookup"><span data-stu-id="83549-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="83549-109">Este comando remove a função denominada ScoreTweet do trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="83549-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="83549-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="83549-110">PARAMETERS</span></span>

### <span data-ttu-id="83549-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83549-111">-DefaultProfile</span></span>
<span data-ttu-id="83549-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="83549-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83549-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="83549-113">-JobName</span></span>
<span data-ttu-id="83549-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="83549-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="83549-115">Este cmdlet remove uma função do trabalho especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="83549-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="83549-116">-Name</span><span class="sxs-lookup"><span data-stu-id="83549-116">-Name</span></span>
<span data-ttu-id="83549-117">Especifica o nome da função Stream Analytics que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="83549-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83549-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83549-118">-ResourceGroupName</span></span>
<span data-ttu-id="83549-119">Especifica o nome do grupo de recursos ao qual pertence uma função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="83549-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="83549-120">Este cmdlet exclui uma função no grupo de recursos que este parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="83549-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="83549-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83549-121">-Confirm</span></span>
<span data-ttu-id="83549-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83549-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83549-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83549-123">-WhatIf</span></span>
<span data-ttu-id="83549-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83549-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83549-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83549-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83549-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83549-126">CommonParameters</span></span>
<span data-ttu-id="83549-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83549-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83549-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83549-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83549-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83549-129">INPUTS</span></span>

### <span data-ttu-id="83549-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83549-130">System.String</span></span>

## <span data-ttu-id="83549-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="83549-131">OUTPUTS</span></span>

### <span data-ttu-id="83549-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83549-132">System.Boolean</span></span>

## <span data-ttu-id="83549-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="83549-133">NOTES</span></span>

## <span data-ttu-id="83549-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83549-134">RELATED LINKS</span></span>

[<span data-ttu-id="83549-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83549-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="83549-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83549-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="83549-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83549-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


