---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283958"
---
# <span data-ttu-id="53814-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53814-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="53814-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53814-102">SYNOPSIS</span></span>
<span data-ttu-id="53814-103">Exclui uma função de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53814-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="53814-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53814-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53814-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53814-105">DESCRIPTION</span></span>
<span data-ttu-id="53814-106">O cmdlet **Remove-AzStreamAnalyticsFunction** exclui uma função de forma assíncrona de um trabalho do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53814-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="53814-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53814-107">EXAMPLES</span></span>

### <span data-ttu-id="53814-108">Exemplo 1: remover uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="53814-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="53814-109">Esse comando Remove a função denominada ScoreTweet do trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="53814-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="53814-110">OS</span><span class="sxs-lookup"><span data-stu-id="53814-110">PARAMETERS</span></span>

### <span data-ttu-id="53814-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53814-111">-DefaultProfile</span></span>
<span data-ttu-id="53814-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53814-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53814-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="53814-113">-JobName</span></span>
<span data-ttu-id="53814-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="53814-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="53814-115">Esse cmdlet Remove uma função do trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="53814-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="53814-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="53814-116">-Name</span></span>
<span data-ttu-id="53814-117">Especifica o nome da função do Stream Analytics que o cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="53814-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="53814-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53814-118">-ResourceGroupName</span></span>
<span data-ttu-id="53814-119">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="53814-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="53814-120">Esse cmdlet exclui uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="53814-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53814-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53814-121">-Confirm</span></span>
<span data-ttu-id="53814-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53814-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53814-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53814-123">-WhatIf</span></span>
<span data-ttu-id="53814-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53814-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53814-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53814-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53814-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53814-126">CommonParameters</span></span>
<span data-ttu-id="53814-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53814-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53814-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53814-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53814-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53814-129">INPUTS</span></span>

### <span data-ttu-id="53814-130">System. String</span><span class="sxs-lookup"><span data-stu-id="53814-130">System.String</span></span>

## <span data-ttu-id="53814-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53814-131">OUTPUTS</span></span>

### <span data-ttu-id="53814-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53814-132">System.Boolean</span></span>

## <span data-ttu-id="53814-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53814-133">NOTES</span></span>

## <span data-ttu-id="53814-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53814-134">RELATED LINKS</span></span>

[<span data-ttu-id="53814-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53814-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="53814-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53814-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="53814-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53814-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


