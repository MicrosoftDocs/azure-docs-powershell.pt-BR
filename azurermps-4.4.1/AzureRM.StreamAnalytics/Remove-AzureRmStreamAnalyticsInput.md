---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440155"
---
# <span data-ttu-id="bd418-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bd418-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="bd418-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd418-102">SYNOPSIS</span></span>
<span data-ttu-id="bd418-103">Exclui uma entrada de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd418-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd418-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd418-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd418-105">DESCRIPTION</span></span>
<span data-ttu-id="bd418-106">O cmdlet **Remove-AzureRmStreamAnalyticsInput** exclui de forma assíncrona uma entrada de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="bd418-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="bd418-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd418-107">EXAMPLES</span></span>

### <span data-ttu-id="bd418-108">EXEMPLO 1: remover um fluxo de entrada de um trabalho</span><span class="sxs-lookup"><span data-stu-id="bd418-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="bd418-109">Esse comando Remove a entrada EventStream do StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bd418-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="bd418-110">OS</span><span class="sxs-lookup"><span data-stu-id="bd418-110">PARAMETERS</span></span>

### <span data-ttu-id="bd418-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="bd418-111">-JobName</span></span>
<span data-ttu-id="bd418-112">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="bd418-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="bd418-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd418-113">-Name</span></span>
<span data-ttu-id="bd418-114">Especifica o nome da entrada do Azure Stream Analytics a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bd418-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="bd418-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd418-115">-ResourceGroupName</span></span>
<span data-ttu-id="bd418-116">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="bd418-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="bd418-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd418-117">-Confirm</span></span>
<span data-ttu-id="bd418-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd418-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd418-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd418-119">-WhatIf</span></span>
<span data-ttu-id="bd418-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd418-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd418-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd418-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd418-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd418-122">-DefaultProfile</span></span>
<span data-ttu-id="bd418-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd418-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd418-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd418-124">CommonParameters</span></span>
<span data-ttu-id="bd418-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd418-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd418-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd418-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd418-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd418-127">INPUTS</span></span>

## <span data-ttu-id="bd418-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd418-128">OUTPUTS</span></span>

### <span data-ttu-id="bd418-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="bd418-129">System.Object</span></span>

## <span data-ttu-id="bd418-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd418-130">NOTES</span></span>

## <span data-ttu-id="bd418-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd418-131">RELATED LINKS</span></span>

[<span data-ttu-id="bd418-132">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bd418-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="bd418-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bd418-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="bd418-134">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bd418-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


