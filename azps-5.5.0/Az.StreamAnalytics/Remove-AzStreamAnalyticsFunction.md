---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112455"
---
# <span data-ttu-id="b6255-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b6255-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="b6255-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6255-102">SYNOPSIS</span></span>
<span data-ttu-id="b6255-103">Exclui uma função de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6255-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="b6255-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6255-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6255-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6255-105">DESCRIPTION</span></span>
<span data-ttu-id="b6255-106">O cmdlet **Remove-AzStreamAnalyticsFunction** exclui uma função assíncrona de um trabalho do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6255-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="b6255-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6255-107">EXAMPLES</span></span>

### <span data-ttu-id="b6255-108">Exemplo 1: Remover uma função Análise de Fluxo</span><span class="sxs-lookup"><span data-stu-id="b6255-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="b6255-109">Esse comando remove a função chamada ScoreTweet do trabalho chamado Stream Job22.</span><span class="sxs-lookup"><span data-stu-id="b6255-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="b6255-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6255-110">PARAMETERS</span></span>

### <span data-ttu-id="b6255-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6255-111">-DefaultProfile</span></span>
<span data-ttu-id="b6255-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b6255-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6255-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b6255-113">-JobName</span></span>
<span data-ttu-id="b6255-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="b6255-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="b6255-115">Este cmdlet remove uma função do trabalho especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b6255-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6255-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6255-116">-Name</span></span>
<span data-ttu-id="b6255-117">Especifica o nome da função Análise de Fluxo que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b6255-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6255-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6255-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6255-119">Especifica o nome do grupo de recursos ao qual uma função de Análise de Fluxo pertence.</span><span class="sxs-lookup"><span data-stu-id="b6255-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="b6255-120">Esse cmdlet exclui uma função no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b6255-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6255-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b6255-121">-Confirm</span></span>
<span data-ttu-id="b6255-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6255-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6255-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6255-123">-WhatIf</span></span>
<span data-ttu-id="b6255-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b6255-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6255-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6255-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6255-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6255-126">CommonParameters</span></span>
<span data-ttu-id="b6255-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6255-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6255-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6255-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6255-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6255-129">INPUTS</span></span>

### <span data-ttu-id="b6255-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b6255-130">System.String</span></span>

## <span data-ttu-id="b6255-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6255-131">OUTPUTS</span></span>

### <span data-ttu-id="b6255-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6255-132">System.Boolean</span></span>

## <span data-ttu-id="b6255-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b6255-133">NOTES</span></span>

## <span data-ttu-id="b6255-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6255-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6255-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b6255-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="b6255-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b6255-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="b6255-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b6255-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


