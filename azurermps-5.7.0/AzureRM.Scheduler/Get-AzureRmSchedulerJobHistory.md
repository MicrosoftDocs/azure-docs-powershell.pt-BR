---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 6c1582c8e82bf344685f9e1feb002625bddd6748
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602513"
---
# <span data-ttu-id="a4123-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="a4123-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="a4123-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4123-102">SYNOPSIS</span></span>
<span data-ttu-id="a4123-103">Obtém o histórico de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a4123-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4123-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4123-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4123-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4123-105">DESCRIPTION</span></span>
<span data-ttu-id="a4123-106">O cmdlet **Get-AzureRmSchedulerJobHistory** Obtém o histórico de um trabalho do Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="a4123-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="a4123-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4123-107">EXAMPLES</span></span>

## <span data-ttu-id="a4123-108">OS</span><span class="sxs-lookup"><span data-stu-id="a4123-108">PARAMETERS</span></span>

### <span data-ttu-id="a4123-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4123-109">-DefaultProfile</span></span>
<span data-ttu-id="a4123-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4123-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4123-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a4123-111">-JobCollectionName</span></span>
<span data-ttu-id="a4123-112">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a4123-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="a4123-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="a4123-113">-JobExecutionStatus</span></span>
<span data-ttu-id="a4123-114">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a4123-114">Specifies the status of a job.</span></span>
<span data-ttu-id="a4123-115">Esse cmdlet obtém o histórico correspondente ao status especificado.</span><span class="sxs-lookup"><span data-stu-id="a4123-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="a4123-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a4123-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4123-117">Feito</span><span class="sxs-lookup"><span data-stu-id="a4123-117">Completed</span></span> 
- <span data-ttu-id="a4123-118">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="a4123-118">Failed</span></span> 
- <span data-ttu-id="a4123-119">Adiada</span><span class="sxs-lookup"><span data-stu-id="a4123-119">Postponed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4123-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="a4123-120">-JobName</span></span>
<span data-ttu-id="a4123-121">Especifica o nome de um trabalho para o qual esse cmdlet obtém histórico.</span><span class="sxs-lookup"><span data-stu-id="a4123-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="a4123-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4123-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4123-123">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="a4123-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a4123-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4123-124">CommonParameters</span></span>
<span data-ttu-id="a4123-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4123-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4123-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4123-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4123-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4123-127">INPUTS</span></span>

### <span data-ttu-id="a4123-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a4123-128">None</span></span>
<span data-ttu-id="a4123-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a4123-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4123-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4123-130">OUTPUTS</span></span>

### <span data-ttu-id="a4123-131">Microsoft. Azure. Commands. scheduler. Models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="a4123-131">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="a4123-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4123-132">NOTES</span></span>

## <span data-ttu-id="a4123-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4123-133">RELATED LINKS</span></span>

[<span data-ttu-id="a4123-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="a4123-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


