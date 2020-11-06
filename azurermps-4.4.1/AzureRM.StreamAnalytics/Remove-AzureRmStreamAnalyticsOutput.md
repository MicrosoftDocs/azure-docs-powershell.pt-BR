---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602183"
---
# <span data-ttu-id="f1367-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1367-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f1367-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1367-102">SYNOPSIS</span></span>
<span data-ttu-id="f1367-103">Exclui uma saída de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f1367-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1367-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1367-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1367-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1367-105">DESCRIPTION</span></span>
<span data-ttu-id="f1367-106">O cmdlet **Remove-AzureRmStreamAnalyticsOutput** exclui de forma assíncrona uma saída de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="f1367-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f1367-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1367-107">EXAMPLES</span></span>

### <span data-ttu-id="f1367-108">EXEMPLO 1: remover uma saída de um trabalho</span><span class="sxs-lookup"><span data-stu-id="f1367-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f1367-109">Esse comando Remove a saída de saída no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f1367-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="f1367-110">OS</span><span class="sxs-lookup"><span data-stu-id="f1367-110">PARAMETERS</span></span>

### <span data-ttu-id="f1367-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1367-111">-JobName</span></span>
<span data-ttu-id="f1367-112">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="f1367-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f1367-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1367-113">-Name</span></span>
<span data-ttu-id="f1367-114">Especifica o nome da saída do Azure Stream Analytics a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f1367-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="f1367-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1367-115">-ResourceGroupName</span></span>
<span data-ttu-id="f1367-116">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="f1367-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f1367-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1367-117">-Confirm</span></span>
<span data-ttu-id="f1367-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1367-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1367-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1367-119">-WhatIf</span></span>
<span data-ttu-id="f1367-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1367-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1367-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1367-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1367-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1367-122">-DefaultProfile</span></span>
<span data-ttu-id="f1367-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1367-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1367-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1367-124">CommonParameters</span></span>
<span data-ttu-id="f1367-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1367-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1367-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1367-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1367-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1367-127">INPUTS</span></span>

## <span data-ttu-id="f1367-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1367-128">OUTPUTS</span></span>

### <span data-ttu-id="f1367-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="f1367-129">System.Object</span></span>

## <span data-ttu-id="f1367-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1367-130">NOTES</span></span>

## <span data-ttu-id="f1367-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1367-131">RELATED LINKS</span></span>

[<span data-ttu-id="f1367-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1367-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f1367-133">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1367-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f1367-134">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1367-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


