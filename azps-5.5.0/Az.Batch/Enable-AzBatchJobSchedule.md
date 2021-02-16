---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117974"
---
# <span data-ttu-id="6dc31-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6dc31-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="6dc31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dc31-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc31-103">Habilita um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="6dc31-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="6dc31-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dc31-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc31-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6dc31-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc31-106">O cmdlet **Enable-AzBatch JobSchedule** habilita um cronograma de trabalho do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="6dc31-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="6dc31-107">Depois de habilitar um cronograma de trabalho, os trabalhos podem ser criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="6dc31-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="6dc31-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6dc31-108">EXAMPLES</span></span>

### <span data-ttu-id="6dc31-109">Exemplo 1: Habilitar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="6dc31-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="6dc31-110">Esse comando habilita o cronograma de trabalho que tem o JobSchedule17 de ID.</span><span class="sxs-lookup"><span data-stu-id="6dc31-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="6dc31-111">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="6dc31-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6dc31-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dc31-112">PARAMETERS</span></span>

### <span data-ttu-id="6dc31-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6dc31-113">-BatchContext</span></span>
<span data-ttu-id="6dc31-114">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="6dc31-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6dc31-115">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="6dc31-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6dc31-116">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="6dc31-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6dc31-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6dc31-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6dc31-118">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6dc31-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6dc31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc31-119">-DefaultProfile</span></span>
<span data-ttu-id="6dc31-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6dc31-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dc31-121">-ID</span><span class="sxs-lookup"><span data-stu-id="6dc31-121">-Id</span></span>
<span data-ttu-id="6dc31-122">Especifica a ID do cronograma de trabalho que esse cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="6dc31-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc31-123">CommonParameters</span></span>
<span data-ttu-id="6dc31-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc31-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dc31-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc31-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="6dc31-126">INPUTS</span></span>

### <span data-ttu-id="6dc31-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6dc31-127">System.String</span></span>

### <span data-ttu-id="6dc31-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6dc31-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6dc31-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="6dc31-129">OUTPUTS</span></span>

### <span data-ttu-id="6dc31-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="6dc31-130">System.Void</span></span>

## <span data-ttu-id="6dc31-131">Notas</span><span class="sxs-lookup"><span data-stu-id="6dc31-131">NOTES</span></span>

## <span data-ttu-id="6dc31-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dc31-132">RELATED LINKS</span></span>

[<span data-ttu-id="6dc31-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6dc31-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="6dc31-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6dc31-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6dc31-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6dc31-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="6dc31-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6dc31-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="6dc31-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6dc31-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="6dc31-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6dc31-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="6dc31-139">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="6dc31-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
