---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785043"
---
# <span data-ttu-id="e4dbd-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="e4dbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e4dbd-103">Habilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-103">Enables a Batch job.</span></span>

## <span data-ttu-id="e4dbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4dbd-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4dbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="e4dbd-106">O cmdlet **Enable-AzBatchJob** habilita um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="e4dbd-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="e4dbd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4dbd-108">EXAMPLES</span></span>

### <span data-ttu-id="e4dbd-109">Exemplo 1: habilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="e4dbd-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="e4dbd-110">Esse comando habilita o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e4dbd-111">Use o cmdlet Get-AzBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e4dbd-112">OS</span><span class="sxs-lookup"><span data-stu-id="e4dbd-112">PARAMETERS</span></span>

### <span data-ttu-id="e4dbd-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e4dbd-113">-BatchContext</span></span>
<span data-ttu-id="e4dbd-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e4dbd-115">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e4dbd-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e4dbd-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e4dbd-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e4dbd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4dbd-119">-DefaultProfile</span></span>
<span data-ttu-id="e4dbd-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4dbd-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e4dbd-121">-Id</span></span>
<span data-ttu-id="e4dbd-122">Especifica a ID do trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="e4dbd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4dbd-123">CommonParameters</span></span>
<span data-ttu-id="e4dbd-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4dbd-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4dbd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4dbd-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4dbd-126">INPUTS</span></span>

### <span data-ttu-id="e4dbd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e4dbd-127">System.String</span></span>

### <span data-ttu-id="e4dbd-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e4dbd-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e4dbd-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4dbd-129">OUTPUTS</span></span>

### <span data-ttu-id="e4dbd-130">System. void</span><span class="sxs-lookup"><span data-stu-id="e4dbd-130">System.Void</span></span>

## <span data-ttu-id="e4dbd-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4dbd-131">NOTES</span></span>

## <span data-ttu-id="e4dbd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4dbd-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4dbd-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="e4dbd-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e4dbd-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e4dbd-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="e4dbd-137">Parar-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="e4dbd-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="e4dbd-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


