---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 98074a9893525882ce63ab86e31c677281f34ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427120"
---
# <span data-ttu-id="818ab-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="818ab-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="818ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="818ab-102">SYNOPSIS</span></span>
<span data-ttu-id="818ab-103">Exclui uma saída de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="818ab-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="818ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="818ab-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="818ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="818ab-105">DESCRIPTION</span></span>
<span data-ttu-id="818ab-106">O cmdlet **Remove-AzureRmStreamAnalyticsOutput** exclui de forma assíncrona uma saída de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="818ab-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="818ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="818ab-107">EXAMPLES</span></span>

### <span data-ttu-id="818ab-108">EXEMPLO 1: remover uma saída de um trabalho</span><span class="sxs-lookup"><span data-stu-id="818ab-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="818ab-109">Esse comando Remove a saída de saída no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="818ab-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="818ab-110">OS</span><span class="sxs-lookup"><span data-stu-id="818ab-110">PARAMETERS</span></span>

### <span data-ttu-id="818ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="818ab-111">-DefaultProfile</span></span>
<span data-ttu-id="818ab-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="818ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="818ab-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="818ab-113">-JobName</span></span>
<span data-ttu-id="818ab-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="818ab-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="818ab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="818ab-115">-Name</span></span>
<span data-ttu-id="818ab-116">Especifica o nome da saída do Azure Stream Analytics a ser removida.</span><span class="sxs-lookup"><span data-stu-id="818ab-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="818ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="818ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="818ab-118">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="818ab-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="818ab-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="818ab-119">-Confirm</span></span>
<span data-ttu-id="818ab-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="818ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="818ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="818ab-121">-WhatIf</span></span>
<span data-ttu-id="818ab-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="818ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="818ab-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="818ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="818ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="818ab-124">CommonParameters</span></span>
<span data-ttu-id="818ab-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="818ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="818ab-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="818ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="818ab-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="818ab-127">INPUTS</span></span>

### <span data-ttu-id="818ab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="818ab-128">System.String</span></span>

## <span data-ttu-id="818ab-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="818ab-129">OUTPUTS</span></span>

### <span data-ttu-id="818ab-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="818ab-130">System.Boolean</span></span>

## <span data-ttu-id="818ab-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="818ab-131">NOTES</span></span>

## <span data-ttu-id="818ab-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="818ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="818ab-133">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="818ab-133">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="818ab-134">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="818ab-134">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="818ab-135">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="818ab-135">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)

