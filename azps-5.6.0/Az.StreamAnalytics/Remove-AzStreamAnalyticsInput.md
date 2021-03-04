---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: 2e0443976d36339c9866c08118ef08c37fafac48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888113"
---
# <span data-ttu-id="42f34-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42f34-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="42f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f34-102">SYNOPSIS</span></span>
<span data-ttu-id="42f34-103">Exclui uma entrada de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42f34-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="42f34-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42f34-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f34-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42f34-105">DESCRIPTION</span></span>
<span data-ttu-id="42f34-106">O cmdlet **Remove-AzStreamAnalyticsInput** exclui de forma assíncrona uma entrada de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="42f34-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="42f34-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42f34-107">EXAMPLES</span></span>

### <span data-ttu-id="42f34-108">EXEMPLO 1: Remover um fluxo de entrada de um trabalho</span><span class="sxs-lookup"><span data-stu-id="42f34-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="42f34-109">Este comando remove a entrada EventStream do StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="42f34-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="42f34-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42f34-110">PARAMETERS</span></span>

### <span data-ttu-id="42f34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f34-111">-DefaultProfile</span></span>
<span data-ttu-id="42f34-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="42f34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f34-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="42f34-113">-JobName</span></span>
<span data-ttu-id="42f34-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="42f34-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="42f34-115">-Name</span><span class="sxs-lookup"><span data-stu-id="42f34-115">-Name</span></span>
<span data-ttu-id="42f34-116">Especifica o nome da entrada do Azure Stream Analytics a ser removido.</span><span class="sxs-lookup"><span data-stu-id="42f34-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="42f34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f34-117">-ResourceGroupName</span></span>
<span data-ttu-id="42f34-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="42f34-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="42f34-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42f34-119">-Confirm</span></span>
<span data-ttu-id="42f34-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42f34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f34-121">-WhatIf</span></span>
<span data-ttu-id="42f34-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42f34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f34-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42f34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f34-124">CommonParameters</span></span>
<span data-ttu-id="42f34-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f34-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f34-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f34-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42f34-127">INPUTS</span></span>

### <span data-ttu-id="42f34-128">System.String</span><span class="sxs-lookup"><span data-stu-id="42f34-128">System.String</span></span>

## <span data-ttu-id="42f34-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42f34-129">OUTPUTS</span></span>

### <span data-ttu-id="42f34-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42f34-130">System.Boolean</span></span>

## <span data-ttu-id="42f34-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="42f34-131">NOTES</span></span>

## <span data-ttu-id="42f34-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42f34-132">RELATED LINKS</span></span>

[<span data-ttu-id="42f34-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42f34-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="42f34-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42f34-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="42f34-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="42f34-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


