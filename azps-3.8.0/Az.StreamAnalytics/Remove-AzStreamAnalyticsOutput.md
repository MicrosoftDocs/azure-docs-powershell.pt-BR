---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777493"
---
# <span data-ttu-id="4ab43-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4ab43-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="4ab43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ab43-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab43-103">Exclui uma saída de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4ab43-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="4ab43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ab43-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab43-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ab43-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab43-106">O cmdlet **Remove-AzStreamAnalyticsOutput** exclui de forma assíncrona uma saída de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab43-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="4ab43-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ab43-107">EXAMPLES</span></span>

### <span data-ttu-id="4ab43-108">EXEMPLO 1: remover uma saída de um trabalho</span><span class="sxs-lookup"><span data-stu-id="4ab43-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="4ab43-109">Esse comando Remove a saída de saída no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="4ab43-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="4ab43-110">OS</span><span class="sxs-lookup"><span data-stu-id="4ab43-110">PARAMETERS</span></span>

### <span data-ttu-id="4ab43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab43-111">-DefaultProfile</span></span>
<span data-ttu-id="4ab43-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab43-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ab43-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="4ab43-113">-JobName</span></span>
<span data-ttu-id="4ab43-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="4ab43-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="4ab43-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ab43-115">-Name</span></span>
<span data-ttu-id="4ab43-116">Especifica o nome da saída do Azure Stream Analytics a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4ab43-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="4ab43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab43-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ab43-118">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="4ab43-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="4ab43-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ab43-119">-Confirm</span></span>
<span data-ttu-id="4ab43-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ab43-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab43-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab43-121">-WhatIf</span></span>
<span data-ttu-id="4ab43-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ab43-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab43-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ab43-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab43-124">CommonParameters</span></span>
<span data-ttu-id="4ab43-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab43-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab43-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab43-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ab43-127">INPUTS</span></span>

### <span data-ttu-id="4ab43-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab43-128">System.String</span></span>

## <span data-ttu-id="4ab43-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ab43-129">OUTPUTS</span></span>

### <span data-ttu-id="4ab43-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ab43-130">System.Boolean</span></span>

## <span data-ttu-id="4ab43-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ab43-131">NOTES</span></span>

## <span data-ttu-id="4ab43-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ab43-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ab43-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4ab43-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="4ab43-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4ab43-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="4ab43-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4ab43-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


