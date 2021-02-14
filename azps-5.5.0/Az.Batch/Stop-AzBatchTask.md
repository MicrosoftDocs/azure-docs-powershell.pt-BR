---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116596"
---
# <span data-ttu-id="0cbc3-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0cbc3-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="0cbc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="0cbc3-103">Interrompe uma tarefa em lotes.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-103">Stops a Batch task.</span></span>

## <span data-ttu-id="0cbc3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cbc3-104">SYNTAX</span></span>

### <span data-ttu-id="0cbc3-105">Id</span><span class="sxs-lookup"><span data-stu-id="0cbc3-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cbc3-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0cbc3-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cbc3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cbc3-107">DESCRIPTION</span></span>
<span data-ttu-id="0cbc3-108">O **cmdlet Stop-AzBatchTask** interrompe uma tarefa do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="0cbc3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0cbc3-109">EXAMPLES</span></span>

### <span data-ttu-id="0cbc3-110">Exemplo 1: Excluir uma tarefa em lotes por ID</span><span class="sxs-lookup"><span data-stu-id="0cbc3-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="0cbc3-111">Esse comando interrompe uma tarefa que tem a Tarefa23 de ID sob o trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="0cbc3-112">O comando solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="0cbc3-113">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0cbc3-114">Exemplo 2: Interromper uma tarefa em lotes usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="0cbc3-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="0cbc3-115">Esse comando obtém a tarefa Lote que tem a Tarefa de ID26 no trabalho que tem o Trabalho de ID-000001 usando o cmdlet Get-AzBatchTask id.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="0cbc3-116">O comando passa essa tarefa para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0cbc3-117">O comando interrompe essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-117">The command stops that task.</span></span>

## <span data-ttu-id="0cbc3-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cbc3-118">PARAMETERS</span></span>

### <span data-ttu-id="0cbc3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0cbc3-119">-BatchContext</span></span>
<span data-ttu-id="0cbc3-120">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0cbc3-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0cbc3-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0cbc3-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0cbc3-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0cbc3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cbc3-125">-DefaultProfile</span></span>
<span data-ttu-id="0cbc3-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cbc3-127">-ID</span><span class="sxs-lookup"><span data-stu-id="0cbc3-127">-Id</span></span>
<span data-ttu-id="0cbc3-128">Especifica a ID da tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0cbc3-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="0cbc3-129">-JobId</span></span>
<span data-ttu-id="0cbc3-130">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="0cbc3-131">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="0cbc3-131">-Task</span></span>
<span data-ttu-id="0cbc3-132">Especifica a tarefa que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="0cbc3-133">Para obter um **objeto PSCloudTask,** use Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="0cbc3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cbc3-134">CommonParameters</span></span>
<span data-ttu-id="0cbc3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cbc3-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cbc3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cbc3-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="0cbc3-137">INPUTS</span></span>

### <span data-ttu-id="0cbc3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0cbc3-138">System.String</span></span>

### <span data-ttu-id="0cbc3-139">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0cbc3-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="0cbc3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0cbc3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0cbc3-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="0cbc3-141">OUTPUTS</span></span>

### <span data-ttu-id="0cbc3-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="0cbc3-142">System.Void</span></span>

## <span data-ttu-id="0cbc3-143">Notas</span><span class="sxs-lookup"><span data-stu-id="0cbc3-143">NOTES</span></span>

## <span data-ttu-id="0cbc3-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cbc3-144">RELATED LINKS</span></span>

[<span data-ttu-id="0cbc3-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0cbc3-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="0cbc3-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0cbc3-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="0cbc3-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0cbc3-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="0cbc3-148">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="0cbc3-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
