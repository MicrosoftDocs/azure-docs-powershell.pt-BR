---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117976"
---
# <span data-ttu-id="d9bd3-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9bd3-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="d9bd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bd3-103">Habilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-103">Enables a Batch job.</span></span>

## <span data-ttu-id="d9bd3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9bd3-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9bd3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bd3-106">O **cmdlet Enable-AzBatch Job** habilita um trabalho do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="d9bd3-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="d9bd3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d9bd3-108">EXAMPLES</span></span>

### <span data-ttu-id="d9bd3-109">Exemplo 1: Habilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="d9bd3-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="d9bd3-110">Esse comando habilita o trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d9bd3-111">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d9bd3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9bd3-112">PARAMETERS</span></span>

### <span data-ttu-id="d9bd3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9bd3-113">-BatchContext</span></span>
<span data-ttu-id="d9bd3-114">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9bd3-115">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9bd3-116">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9bd3-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9bd3-118">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9bd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bd3-119">-DefaultProfile</span></span>
<span data-ttu-id="d9bd3-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bd3-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d9bd3-121">-Id</span></span>
<span data-ttu-id="d9bd3-122">Especifica a ID do trabalho que esse cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="d9bd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bd3-123">CommonParameters</span></span>
<span data-ttu-id="d9bd3-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bd3-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9bd3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bd3-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="d9bd3-126">INPUTS</span></span>

### <span data-ttu-id="d9bd3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d9bd3-127">System.String</span></span>

### <span data-ttu-id="d9bd3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9bd3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d9bd3-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="d9bd3-129">OUTPUTS</span></span>

### <span data-ttu-id="d9bd3-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d9bd3-130">System.Void</span></span>

## <span data-ttu-id="d9bd3-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d9bd3-131">NOTES</span></span>

## <span data-ttu-id="d9bd3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9bd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9bd3-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9bd3-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="d9bd3-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9bd3-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="d9bd3-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9bd3-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="d9bd3-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9bd3-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="d9bd3-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9bd3-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="d9bd3-138">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="d9bd3-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
