---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 950d761324f0750f2433b0b88edb5d37859945e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889388"
---
# <span data-ttu-id="b956a-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b956a-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b956a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b956a-102">SYNOPSIS</span></span>
<span data-ttu-id="b956a-103">Exclui uma saída de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b956a-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="b956a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b956a-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b956a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b956a-105">DESCRIPTION</span></span>
<span data-ttu-id="b956a-106">O cmdlet **Remove-AzStreamAnalyticsOutput** exclui de forma assíncrona uma saída de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="b956a-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b956a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b956a-107">EXAMPLES</span></span>

### <span data-ttu-id="b956a-108">EXEMPLO 1: Remover uma saída de um trabalho</span><span class="sxs-lookup"><span data-stu-id="b956a-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b956a-109">Este comando remove a saída Saída no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b956a-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="b956a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b956a-110">PARAMETERS</span></span>

### <span data-ttu-id="b956a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b956a-111">-DefaultProfile</span></span>
<span data-ttu-id="b956a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b956a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b956a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b956a-113">-JobName</span></span>
<span data-ttu-id="b956a-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="b956a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b956a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b956a-115">-Name</span></span>
<span data-ttu-id="b956a-116">Especifica o nome da saída do Azure Stream Analytics a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b956a-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="b956a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b956a-117">-ResourceGroupName</span></span>
<span data-ttu-id="b956a-118">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="b956a-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b956a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b956a-119">-Confirm</span></span>
<span data-ttu-id="b956a-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b956a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b956a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b956a-121">-WhatIf</span></span>
<span data-ttu-id="b956a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b956a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b956a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b956a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b956a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b956a-124">CommonParameters</span></span>
<span data-ttu-id="b956a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b956a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b956a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b956a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b956a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b956a-127">INPUTS</span></span>

### <span data-ttu-id="b956a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b956a-128">System.String</span></span>

## <span data-ttu-id="b956a-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b956a-129">OUTPUTS</span></span>

### <span data-ttu-id="b956a-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b956a-130">System.Boolean</span></span>

## <span data-ttu-id="b956a-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b956a-131">NOTES</span></span>

## <span data-ttu-id="b956a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b956a-132">RELATED LINKS</span></span>

[<span data-ttu-id="b956a-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b956a-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="b956a-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b956a-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="b956a-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b956a-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


