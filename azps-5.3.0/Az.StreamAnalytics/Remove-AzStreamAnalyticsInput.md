---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272475"
---
# <span data-ttu-id="24c35-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="24c35-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="24c35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24c35-102">SYNOPSIS</span></span>
<span data-ttu-id="24c35-103">Exclui uma entrada de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="24c35-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="24c35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24c35-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24c35-105">DESCRIPTION</span></span>
<span data-ttu-id="24c35-106">O cmdlet **Remove-AzStreamAnalyticsInput** exclui de forma assíncrona uma entrada de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="24c35-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="24c35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24c35-107">EXAMPLES</span></span>

### <span data-ttu-id="24c35-108">EXEMPLO 1: remover um fluxo de entrada de um trabalho</span><span class="sxs-lookup"><span data-stu-id="24c35-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="24c35-109">Esse comando Remove a entrada EventStream do StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="24c35-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="24c35-110">OS</span><span class="sxs-lookup"><span data-stu-id="24c35-110">PARAMETERS</span></span>

### <span data-ttu-id="24c35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c35-111">-DefaultProfile</span></span>
<span data-ttu-id="24c35-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24c35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c35-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="24c35-113">-JobName</span></span>
<span data-ttu-id="24c35-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="24c35-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="24c35-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="24c35-115">-Name</span></span>
<span data-ttu-id="24c35-116">Especifica o nome da entrada do Azure Stream Analytics a ser removida.</span><span class="sxs-lookup"><span data-stu-id="24c35-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="24c35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c35-117">-ResourceGroupName</span></span>
<span data-ttu-id="24c35-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="24c35-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="24c35-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24c35-119">-Confirm</span></span>
<span data-ttu-id="24c35-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c35-121">-WhatIf</span></span>
<span data-ttu-id="24c35-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24c35-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c35-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24c35-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c35-124">CommonParameters</span></span>
<span data-ttu-id="24c35-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c35-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c35-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24c35-127">INPUTS</span></span>

### <span data-ttu-id="24c35-128">System. String</span><span class="sxs-lookup"><span data-stu-id="24c35-128">System.String</span></span>

## <span data-ttu-id="24c35-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24c35-129">OUTPUTS</span></span>

### <span data-ttu-id="24c35-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24c35-130">System.Boolean</span></span>

## <span data-ttu-id="24c35-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24c35-131">NOTES</span></span>

## <span data-ttu-id="24c35-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24c35-132">RELATED LINKS</span></span>

[<span data-ttu-id="24c35-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="24c35-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="24c35-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="24c35-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="24c35-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="24c35-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


