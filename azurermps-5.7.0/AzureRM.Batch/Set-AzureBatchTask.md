---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: 6e6bb12aeb5b5d319b0997578991c87e91c81003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430524"
---
# <span data-ttu-id="a41d5-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a41d5-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="a41d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a41d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a41d5-103">Atualiza as propriedades de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="a41d5-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a41d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a41d5-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a41d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a41d5-105">DESCRIPTION</span></span>
<span data-ttu-id="a41d5-106">O cmdlet **set-AzureBatchTask** atualiza as propriedades de uma tarefa no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="a41d5-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="a41d5-107">Use o cmdlet Get-AzureBatchTask para obter um objeto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="a41d5-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="a41d5-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="a41d5-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a41d5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a41d5-109">EXAMPLES</span></span>

### <span data-ttu-id="a41d5-110">Exemplo 1: atualizar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="a41d5-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="a41d5-111">O primeiro comando obtém uma tarefa usando **Get-AzureBatchTask** e, em seguida, armazena-a na variável $Task.</span><span class="sxs-lookup"><span data-stu-id="a41d5-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="a41d5-112">Os próximos dois comandos modificam as restrições da tarefa em $Task.</span><span class="sxs-lookup"><span data-stu-id="a41d5-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="a41d5-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Task.</span><span class="sxs-lookup"><span data-stu-id="a41d5-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="a41d5-114">OS</span><span class="sxs-lookup"><span data-stu-id="a41d5-114">PARAMETERS</span></span>

### <span data-ttu-id="a41d5-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a41d5-115">-BatchContext</span></span>
<span data-ttu-id="a41d5-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a41d5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a41d5-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a41d5-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a41d5-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="a41d5-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a41d5-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a41d5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a41d5-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a41d5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a41d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41d5-121">-DefaultProfile</span></span>
<span data-ttu-id="a41d5-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a41d5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a41d5-123">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="a41d5-123">-Task</span></span>
<span data-ttu-id="a41d5-124">Especifica o **PSCloudTask** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a41d5-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a41d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41d5-125">CommonParameters</span></span>
<span data-ttu-id="a41d5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a41d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41d5-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a41d5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41d5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a41d5-128">INPUTS</span></span>

### <span data-ttu-id="a41d5-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a41d5-129">BatchAccountContext</span></span>
<span data-ttu-id="a41d5-130">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a41d5-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a41d5-131">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a41d5-131">PSCloudTask</span></span>
<span data-ttu-id="a41d5-132">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a41d5-132">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="a41d5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a41d5-133">OUTPUTS</span></span>

## <span data-ttu-id="a41d5-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a41d5-134">NOTES</span></span>

## <span data-ttu-id="a41d5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a41d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="a41d5-136">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a41d5-136">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="a41d5-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a41d5-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a41d5-138">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a41d5-138">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="a41d5-139">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a41d5-139">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="a41d5-140">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a41d5-140">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="a41d5-141">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="a41d5-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


