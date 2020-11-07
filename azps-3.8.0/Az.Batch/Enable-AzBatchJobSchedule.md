---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 0684652dd5e5a0232e5808119ae8453be8f9ade8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947184"
---
# <span data-ttu-id="8e08f-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e08f-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="8e08f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e08f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e08f-103">Habilita um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="8e08f-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="8e08f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e08f-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e08f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e08f-105">DESCRIPTION</span></span>
<span data-ttu-id="8e08f-106">O cmdlet **Enable-AzBatchJobSchedule** habilita um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e08f-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="8e08f-107">Depois de habilitar um plano de trabalho, os trabalhos podem ser criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="8e08f-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="8e08f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e08f-108">EXAMPLES</span></span>

### <span data-ttu-id="8e08f-109">Exemplo 1: habilitar um plano de trabalho</span><span class="sxs-lookup"><span data-stu-id="8e08f-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="8e08f-110">Esse comando habilita o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="8e08f-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8e08f-111">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="8e08f-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8e08f-112">OS</span><span class="sxs-lookup"><span data-stu-id="8e08f-112">PARAMETERS</span></span>

### <span data-ttu-id="8e08f-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e08f-113">-BatchContext</span></span>
<span data-ttu-id="8e08f-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8e08f-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e08f-115">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8e08f-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e08f-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8e08f-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e08f-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8e08f-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e08f-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8e08f-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e08f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e08f-119">-DefaultProfile</span></span>
<span data-ttu-id="8e08f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e08f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e08f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="8e08f-121">-Id</span></span>
<span data-ttu-id="8e08f-122">Especifica a ID do agendamento de trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="8e08f-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="8e08f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e08f-123">CommonParameters</span></span>
<span data-ttu-id="8e08f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e08f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e08f-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e08f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e08f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e08f-126">INPUTS</span></span>

### <span data-ttu-id="8e08f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8e08f-127">System.String</span></span>

### <span data-ttu-id="8e08f-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e08f-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e08f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e08f-129">OUTPUTS</span></span>

### <span data-ttu-id="8e08f-130">System. void</span><span class="sxs-lookup"><span data-stu-id="8e08f-130">System.Void</span></span>

## <span data-ttu-id="8e08f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e08f-131">NOTES</span></span>

## <span data-ttu-id="8e08f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e08f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e08f-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e08f-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="8e08f-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e08f-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e08f-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e08f-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="8e08f-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e08f-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="8e08f-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e08f-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="8e08f-138">Parar-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e08f-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="8e08f-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8e08f-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


