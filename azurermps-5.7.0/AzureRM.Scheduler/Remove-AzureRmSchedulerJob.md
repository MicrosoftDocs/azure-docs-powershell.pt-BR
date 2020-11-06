---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: de8f9e05cbec17d6a92f3c4e567bd5dce96005ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431615"
---
# <span data-ttu-id="0bda6-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="0bda6-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="0bda6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bda6-102">SYNOPSIS</span></span>
<span data-ttu-id="0bda6-103">Remove um trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="0bda6-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bda6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bda6-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bda6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bda6-105">DESCRIPTION</span></span>
<span data-ttu-id="0bda6-106">O cmdlet **Remove-AzureRmSchedulerJob** remove um trabalho do Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bda6-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="0bda6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bda6-107">EXAMPLES</span></span>

## <span data-ttu-id="0bda6-108">OS</span><span class="sxs-lookup"><span data-stu-id="0bda6-108">PARAMETERS</span></span>

### <span data-ttu-id="0bda6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bda6-109">-DefaultProfile</span></span>
<span data-ttu-id="0bda6-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bda6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bda6-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0bda6-111">-JobCollectionName</span></span>
<span data-ttu-id="0bda6-112">Especifica o nome de uma coleção de trabalho que contém o trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0bda6-112">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="0bda6-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0bda6-113">-JobName</span></span>
<span data-ttu-id="0bda6-114">Especifica o nome de um trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0bda6-114">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="0bda6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bda6-115">-PassThru</span></span>
<span data-ttu-id="0bda6-116">Indica que esse cmdlet retorna um valor Success em Success.</span><span class="sxs-lookup"><span data-stu-id="0bda6-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="0bda6-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0bda6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bda6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bda6-118">-ResourceGroupName</span></span>
<span data-ttu-id="0bda6-119">Especifica o grupo de recursos do trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0bda6-119">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="0bda6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0bda6-120">-Confirm</span></span>
<span data-ttu-id="0bda6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bda6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bda6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bda6-122">-WhatIf</span></span>
<span data-ttu-id="0bda6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0bda6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bda6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0bda6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bda6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bda6-125">CommonParameters</span></span>
<span data-ttu-id="0bda6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bda6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bda6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bda6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bda6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bda6-128">INPUTS</span></span>

### <span data-ttu-id="0bda6-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0bda6-129">None</span></span>
<span data-ttu-id="0bda6-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0bda6-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0bda6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bda6-131">OUTPUTS</span></span>

## <span data-ttu-id="0bda6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bda6-132">NOTES</span></span>

## <span data-ttu-id="0bda6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bda6-133">RELATED LINKS</span></span>

[<span data-ttu-id="0bda6-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="0bda6-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


