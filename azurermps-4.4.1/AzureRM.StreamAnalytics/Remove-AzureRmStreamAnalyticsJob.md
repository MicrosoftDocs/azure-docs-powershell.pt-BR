---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 9ba839bbfc6740d9d62c9a036d233a8b5a1ce0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440152"
---
# <span data-ttu-id="d1323-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1323-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="d1323-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1323-102">SYNOPSIS</span></span>
<span data-ttu-id="d1323-103">Remove um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d1323-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1323-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1323-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1323-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1323-105">DESCRIPTION</span></span>
<span data-ttu-id="d1323-106">O cmdlet **Remove-AzureRmStreamAnalyticsJob** exclui de forma assíncrona um trabalho específico do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="d1323-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="d1323-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1323-107">EXAMPLES</span></span>

### <span data-ttu-id="d1323-108">EXEMPLO 1: remover um trabalho</span><span class="sxs-lookup"><span data-stu-id="d1323-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="d1323-109">Esse comando Remove o job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d1323-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="d1323-110">OS</span><span class="sxs-lookup"><span data-stu-id="d1323-110">PARAMETERS</span></span>

### <span data-ttu-id="d1323-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1323-111">-Name</span></span>
<span data-ttu-id="d1323-112">Especifica o nome do trabalho do Azure Stream Analytics a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d1323-112">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="d1323-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1323-113">-ResourceGroupName</span></span>
<span data-ttu-id="d1323-114">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="d1323-114">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="d1323-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1323-115">-Confirm</span></span>
<span data-ttu-id="d1323-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1323-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1323-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1323-117">-WhatIf</span></span>
<span data-ttu-id="d1323-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1323-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1323-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1323-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1323-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1323-120">-DefaultProfile</span></span>
<span data-ttu-id="d1323-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1323-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1323-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1323-122">CommonParameters</span></span>
<span data-ttu-id="d1323-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1323-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1323-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1323-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1323-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1323-125">INPUTS</span></span>

## <span data-ttu-id="d1323-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1323-126">OUTPUTS</span></span>

### <span data-ttu-id="d1323-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="d1323-127">System.Object</span></span>

## <span data-ttu-id="d1323-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1323-128">NOTES</span></span>

## <span data-ttu-id="d1323-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1323-129">RELATED LINKS</span></span>

[<span data-ttu-id="d1323-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1323-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1323-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1323-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1323-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1323-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1323-133">Parar-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1323-133">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


