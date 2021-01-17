---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430536"
---
# <span data-ttu-id="13bde-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13bde-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="13bde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13bde-102">SYNOPSIS</span></span>
<span data-ttu-id="13bde-103">Desabilita o cronograma de um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="13bde-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="13bde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13bde-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13bde-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13bde-105">DESCRIPTION</span></span>
<span data-ttu-id="13bde-106">O cmdlet **Disable-AzBatchJobSchedule** desabilita um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="13bde-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="13bde-107">Se você desabilitar um cronograma, os trabalhos não serão criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="13bde-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="13bde-108">Você pode habilitar um cronograma desabilitado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="13bde-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="13bde-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13bde-109">EXAMPLES</span></span>

### <span data-ttu-id="13bde-110">Exemplo 1: desabilitar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="13bde-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="13bde-111">Esse comando desabilita o plano de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="13bde-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="13bde-112">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="13bde-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="13bde-113">OS</span><span class="sxs-lookup"><span data-stu-id="13bde-113">PARAMETERS</span></span>

### <span data-ttu-id="13bde-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="13bde-114">-BatchContext</span></span>
<span data-ttu-id="13bde-115">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="13bde-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="13bde-116">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="13bde-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="13bde-117">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="13bde-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="13bde-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="13bde-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="13bde-119">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="13bde-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="13bde-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bde-120">-DefaultProfile</span></span>
<span data-ttu-id="13bde-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13bde-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13bde-122">-ID</span><span class="sxs-lookup"><span data-stu-id="13bde-122">-Id</span></span>
<span data-ttu-id="13bde-123">Especifica a ID do agendamento de trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="13bde-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="13bde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bde-124">CommonParameters</span></span>
<span data-ttu-id="13bde-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bde-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13bde-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bde-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13bde-127">INPUTS</span></span>

### <span data-ttu-id="13bde-128">System. String</span><span class="sxs-lookup"><span data-stu-id="13bde-128">System.String</span></span>

### <span data-ttu-id="13bde-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="13bde-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="13bde-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13bde-130">OUTPUTS</span></span>

### <span data-ttu-id="13bde-131">System. void</span><span class="sxs-lookup"><span data-stu-id="13bde-131">System.Void</span></span>

## <span data-ttu-id="13bde-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13bde-132">NOTES</span></span>

## <span data-ttu-id="13bde-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13bde-133">RELATED LINKS</span></span>

[<span data-ttu-id="13bde-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13bde-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="13bde-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="13bde-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="13bde-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13bde-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="13bde-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13bde-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="13bde-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13bde-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="13bde-139">Parar-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13bde-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="13bde-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="13bde-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
