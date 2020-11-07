---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 7e9a7a5dbcb730bb5aa2be653b32ef4c9690e139
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93784976"
---
# <span data-ttu-id="c6284-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6284-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="c6284-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6284-102">SYNOPSIS</span></span>
<span data-ttu-id="c6284-103">Interrompe uma tarefa em lote.</span><span class="sxs-lookup"><span data-stu-id="c6284-103">Stops a Batch task.</span></span>

## <span data-ttu-id="c6284-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6284-104">SYNTAX</span></span>

### <span data-ttu-id="c6284-105">%</span><span class="sxs-lookup"><span data-stu-id="c6284-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6284-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c6284-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6284-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6284-107">DESCRIPTION</span></span>
<span data-ttu-id="c6284-108">O cmdlet **Stop-AzBatchTask** interrompe uma tarefa em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6284-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="c6284-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6284-109">EXAMPLES</span></span>

### <span data-ttu-id="c6284-110">Exemplo 1: excluir uma tarefa em lote por ID</span><span class="sxs-lookup"><span data-stu-id="c6284-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="c6284-111">Esse comando interrompe uma tarefa com a ID Task23 sob o trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="c6284-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c6284-112">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="c6284-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="c6284-113">Use o cmdlet Get-AzBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="c6284-113">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c6284-114">Exemplo 2: interromper uma tarefa em lote usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c6284-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="c6284-115">Esse comando obtém a tarefa em lotes que tem a ID Task26 no trabalho com o ID Job-000001 usando o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c6284-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="c6284-116">O comando transmite essa tarefa para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6284-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c6284-117">O comando interrompe a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c6284-117">The command stops that task.</span></span>

## <span data-ttu-id="c6284-118">OS</span><span class="sxs-lookup"><span data-stu-id="c6284-118">PARAMETERS</span></span>

### <span data-ttu-id="c6284-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c6284-119">-BatchContext</span></span>
<span data-ttu-id="c6284-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c6284-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c6284-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c6284-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c6284-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="c6284-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c6284-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c6284-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c6284-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c6284-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c6284-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6284-125">-DefaultProfile</span></span>
<span data-ttu-id="c6284-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6284-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6284-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c6284-127">-Id</span></span>
<span data-ttu-id="c6284-128">Especifica a ID da tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="c6284-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c6284-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="c6284-129">-JobId</span></span>
<span data-ttu-id="c6284-130">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c6284-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="c6284-131">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="c6284-131">-Task</span></span>
<span data-ttu-id="c6284-132">Especifica a tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="c6284-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="c6284-133">Para obter um objeto **PSCloudTask** , use o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c6284-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="c6284-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6284-134">CommonParameters</span></span>
<span data-ttu-id="c6284-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6284-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6284-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6284-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6284-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6284-137">INPUTS</span></span>

### <span data-ttu-id="c6284-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c6284-138">System.String</span></span>

### <span data-ttu-id="c6284-139">Microsoft.Azure.Commands.Batch. Modelos. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c6284-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="c6284-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c6284-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c6284-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6284-141">OUTPUTS</span></span>

### <span data-ttu-id="c6284-142">System. void</span><span class="sxs-lookup"><span data-stu-id="c6284-142">System.Void</span></span>

## <span data-ttu-id="c6284-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6284-143">NOTES</span></span>

## <span data-ttu-id="c6284-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6284-144">RELATED LINKS</span></span>

[<span data-ttu-id="c6284-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6284-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="c6284-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6284-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="c6284-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6284-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="c6284-148">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c6284-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


