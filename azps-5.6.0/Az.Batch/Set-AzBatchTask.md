---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80fc0c530904717561aa34ca98844fede75e747e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890658"
---
# <span data-ttu-id="0a7ff-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0a7ff-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="0a7ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7ff-103">Atualiza as propriedades de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="0a7ff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0a7ff-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a7ff-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0a7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="0a7ff-106">O cmdlet **Set-AzBatchTask** atualiza as propriedades de uma tarefa no serviço Batch do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="0a7ff-107">Use o cmdlet Get-AzBatchTask para obter um **objeto PSCloudTask.**</span><span class="sxs-lookup"><span data-stu-id="0a7ff-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="0a7ff-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para comprometer suas alterações no serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="0a7ff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a7ff-109">EXAMPLES</span></span>

### <span data-ttu-id="0a7ff-110">Exemplo 1: atualizar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="0a7ff-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="0a7ff-111">O primeiro comando obtém uma tarefa usando **Get-AzBatchTask** e a armazena na variável $Task.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="0a7ff-112">Os dois comandos a seguir modificam as restrições da tarefa em $Task.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="0a7ff-113">O comando final atualiza o serviço Batch para corresponder ao objeto local $Task.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="0a7ff-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0a7ff-114">PARAMETERS</span></span>

### <span data-ttu-id="0a7ff-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0a7ff-115">-BatchContext</span></span>
<span data-ttu-id="0a7ff-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0a7ff-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0a7ff-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0a7ff-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0a7ff-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0a7ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7ff-121">-DefaultProfile</span></span>
<span data-ttu-id="0a7ff-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a7ff-123">-Task</span><span class="sxs-lookup"><span data-stu-id="0a7ff-123">-Task</span></span>
<span data-ttu-id="0a7ff-124">Especifica o **PSCloudTask ao** qual este cmdlet atualiza o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="0a7ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7ff-125">CommonParameters</span></span>
<span data-ttu-id="0a7ff-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7ff-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a7ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7ff-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a7ff-128">INPUTS</span></span>

### <span data-ttu-id="0a7ff-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0a7ff-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="0a7ff-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0a7ff-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0a7ff-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0a7ff-131">OUTPUTS</span></span>

### <span data-ttu-id="0a7ff-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="0a7ff-132">System.Void</span></span>

## <span data-ttu-id="0a7ff-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="0a7ff-133">NOTES</span></span>

## <span data-ttu-id="0a7ff-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a7ff-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a7ff-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0a7ff-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="0a7ff-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0a7ff-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0a7ff-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0a7ff-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="0a7ff-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0a7ff-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="0a7ff-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0a7ff-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="0a7ff-140">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="0a7ff-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
