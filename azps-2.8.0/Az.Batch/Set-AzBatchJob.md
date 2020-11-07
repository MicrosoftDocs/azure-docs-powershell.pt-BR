---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 86e977c3d538c9eeb5f26da7d70db1726adf119b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785091"
---
# <span data-ttu-id="6f58c-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="6f58c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f58c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f58c-103">Atualiza um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="6f58c-103">Updates a Batch job.</span></span>

## <span data-ttu-id="6f58c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f58c-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f58c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f58c-105">DESCRIPTION</span></span>
<span data-ttu-id="6f58c-106">O cmdlet **set-AzBatchJob** atualiza um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f58c-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="6f58c-107">Use o cmdlet Get-AzBatchJob para obter um objeto **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="6f58c-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="6f58c-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="6f58c-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="6f58c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f58c-109">EXAMPLES</span></span>

### <span data-ttu-id="6f58c-110">Exemplo 1: atualizar um trabalho</span><span class="sxs-lookup"><span data-stu-id="6f58c-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="6f58c-111">O primeiro comando obtém um trabalho usando **Get-AzBatchJob** e, em seguida, armazena-o na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="6f58c-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="6f58c-112">O segundo comando modifica a especificação de prioridade no objeto $Job.</span><span class="sxs-lookup"><span data-stu-id="6f58c-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="6f58c-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Job.</span><span class="sxs-lookup"><span data-stu-id="6f58c-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="6f58c-114">OS</span><span class="sxs-lookup"><span data-stu-id="6f58c-114">PARAMETERS</span></span>

### <span data-ttu-id="6f58c-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f58c-115">-BatchContext</span></span>
<span data-ttu-id="6f58c-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6f58c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f58c-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6f58c-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6f58c-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="6f58c-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6f58c-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6f58c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6f58c-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6f58c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6f58c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f58c-121">-DefaultProfile</span></span>
<span data-ttu-id="6f58c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f58c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f58c-123">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="6f58c-123">-Job</span></span>
<span data-ttu-id="6f58c-124">Especifica um **PSCloudJob** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6f58c-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="6f58c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f58c-125">CommonParameters</span></span>
<span data-ttu-id="6f58c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f58c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f58c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f58c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f58c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f58c-128">INPUTS</span></span>

### <span data-ttu-id="6f58c-129">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="6f58c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f58c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6f58c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f58c-131">OUTPUTS</span></span>

### <span data-ttu-id="6f58c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="6f58c-132">System.Void</span></span>

## <span data-ttu-id="6f58c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f58c-133">NOTES</span></span>

## <span data-ttu-id="6f58c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f58c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f58c-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="6f58c-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="6f58c-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6f58c-138">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6f58c-138">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6f58c-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="6f58c-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="6f58c-141">Parar-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f58c-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="6f58c-142">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="6f58c-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


