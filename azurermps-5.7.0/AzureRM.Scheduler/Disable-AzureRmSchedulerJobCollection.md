---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: c754b7e30fdec3a179beefdf48292a781ec083db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429680"
---
# <span data-ttu-id="998e7-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="998e7-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="998e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="998e7-102">SYNOPSIS</span></span>
<span data-ttu-id="998e7-103">Desabilita uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="998e7-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="998e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="998e7-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="998e7-105">DESCRIPTION</span></span>
<span data-ttu-id="998e7-106">O cmdlet **Disable-AzureRmSchedulerJobCollection** desabilita uma coleção de trabalhos no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="998e7-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="998e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="998e7-107">EXAMPLES</span></span>

## <span data-ttu-id="998e7-108">OS</span><span class="sxs-lookup"><span data-stu-id="998e7-108">PARAMETERS</span></span>

### <span data-ttu-id="998e7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998e7-109">-DefaultProfile</span></span>
<span data-ttu-id="998e7-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="998e7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e7-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="998e7-111">-JobCollectionName</span></span>
<span data-ttu-id="998e7-112">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="998e7-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998e7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="998e7-113">-PassThru</span></span>
<span data-ttu-id="998e7-114">Indica que esse cmdlet retorna um valor Success em Success.</span><span class="sxs-lookup"><span data-stu-id="998e7-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="998e7-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="998e7-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998e7-116">-ResourceGroupName</span></span>
<span data-ttu-id="998e7-117">Especifica o grupo de recursos da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="998e7-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998e7-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="998e7-118">-Confirm</span></span>
<span data-ttu-id="998e7-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="998e7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998e7-120">-WhatIf</span></span>
<span data-ttu-id="998e7-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="998e7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998e7-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="998e7-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998e7-123">CommonParameters</span></span>
<span data-ttu-id="998e7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998e7-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998e7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998e7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="998e7-126">INPUTS</span></span>

### <span data-ttu-id="998e7-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="998e7-127">None</span></span>
<span data-ttu-id="998e7-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="998e7-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="998e7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="998e7-129">OUTPUTS</span></span>

## <span data-ttu-id="998e7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="998e7-130">NOTES</span></span>

## <span data-ttu-id="998e7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="998e7-131">RELATED LINKS</span></span>

[<span data-ttu-id="998e7-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="998e7-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="998e7-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="998e7-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="998e7-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="998e7-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="998e7-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="998e7-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="998e7-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="998e7-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

