---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: d76b1139955490189aeb9c2269cc4e9ede8197be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431527"
---
# <span data-ttu-id="1bb9e-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1bb9e-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1bb9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bb9e-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb9e-103">Exclui uma função de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bb9e-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bb9e-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb9e-106">O cmdlet **Remove-AzureRmStreamAnalyticsFunction** exclui uma função de forma assíncrona de um trabalho do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="1bb9e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bb9e-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb9e-108">Exemplo 1: remover uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="1bb9e-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="1bb9e-109">Esse comando Remove a função denominada ScoreTweet do trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="1bb9e-110">OS</span><span class="sxs-lookup"><span data-stu-id="1bb9e-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb9e-111">-DefaultProfile</span></span>
<span data-ttu-id="1bb9e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb9e-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1bb9e-113">-JobName</span></span>
<span data-ttu-id="1bb9e-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="1bb9e-115">Esse cmdlet Remove uma função do trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb9e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bb9e-116">-Name</span></span>
<span data-ttu-id="1bb9e-117">Especifica o nome da função do Stream Analytics que o cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb9e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb9e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1bb9e-119">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="1bb9e-120">Esse cmdlet exclui uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb9e-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1bb9e-121">-Confirm</span></span>
<span data-ttu-id="1bb9e-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb9e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb9e-123">-WhatIf</span></span>
<span data-ttu-id="1bb9e-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb9e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb9e-126">CommonParameters</span></span>
<span data-ttu-id="1bb9e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb9e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb9e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bb9e-129">INPUTS</span></span>

### <span data-ttu-id="1bb9e-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1bb9e-130">None</span></span>
<span data-ttu-id="1bb9e-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1bb9e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1bb9e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bb9e-132">OUTPUTS</span></span>

### <span data-ttu-id="1bb9e-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="1bb9e-133">System.Object</span></span>

## <span data-ttu-id="1bb9e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bb9e-134">NOTES</span></span>

## <span data-ttu-id="1bb9e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bb9e-135">RELATED LINKS</span></span>

[<span data-ttu-id="1bb9e-136">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1bb9e-136">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="1bb9e-137">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1bb9e-137">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="1bb9e-138">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1bb9e-138">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


