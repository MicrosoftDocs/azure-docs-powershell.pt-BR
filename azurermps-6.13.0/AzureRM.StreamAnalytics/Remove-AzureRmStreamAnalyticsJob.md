---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430802"
---
# <span data-ttu-id="5b002-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5b002-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="5b002-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b002-102">SYNOPSIS</span></span>
<span data-ttu-id="5b002-103">Remove um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5b002-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b002-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b002-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b002-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b002-105">DESCRIPTION</span></span>
<span data-ttu-id="5b002-106">O cmdlet **Remove-AzureRmStreamAnalyticsJob** exclui de forma assíncrona um trabalho específico do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="5b002-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="5b002-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b002-107">EXAMPLES</span></span>

### <span data-ttu-id="5b002-108">EXEMPLO 1: remover um trabalho</span><span class="sxs-lookup"><span data-stu-id="5b002-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="5b002-109">Esse comando Remove o job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5b002-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="5b002-110">OS</span><span class="sxs-lookup"><span data-stu-id="5b002-110">PARAMETERS</span></span>

### <span data-ttu-id="5b002-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b002-111">-DefaultProfile</span></span>
<span data-ttu-id="5b002-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b002-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b002-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b002-113">-Name</span></span>
<span data-ttu-id="5b002-114">Especifica o nome do trabalho do Azure Stream Analytics a ser removido.</span><span class="sxs-lookup"><span data-stu-id="5b002-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="5b002-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b002-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b002-116">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="5b002-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="5b002-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b002-117">-Confirm</span></span>
<span data-ttu-id="5b002-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b002-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b002-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b002-119">-WhatIf</span></span>
<span data-ttu-id="5b002-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b002-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b002-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b002-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b002-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b002-122">CommonParameters</span></span>
<span data-ttu-id="5b002-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b002-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b002-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b002-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b002-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b002-125">INPUTS</span></span>

### <span data-ttu-id="5b002-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5b002-126">System.String</span></span>

## <span data-ttu-id="5b002-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b002-127">OUTPUTS</span></span>

### <span data-ttu-id="5b002-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b002-128">System.Boolean</span></span>

## <span data-ttu-id="5b002-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b002-129">NOTES</span></span>

## <span data-ttu-id="5b002-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b002-130">RELATED LINKS</span></span>

[<span data-ttu-id="5b002-131">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5b002-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5b002-132">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5b002-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5b002-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5b002-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="5b002-134">Parar-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5b002-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


