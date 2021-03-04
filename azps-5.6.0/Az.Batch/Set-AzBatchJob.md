---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: cc084f276f379013125693e3314ff1eab8a7b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887034"
---
# <span data-ttu-id="283e7-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="283e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="283e7-102">SYNOPSIS</span></span>
<span data-ttu-id="283e7-103">Atualiza um trabalho em lote.</span><span class="sxs-lookup"><span data-stu-id="283e7-103">Updates a Batch job.</span></span>

## <span data-ttu-id="283e7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="283e7-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="283e7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="283e7-105">DESCRIPTION</span></span>
<span data-ttu-id="283e7-106">O cmdlet **Set-AzBatchJob** atualiza um trabalho do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="283e7-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="283e7-107">Use o cmdlet Get-AzBatchJob para obter um **objeto PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="283e7-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="283e7-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para comprometer suas alterações no serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="283e7-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="283e7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="283e7-109">EXAMPLES</span></span>

### <span data-ttu-id="283e7-110">Exemplo 1: atualizar um trabalho</span><span class="sxs-lookup"><span data-stu-id="283e7-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="283e7-111">O primeiro comando obtém um trabalho usando **Get-AzBatchJob** e o armazena na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="283e7-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="283e7-112">O segundo comando modifica a especificação de prioridade no objeto $Job.</span><span class="sxs-lookup"><span data-stu-id="283e7-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="283e7-113">O comando final atualiza o serviço Batch para corresponder ao objeto local no $Job.</span><span class="sxs-lookup"><span data-stu-id="283e7-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="283e7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="283e7-114">PARAMETERS</span></span>

### <span data-ttu-id="283e7-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="283e7-115">-BatchContext</span></span>
<span data-ttu-id="283e7-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="283e7-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="283e7-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="283e7-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="283e7-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="283e7-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="283e7-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="283e7-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="283e7-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="283e7-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="283e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283e7-121">-DefaultProfile</span></span>
<span data-ttu-id="283e7-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="283e7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="283e7-123">-Job</span><span class="sxs-lookup"><span data-stu-id="283e7-123">-Job</span></span>
<span data-ttu-id="283e7-124">Especifica um **PSCloudJob** ao qual este cmdlet atualiza o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="283e7-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="283e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283e7-125">CommonParameters</span></span>
<span data-ttu-id="283e7-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283e7-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="283e7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283e7-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="283e7-128">INPUTS</span></span>

### <span data-ttu-id="283e7-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="283e7-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="283e7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="283e7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="283e7-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="283e7-131">OUTPUTS</span></span>

### <span data-ttu-id="283e7-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="283e7-132">System.Void</span></span>

## <span data-ttu-id="283e7-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="283e7-133">NOTES</span></span>

## <span data-ttu-id="283e7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="283e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="283e7-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="283e7-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="283e7-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="283e7-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="283e7-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="283e7-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="283e7-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="283e7-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="283e7-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="283e7-142">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="283e7-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
