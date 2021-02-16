---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127124"
---
# <span data-ttu-id="2ab96-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="2ab96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ab96-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab96-103">Atualiza um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="2ab96-103">Updates a Batch job.</span></span>

## <span data-ttu-id="2ab96-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ab96-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ab96-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ab96-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab96-106">O **cmdlet Set-AzBatch Job** atualiza um trabalho do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="2ab96-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="2ab96-107">Use o Get-AzBatchJob cmdlet para obter um **objeto PSCloudCloudCloud.**</span><span class="sxs-lookup"><span data-stu-id="2ab96-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="2ab96-108">Modifique as propriedades desse objeto e use o cmdlet atual para comprometer suas alterações no serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="2ab96-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="2ab96-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2ab96-109">EXAMPLES</span></span>

### <span data-ttu-id="2ab96-110">Exemplo 1: Atualizar um trabalho</span><span class="sxs-lookup"><span data-stu-id="2ab96-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="2ab96-111">O primeiro comando obtém um trabalho usando **Get-AzBatch Job** e, em seguida, o armazena na variável $Job dados.</span><span class="sxs-lookup"><span data-stu-id="2ab96-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="2ab96-112">O segundo comando modifica a especificação de prioridade no $Job objeto.</span><span class="sxs-lookup"><span data-stu-id="2ab96-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="2ab96-113">O comando final atualiza o serviço Lote para corresponder ao objeto local no $Job.</span><span class="sxs-lookup"><span data-stu-id="2ab96-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="2ab96-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ab96-114">PARAMETERS</span></span>

### <span data-ttu-id="2ab96-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2ab96-115">-BatchContext</span></span>
<span data-ttu-id="2ab96-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="2ab96-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2ab96-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="2ab96-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2ab96-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="2ab96-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2ab96-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="2ab96-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2ab96-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2ab96-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2ab96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab96-121">-DefaultProfile</span></span>
<span data-ttu-id="2ab96-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2ab96-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ab96-123">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="2ab96-123">-Job</span></span>
<span data-ttu-id="2ab96-124">Especifica um **PSCloudCloudCloud ao** qual este cmdlet atualiza o serviço Em lotes.</span><span class="sxs-lookup"><span data-stu-id="2ab96-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="2ab96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab96-125">CommonParameters</span></span>
<span data-ttu-id="2ab96-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab96-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ab96-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab96-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="2ab96-128">INPUTS</span></span>

### <span data-ttu-id="2ab96-129">Microsoft.Azure.Commands.Batch. Models.PSCloudCloud</span><span class="sxs-lookup"><span data-stu-id="2ab96-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="2ab96-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2ab96-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2ab96-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="2ab96-131">OUTPUTS</span></span>

### <span data-ttu-id="2ab96-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="2ab96-132">System.Void</span></span>

## <span data-ttu-id="2ab96-133">Notas</span><span class="sxs-lookup"><span data-stu-id="2ab96-133">NOTES</span></span>

## <span data-ttu-id="2ab96-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ab96-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ab96-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2ab96-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="2ab96-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2ab96-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2ab96-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2ab96-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2ab96-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2ab96-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ab96-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2ab96-142">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="2ab96-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
