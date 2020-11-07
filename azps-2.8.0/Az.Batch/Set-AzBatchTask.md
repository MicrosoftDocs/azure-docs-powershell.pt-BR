---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: b49ab8a6a08802ec670fb605e707ae46c51ddab2
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785085"
---
# <span data-ttu-id="91753-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="91753-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="91753-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91753-102">SYNOPSIS</span></span>
<span data-ttu-id="91753-103">Atualiza as propriedades de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="91753-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="91753-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91753-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91753-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91753-105">DESCRIPTION</span></span>
<span data-ttu-id="91753-106">O cmdlet **set-AzBatchTask** atualiza as propriedades de uma tarefa no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="91753-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="91753-107">Use o cmdlet Get-AzBatchTask para obter um objeto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="91753-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="91753-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="91753-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="91753-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91753-109">EXAMPLES</span></span>

### <span data-ttu-id="91753-110">Exemplo 1: atualizar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="91753-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="91753-111">O primeiro comando obtém uma tarefa usando **Get-AzBatchTask** e, em seguida, armazena-a na variável $Task.</span><span class="sxs-lookup"><span data-stu-id="91753-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="91753-112">Os próximos dois comandos modificam as restrições da tarefa em $Task.</span><span class="sxs-lookup"><span data-stu-id="91753-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="91753-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Task.</span><span class="sxs-lookup"><span data-stu-id="91753-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="91753-114">OS</span><span class="sxs-lookup"><span data-stu-id="91753-114">PARAMETERS</span></span>

### <span data-ttu-id="91753-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="91753-115">-BatchContext</span></span>
<span data-ttu-id="91753-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="91753-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="91753-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="91753-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="91753-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="91753-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="91753-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="91753-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="91753-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="91753-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="91753-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91753-121">-DefaultProfile</span></span>
<span data-ttu-id="91753-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91753-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91753-123">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="91753-123">-Task</span></span>
<span data-ttu-id="91753-124">Especifica o **PSCloudTask** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="91753-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="91753-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91753-125">CommonParameters</span></span>
<span data-ttu-id="91753-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91753-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91753-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91753-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91753-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91753-128">INPUTS</span></span>

### <span data-ttu-id="91753-129">Microsoft.Azure.Commands.Batch. Modelos. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="91753-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="91753-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="91753-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="91753-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91753-131">OUTPUTS</span></span>

### <span data-ttu-id="91753-132">System. void</span><span class="sxs-lookup"><span data-stu-id="91753-132">System.Void</span></span>

## <span data-ttu-id="91753-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91753-133">NOTES</span></span>

## <span data-ttu-id="91753-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91753-134">RELATED LINKS</span></span>

[<span data-ttu-id="91753-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="91753-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="91753-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="91753-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="91753-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="91753-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="91753-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="91753-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="91753-139">Parar-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="91753-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="91753-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="91753-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


