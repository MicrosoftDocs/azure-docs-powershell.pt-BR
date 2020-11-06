---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 1a977578b278c51d8e66b0f502ba12fbac39e810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428356"
---
# <span data-ttu-id="221b1-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="221b1-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="221b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="221b1-102">SYNOPSIS</span></span>
<span data-ttu-id="221b1-103">Remove uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="221b1-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="221b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="221b1-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="221b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="221b1-105">DESCRIPTION</span></span>
<span data-ttu-id="221b1-106">O cmdlet **Remove-AzureRmSchedulerJobCollection** remove uma coleção de trabalhos do Azure scheduler.</span><span class="sxs-lookup"><span data-stu-id="221b1-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="221b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="221b1-107">EXAMPLES</span></span>

## <span data-ttu-id="221b1-108">OS</span><span class="sxs-lookup"><span data-stu-id="221b1-108">PARAMETERS</span></span>

### <span data-ttu-id="221b1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="221b1-109">-DefaultProfile</span></span>
<span data-ttu-id="221b1-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="221b1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="221b1-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="221b1-111">-JobCollectionName</span></span>
<span data-ttu-id="221b1-112">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="221b1-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="221b1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="221b1-113">-PassThru</span></span>
<span data-ttu-id="221b1-114">Indica que esse cmdlet retorna um valor Success em Success.</span><span class="sxs-lookup"><span data-stu-id="221b1-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="221b1-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="221b1-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="221b1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="221b1-116">-ResourceGroupName</span></span>
<span data-ttu-id="221b1-117">Especifica o grupo de recursos da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="221b1-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="221b1-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="221b1-118">-Confirm</span></span>
<span data-ttu-id="221b1-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="221b1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="221b1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="221b1-120">-WhatIf</span></span>
<span data-ttu-id="221b1-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="221b1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="221b1-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="221b1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="221b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="221b1-123">CommonParameters</span></span>
<span data-ttu-id="221b1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="221b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="221b1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="221b1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="221b1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="221b1-126">INPUTS</span></span>

### <span data-ttu-id="221b1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="221b1-127">System.String</span></span>

## <span data-ttu-id="221b1-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="221b1-128">OUTPUTS</span></span>

### <span data-ttu-id="221b1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="221b1-129">System.String</span></span>

## <span data-ttu-id="221b1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="221b1-130">NOTES</span></span>

## <span data-ttu-id="221b1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="221b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="221b1-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="221b1-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="221b1-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="221b1-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="221b1-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="221b1-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="221b1-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="221b1-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="221b1-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="221b1-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

