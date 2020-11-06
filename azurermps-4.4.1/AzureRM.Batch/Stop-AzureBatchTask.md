---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432248"
---
# <span data-ttu-id="50e93-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="50e93-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="50e93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50e93-102">SYNOPSIS</span></span>
<span data-ttu-id="50e93-103">Interrompe uma tarefa em lote.</span><span class="sxs-lookup"><span data-stu-id="50e93-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50e93-104">SYNTAX</span></span>

### <span data-ttu-id="50e93-105">%</span><span class="sxs-lookup"><span data-stu-id="50e93-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e93-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="50e93-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e93-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50e93-107">DESCRIPTION</span></span>
<span data-ttu-id="50e93-108">O cmdlet **Stop-AzureBatchTask** interrompe uma tarefa em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="50e93-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="50e93-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50e93-109">EXAMPLES</span></span>

### <span data-ttu-id="50e93-110">Exemplo 1: excluir uma tarefa em lote por ID</span><span class="sxs-lookup"><span data-stu-id="50e93-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="50e93-111">Esse comando interrompe uma tarefa com a ID Task23 sob o trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="50e93-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="50e93-112">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="50e93-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="50e93-113">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="50e93-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="50e93-114">Exemplo 2: interromper uma tarefa em lote usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="50e93-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="50e93-115">Esse comando obtém a tarefa em lotes que tem a ID Task26 no trabalho com o ID Job-000001 usando o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="50e93-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="50e93-116">O comando transmite essa tarefa para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="50e93-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50e93-117">O comando interrompe a tarefa.</span><span class="sxs-lookup"><span data-stu-id="50e93-117">The command stops that task.</span></span>

## <span data-ttu-id="50e93-118">OS</span><span class="sxs-lookup"><span data-stu-id="50e93-118">PARAMETERS</span></span>

### <span data-ttu-id="50e93-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50e93-119">-BatchContext</span></span>
<span data-ttu-id="50e93-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="50e93-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50e93-121">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="50e93-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="50e93-122">-ID</span><span class="sxs-lookup"><span data-stu-id="50e93-122">-Id</span></span>
<span data-ttu-id="50e93-123">Especifica a ID da tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="50e93-123">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50e93-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="50e93-124">-JobId</span></span>
<span data-ttu-id="50e93-125">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="50e93-125">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50e93-126">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="50e93-126">-Task</span></span>
<span data-ttu-id="50e93-127">Especifica a tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="50e93-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="50e93-128">Para obter um objeto **PSCloudTask** , use o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="50e93-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50e93-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e93-129">-DefaultProfile</span></span>
<span data-ttu-id="50e93-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50e93-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50e93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e93-131">CommonParameters</span></span>
<span data-ttu-id="50e93-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e93-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e93-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50e93-134">INPUTS</span></span>

### <span data-ttu-id="50e93-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50e93-135">BatchAccountContext</span></span>
<span data-ttu-id="50e93-136">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="50e93-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="50e93-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="50e93-137">PSCloudTask</span></span>
<span data-ttu-id="50e93-138">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="50e93-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="50e93-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50e93-139">OUTPUTS</span></span>

## <span data-ttu-id="50e93-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50e93-140">NOTES</span></span>

## <span data-ttu-id="50e93-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50e93-141">RELATED LINKS</span></span>

[<span data-ttu-id="50e93-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="50e93-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="50e93-143">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="50e93-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="50e93-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="50e93-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="50e93-145">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="50e93-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


