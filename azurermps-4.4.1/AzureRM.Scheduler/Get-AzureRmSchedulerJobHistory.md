---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 7eec69a441efbf1a4d9f73e85a0385c24a012e34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433014"
---
# <span data-ttu-id="22a26-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="22a26-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="22a26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22a26-102">SYNOPSIS</span></span>
<span data-ttu-id="22a26-103">Obtém o histórico de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22a26-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22a26-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22a26-105">DESCRIPTION</span></span>
<span data-ttu-id="22a26-106">O cmdlet **Get-AzureRmSchedulerJobHistory** Obtém o histórico de um trabalho do Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="22a26-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="22a26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22a26-107">EXAMPLES</span></span>

## <span data-ttu-id="22a26-108">OS</span><span class="sxs-lookup"><span data-stu-id="22a26-108">PARAMETERS</span></span>

### <span data-ttu-id="22a26-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="22a26-109">-JobCollectionName</span></span>
<span data-ttu-id="22a26-110">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="22a26-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="22a26-111">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="22a26-111">-JobExecutionStatus</span></span>
<span data-ttu-id="22a26-112">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="22a26-112">Specifies the status of a job.</span></span>
<span data-ttu-id="22a26-113">Esse cmdlet obtém o histórico correspondente ao status especificado.</span><span class="sxs-lookup"><span data-stu-id="22a26-113">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="22a26-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="22a26-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22a26-115">Feito</span><span class="sxs-lookup"><span data-stu-id="22a26-115">Completed</span></span> 
- <span data-ttu-id="22a26-116">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="22a26-116">Failed</span></span> 
- <span data-ttu-id="22a26-117">Adiada</span><span class="sxs-lookup"><span data-stu-id="22a26-117">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a26-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="22a26-118">-JobName</span></span>
<span data-ttu-id="22a26-119">Especifica o nome de um trabalho para o qual esse cmdlet obtém histórico.</span><span class="sxs-lookup"><span data-stu-id="22a26-119">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="22a26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a26-120">-ResourceGroupName</span></span>
<span data-ttu-id="22a26-121">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="22a26-121">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="22a26-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a26-122">-DefaultProfile</span></span>
<span data-ttu-id="22a26-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22a26-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a26-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a26-124">CommonParameters</span></span>
<span data-ttu-id="22a26-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a26-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a26-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a26-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a26-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22a26-127">INPUTS</span></span>

## <span data-ttu-id="22a26-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22a26-128">OUTPUTS</span></span>

### <span data-ttu-id="22a26-129">Microsoft. Azure. Commands. scheduler. Models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="22a26-129">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="22a26-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22a26-130">NOTES</span></span>

## <span data-ttu-id="22a26-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22a26-131">RELATED LINKS</span></span>

[<span data-ttu-id="22a26-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="22a26-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


