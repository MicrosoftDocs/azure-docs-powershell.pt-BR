---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 54b9f9b60c1d424e6fd62ede85e517b40df1d062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893404"
---
# <span data-ttu-id="2f9df-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f9df-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="2f9df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f9df-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9df-103">Desabilita um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="2f9df-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="2f9df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2f9df-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f9df-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2f9df-105">DESCRIPTION</span></span>
<span data-ttu-id="2f9df-106">O cmdlet **Disable-AzBatchJobSchedule** desabilita um cronograma de trabalho do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f9df-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="2f9df-107">Se você desabilitar um cronograma, os trabalhos não serão criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="2f9df-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="2f9df-108">Você pode habilitar uma agenda desabilitada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="2f9df-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="2f9df-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f9df-109">EXAMPLES</span></span>

### <span data-ttu-id="2f9df-110">Exemplo 1: Desabilitar um agendamento de trabalho</span><span class="sxs-lookup"><span data-stu-id="2f9df-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="2f9df-111">Este comando desabilita o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="2f9df-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="2f9df-112">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="2f9df-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2f9df-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2f9df-113">PARAMETERS</span></span>

### <span data-ttu-id="2f9df-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2f9df-114">-BatchContext</span></span>
<span data-ttu-id="2f9df-115">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="2f9df-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2f9df-116">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="2f9df-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2f9df-117">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="2f9df-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2f9df-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="2f9df-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2f9df-119">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2f9df-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2f9df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9df-120">-DefaultProfile</span></span>
<span data-ttu-id="2f9df-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2f9df-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f9df-122">-Id</span><span class="sxs-lookup"><span data-stu-id="2f9df-122">-Id</span></span>
<span data-ttu-id="2f9df-123">Especifica a ID do cronograma de trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="2f9df-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="2f9df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9df-124">CommonParameters</span></span>
<span data-ttu-id="2f9df-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9df-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f9df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9df-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f9df-127">INPUTS</span></span>

### <span data-ttu-id="2f9df-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2f9df-128">System.String</span></span>

### <span data-ttu-id="2f9df-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2f9df-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2f9df-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2f9df-130">OUTPUTS</span></span>

### <span data-ttu-id="2f9df-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="2f9df-131">System.Void</span></span>

## <span data-ttu-id="2f9df-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="2f9df-132">NOTES</span></span>

## <span data-ttu-id="2f9df-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f9df-133">RELATED LINKS</span></span>

[<span data-ttu-id="2f9df-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f9df-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="2f9df-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2f9df-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2f9df-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f9df-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="2f9df-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f9df-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="2f9df-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f9df-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="2f9df-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f9df-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="2f9df-140">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="2f9df-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
