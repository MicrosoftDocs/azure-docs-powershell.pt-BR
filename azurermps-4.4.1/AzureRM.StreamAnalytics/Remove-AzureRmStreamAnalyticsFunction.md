---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 10687094bcbbc6cc9a52e648d830d46eac089c4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440156"
---
# <span data-ttu-id="2c9f9-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c9f9-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="2c9f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9f9-103">Exclui uma função de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c9f9-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c9f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9f9-106">O cmdlet **Remove-AzureRmStreamAnalyticsFunction** exclui uma função de forma assíncrona de um trabalho do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="2c9f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c9f9-107">EXAMPLES</span></span>

### <span data-ttu-id="2c9f9-108">Exemplo 1: remover uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2c9f9-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="2c9f9-109">Esse comando Remove a função denominada ScoreTweet do trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="2c9f9-110">OS</span><span class="sxs-lookup"><span data-stu-id="2c9f9-110">PARAMETERS</span></span>

### <span data-ttu-id="2c9f9-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="2c9f9-111">-JobName</span></span>
<span data-ttu-id="2c9f9-112">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="2c9f9-113">Esse cmdlet Remove uma função do trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-113">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c9f9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c9f9-114">-Name</span></span>
<span data-ttu-id="2c9f9-115">Especifica o nome da função do Stream Analytics que o cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-115">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c9f9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9f9-116">-ResourceGroupName</span></span>
<span data-ttu-id="2c9f9-117">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-117">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="2c9f9-118">Esse cmdlet exclui uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-118">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c9f9-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c9f9-119">-Confirm</span></span>
<span data-ttu-id="2c9f9-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c9f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9f9-121">-WhatIf</span></span>
<span data-ttu-id="2c9f9-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9f9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c9f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f9-124">-DefaultProfile</span></span>
<span data-ttu-id="2c9f9-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9f9-126">CommonParameters</span></span>
<span data-ttu-id="2c9f9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9f9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9f9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9f9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c9f9-129">INPUTS</span></span>

## <span data-ttu-id="2c9f9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c9f9-130">OUTPUTS</span></span>

### <span data-ttu-id="2c9f9-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="2c9f9-131">System.Object</span></span>

## <span data-ttu-id="2c9f9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c9f9-132">NOTES</span></span>

## <span data-ttu-id="2c9f9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c9f9-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c9f9-134">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c9f9-134">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="2c9f9-135">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c9f9-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="2c9f9-136">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c9f9-136">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)

