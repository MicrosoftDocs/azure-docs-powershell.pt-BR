---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263521"
---
# <span data-ttu-id="b981e-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b981e-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="b981e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b981e-102">SYNOPSIS</span></span>
<span data-ttu-id="b981e-103">Remove um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b981e-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="b981e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b981e-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b981e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b981e-105">DESCRIPTION</span></span>
<span data-ttu-id="b981e-106">O cmdlet **Remove-AzStreamAnalyticsJob** exclui de forma assíncrona um trabalho específico do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="b981e-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b981e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b981e-107">EXAMPLES</span></span>

### <span data-ttu-id="b981e-108">EXEMPLO 1: remover um trabalho</span><span class="sxs-lookup"><span data-stu-id="b981e-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="b981e-109">Esse comando Remove o job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b981e-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="b981e-110">OS</span><span class="sxs-lookup"><span data-stu-id="b981e-110">PARAMETERS</span></span>

### <span data-ttu-id="b981e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b981e-111">-DefaultProfile</span></span>
<span data-ttu-id="b981e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b981e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b981e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b981e-113">-Name</span></span>
<span data-ttu-id="b981e-114">Especifica o nome do trabalho do Azure Stream Analytics a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b981e-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="b981e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b981e-115">-ResourceGroupName</span></span>
<span data-ttu-id="b981e-116">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="b981e-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="b981e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b981e-117">-Confirm</span></span>
<span data-ttu-id="b981e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b981e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b981e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b981e-119">-WhatIf</span></span>
<span data-ttu-id="b981e-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b981e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b981e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b981e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b981e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b981e-122">CommonParameters</span></span>
<span data-ttu-id="b981e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b981e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b981e-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b981e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b981e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b981e-125">INPUTS</span></span>

### <span data-ttu-id="b981e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b981e-126">System.String</span></span>

## <span data-ttu-id="b981e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b981e-127">OUTPUTS</span></span>

### <span data-ttu-id="b981e-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b981e-128">System.Boolean</span></span>

## <span data-ttu-id="b981e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b981e-129">NOTES</span></span>

## <span data-ttu-id="b981e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b981e-130">RELATED LINKS</span></span>

[<span data-ttu-id="b981e-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b981e-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b981e-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b981e-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b981e-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b981e-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b981e-134">Parar-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b981e-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


