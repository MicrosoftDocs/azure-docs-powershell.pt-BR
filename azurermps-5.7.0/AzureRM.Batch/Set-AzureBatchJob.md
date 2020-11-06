---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440118"
---
# <span data-ttu-id="e986e-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="e986e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e986e-102">SYNOPSIS</span></span>
<span data-ttu-id="e986e-103">Atualiza um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="e986e-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e986e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e986e-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e986e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e986e-105">DESCRIPTION</span></span>
<span data-ttu-id="e986e-106">O cmdlet **set-AzureBatchJob** atualiza um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="e986e-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="e986e-107">Use o cmdlet Get-AzureBatchJob para obter um objeto **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="e986e-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="e986e-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="e986e-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="e986e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e986e-109">EXAMPLES</span></span>

### <span data-ttu-id="e986e-110">Exemplo 1: atualizar um trabalho</span><span class="sxs-lookup"><span data-stu-id="e986e-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="e986e-111">O primeiro comando obtém um pool usando **Get-AzureBatchJob** e, em seguida, armazena-o na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="e986e-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="e986e-112">O segundo comando modifica a especificação de prioridade no objeto $Job.</span><span class="sxs-lookup"><span data-stu-id="e986e-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="e986e-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Job.</span><span class="sxs-lookup"><span data-stu-id="e986e-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="e986e-114">OS</span><span class="sxs-lookup"><span data-stu-id="e986e-114">PARAMETERS</span></span>

### <span data-ttu-id="e986e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e986e-115">-BatchContext</span></span>
<span data-ttu-id="e986e-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e986e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e986e-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e986e-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e986e-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e986e-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e986e-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e986e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e986e-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e986e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e986e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e986e-121">-DefaultProfile</span></span>
<span data-ttu-id="e986e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e986e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e986e-123">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="e986e-123">-Job</span></span>
<span data-ttu-id="e986e-124">Especifica um **PSCloudJob** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e986e-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e986e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e986e-125">CommonParameters</span></span>
<span data-ttu-id="e986e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e986e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e986e-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e986e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e986e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e986e-128">INPUTS</span></span>

### <span data-ttu-id="e986e-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e986e-129">BatchAccountContext</span></span>
<span data-ttu-id="e986e-130">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e986e-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e986e-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="e986e-131">PSCloudJob</span></span>
<span data-ttu-id="e986e-132">O parâmetro ' Job ' aceita o valor do tipo ' PSCloudJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e986e-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="e986e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e986e-133">OUTPUTS</span></span>

## <span data-ttu-id="e986e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e986e-134">NOTES</span></span>

## <span data-ttu-id="e986e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e986e-135">RELATED LINKS</span></span>

[<span data-ttu-id="e986e-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="e986e-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="e986e-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="e986e-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e986e-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e986e-140">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="e986e-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="e986e-142">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e986e-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="e986e-143">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="e986e-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

