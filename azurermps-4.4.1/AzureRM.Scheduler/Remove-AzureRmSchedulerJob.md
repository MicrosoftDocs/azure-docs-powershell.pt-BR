---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 582953886b8ea39e04dee122c85d70884dabcf11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430652"
---
# <span data-ttu-id="e44c6-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e44c6-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="e44c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e44c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e44c6-103">Remove um trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="e44c6-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e44c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e44c6-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e44c6-105">DESCRIPTION</span></span>
<span data-ttu-id="e44c6-106">O cmdlet **Remove-AzureRmSchedulerJob** remove um trabalho do Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="e44c6-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="e44c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e44c6-107">EXAMPLES</span></span>

## <span data-ttu-id="e44c6-108">OS</span><span class="sxs-lookup"><span data-stu-id="e44c6-108">PARAMETERS</span></span>

### <span data-ttu-id="e44c6-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e44c6-109">-JobCollectionName</span></span>
<span data-ttu-id="e44c6-110">Especifica o nome de uma coleção de trabalho que contém o trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e44c6-110">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="e44c6-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="e44c6-111">-JobName</span></span>
<span data-ttu-id="e44c6-112">Especifica o nome de um trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e44c6-112">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="e44c6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e44c6-113">-PassThru</span></span>
<span data-ttu-id="e44c6-114">Indica que esse cmdlet retorna um valor Success em Success.</span><span class="sxs-lookup"><span data-stu-id="e44c6-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="e44c6-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e44c6-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e44c6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44c6-116">-ResourceGroupName</span></span>
<span data-ttu-id="e44c6-117">Especifica o grupo de recursos do trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e44c6-117">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="e44c6-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e44c6-118">-Confirm</span></span>
<span data-ttu-id="e44c6-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e44c6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44c6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44c6-120">-WhatIf</span></span>
<span data-ttu-id="e44c6-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e44c6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44c6-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e44c6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44c6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44c6-123">-DefaultProfile</span></span>
<span data-ttu-id="e44c6-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e44c6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e44c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44c6-125">CommonParameters</span></span>
<span data-ttu-id="e44c6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44c6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44c6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e44c6-128">INPUTS</span></span>

## <span data-ttu-id="e44c6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e44c6-129">OUTPUTS</span></span>

## <span data-ttu-id="e44c6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e44c6-130">NOTES</span></span>

## <span data-ttu-id="e44c6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e44c6-131">RELATED LINKS</span></span>

[<span data-ttu-id="e44c6-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e44c6-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


