---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112453"
---
# <span data-ttu-id="600f6-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="600f6-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="600f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="600f6-102">SYNOPSIS</span></span>
<span data-ttu-id="600f6-103">Exclui uma entrada de um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="600f6-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="600f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="600f6-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600f6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="600f6-105">DESCRIPTION</span></span>
<span data-ttu-id="600f6-106">O cmdlet **Remove-AzStreamAnalyticsInput** exclui assíncronamente uma entrada de um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="600f6-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="600f6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="600f6-107">EXAMPLES</span></span>

### <span data-ttu-id="600f6-108">EXEMPLO 1: Remover um fluxo de entrada de um trabalho</span><span class="sxs-lookup"><span data-stu-id="600f6-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="600f6-109">Esse comando remove a entrada EventStream do StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="600f6-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="600f6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="600f6-110">PARAMETERS</span></span>

### <span data-ttu-id="600f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600f6-111">-DefaultProfile</span></span>
<span data-ttu-id="600f6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="600f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="600f6-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="600f6-113">-JobName</span></span>
<span data-ttu-id="600f6-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="600f6-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="600f6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="600f6-115">-Name</span></span>
<span data-ttu-id="600f6-116">Especifica o nome da entrada do Azure Stream Analytics para remover.</span><span class="sxs-lookup"><span data-stu-id="600f6-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="600f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="600f6-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="600f6-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="600f6-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="600f6-119">-Confirm</span></span>
<span data-ttu-id="600f6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="600f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600f6-121">-WhatIf</span></span>
<span data-ttu-id="600f6-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="600f6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600f6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="600f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600f6-124">CommonParameters</span></span>
<span data-ttu-id="600f6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600f6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600f6-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="600f6-127">INPUTS</span></span>

### <span data-ttu-id="600f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="600f6-128">System.String</span></span>

## <span data-ttu-id="600f6-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="600f6-129">OUTPUTS</span></span>

### <span data-ttu-id="600f6-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="600f6-130">System.Boolean</span></span>

## <span data-ttu-id="600f6-131">Notas</span><span class="sxs-lookup"><span data-stu-id="600f6-131">NOTES</span></span>

## <span data-ttu-id="600f6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="600f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="600f6-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="600f6-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="600f6-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="600f6-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="600f6-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="600f6-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


