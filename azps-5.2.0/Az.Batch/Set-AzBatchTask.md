---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259890"
---
# <span data-ttu-id="51894-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="51894-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="51894-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51894-102">SYNOPSIS</span></span>
<span data-ttu-id="51894-103">Atualiza as propriedades de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="51894-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="51894-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51894-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51894-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51894-105">DESCRIPTION</span></span>
<span data-ttu-id="51894-106">O cmdlet **set-AzBatchTask** atualiza as propriedades de uma tarefa no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="51894-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="51894-107">Use o cmdlet Get-AzBatchTask para obter um objeto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="51894-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="51894-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="51894-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="51894-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51894-109">EXAMPLES</span></span>

### <span data-ttu-id="51894-110">Exemplo 1: atualizar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="51894-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="51894-111">O primeiro comando obtém uma tarefa usando **Get-AzBatchTask** e, em seguida, armazena-a na variável $Task.</span><span class="sxs-lookup"><span data-stu-id="51894-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="51894-112">Os próximos dois comandos modificam as restrições da tarefa em $Task.</span><span class="sxs-lookup"><span data-stu-id="51894-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="51894-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Task.</span><span class="sxs-lookup"><span data-stu-id="51894-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="51894-114">OS</span><span class="sxs-lookup"><span data-stu-id="51894-114">PARAMETERS</span></span>

### <span data-ttu-id="51894-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="51894-115">-BatchContext</span></span>
<span data-ttu-id="51894-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="51894-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="51894-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="51894-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="51894-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="51894-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="51894-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="51894-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="51894-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="51894-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="51894-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51894-121">-DefaultProfile</span></span>
<span data-ttu-id="51894-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51894-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51894-123">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="51894-123">-Task</span></span>
<span data-ttu-id="51894-124">Especifica o **PSCloudTask** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="51894-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="51894-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51894-125">CommonParameters</span></span>
<span data-ttu-id="51894-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51894-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51894-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51894-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51894-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51894-128">INPUTS</span></span>

### <span data-ttu-id="51894-129">Microsoft.Azure.Commands.Batch. Modelos. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="51894-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="51894-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="51894-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="51894-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51894-131">OUTPUTS</span></span>

### <span data-ttu-id="51894-132">System. void</span><span class="sxs-lookup"><span data-stu-id="51894-132">System.Void</span></span>

## <span data-ttu-id="51894-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51894-133">NOTES</span></span>

## <span data-ttu-id="51894-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51894-134">RELATED LINKS</span></span>

[<span data-ttu-id="51894-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="51894-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="51894-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="51894-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="51894-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="51894-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="51894-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="51894-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="51894-139">Parar-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="51894-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="51894-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="51894-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
