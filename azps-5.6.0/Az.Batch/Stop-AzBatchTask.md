---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 5550603bc4204937e8568b50b739ef8b8fadba14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886362"
---
# <span data-ttu-id="cef15-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cef15-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="cef15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef15-102">SYNOPSIS</span></span>
<span data-ttu-id="cef15-103">Interrompe uma tarefa Batch.</span><span class="sxs-lookup"><span data-stu-id="cef15-103">Stops a Batch task.</span></span>

## <span data-ttu-id="cef15-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cef15-104">SYNTAX</span></span>

### <span data-ttu-id="cef15-105">Id</span><span class="sxs-lookup"><span data-stu-id="cef15-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cef15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cef15-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cef15-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cef15-107">DESCRIPTION</span></span>
<span data-ttu-id="cef15-108">O cmdlet **Stop-AzBatchTask** interrompe uma tarefa do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="cef15-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="cef15-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cef15-109">EXAMPLES</span></span>

### <span data-ttu-id="cef15-110">Exemplo 1: Excluir uma tarefa em lotes por ID</span><span class="sxs-lookup"><span data-stu-id="cef15-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="cef15-111">Este comando interrompe uma tarefa que tem a ID Task23 no trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="cef15-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="cef15-112">O comando solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="cef15-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="cef15-113">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="cef15-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cef15-114">Exemplo 2: interromper uma tarefa em lotes usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="cef15-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="cef15-115">Este comando obtém a tarefa Batch que tem a ID Task26 no trabalho que tem a ID Job-000001 usando o cmdlet Get-AzBatchTask ID.</span><span class="sxs-lookup"><span data-stu-id="cef15-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="cef15-116">O comando passa essa tarefa para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="cef15-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cef15-117">O comando interrompe essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="cef15-117">The command stops that task.</span></span>

## <span data-ttu-id="cef15-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cef15-118">PARAMETERS</span></span>

### <span data-ttu-id="cef15-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cef15-119">-BatchContext</span></span>
<span data-ttu-id="cef15-120">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="cef15-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cef15-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="cef15-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cef15-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="cef15-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cef15-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef15-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cef15-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cef15-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cef15-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef15-125">-DefaultProfile</span></span>
<span data-ttu-id="cef15-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cef15-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cef15-127">-Id</span><span class="sxs-lookup"><span data-stu-id="cef15-127">-Id</span></span>
<span data-ttu-id="cef15-128">Especifica a ID da tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="cef15-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="cef15-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="cef15-129">-JobId</span></span>
<span data-ttu-id="cef15-130">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="cef15-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="cef15-131">-Task</span><span class="sxs-lookup"><span data-stu-id="cef15-131">-Task</span></span>
<span data-ttu-id="cef15-132">Especifica a tarefa que esse cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="cef15-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="cef15-133">Para obter um **objeto PSCloudTask,** use o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="cef15-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="cef15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef15-134">CommonParameters</span></span>
<span data-ttu-id="cef15-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef15-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cef15-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef15-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cef15-137">INPUTS</span></span>

### <span data-ttu-id="cef15-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cef15-138">System.String</span></span>

### <span data-ttu-id="cef15-139">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="cef15-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="cef15-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cef15-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cef15-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cef15-141">OUTPUTS</span></span>

### <span data-ttu-id="cef15-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="cef15-142">System.Void</span></span>

## <span data-ttu-id="cef15-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="cef15-143">NOTES</span></span>

## <span data-ttu-id="cef15-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cef15-144">RELATED LINKS</span></span>

[<span data-ttu-id="cef15-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cef15-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="cef15-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cef15-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="cef15-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cef15-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="cef15-148">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="cef15-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
