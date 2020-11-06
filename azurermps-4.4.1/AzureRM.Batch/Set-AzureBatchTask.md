---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440210"
---
# <span data-ttu-id="99642-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="99642-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="99642-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99642-102">SYNOPSIS</span></span>
<span data-ttu-id="99642-103">Atualiza as propriedades de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="99642-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99642-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99642-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99642-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99642-105">DESCRIPTION</span></span>
<span data-ttu-id="99642-106">O cmdlet **set-AzureBatchTask** atualiza as propriedades de uma tarefa no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="99642-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="99642-107">Use o cmdlet Get-AzureBatchTask para obter um objeto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="99642-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="99642-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="99642-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="99642-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99642-109">EXAMPLES</span></span>

### <span data-ttu-id="99642-110">Exemplo 1: atualizar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="99642-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="99642-111">O primeiro comando obtém uma tarefa usando **Get-AzureBatchTask** e, em seguida, armazena-a na variável $Task.</span><span class="sxs-lookup"><span data-stu-id="99642-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="99642-112">Os próximos dois comandos modificam as restrições da tarefa em $Task.</span><span class="sxs-lookup"><span data-stu-id="99642-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="99642-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Task.</span><span class="sxs-lookup"><span data-stu-id="99642-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="99642-114">OS</span><span class="sxs-lookup"><span data-stu-id="99642-114">PARAMETERS</span></span>

### <span data-ttu-id="99642-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99642-115">-BatchContext</span></span>
<span data-ttu-id="99642-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="99642-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99642-117">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="99642-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99642-118">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="99642-118">-Task</span></span>
<span data-ttu-id="99642-119">Especifica o **PSCloudTask** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="99642-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99642-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99642-120">-DefaultProfile</span></span>
<span data-ttu-id="99642-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99642-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99642-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99642-122">CommonParameters</span></span>
<span data-ttu-id="99642-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99642-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99642-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99642-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99642-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99642-125">INPUTS</span></span>

### <span data-ttu-id="99642-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99642-126">BatchAccountContext</span></span>
<span data-ttu-id="99642-127">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="99642-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="99642-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="99642-128">PSCloudTask</span></span>
<span data-ttu-id="99642-129">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="99642-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="99642-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99642-130">OUTPUTS</span></span>

## <span data-ttu-id="99642-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99642-131">NOTES</span></span>

## <span data-ttu-id="99642-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99642-132">RELATED LINKS</span></span>

[<span data-ttu-id="99642-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="99642-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="99642-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="99642-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="99642-135">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="99642-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="99642-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="99642-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="99642-137">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="99642-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="99642-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="99642-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


