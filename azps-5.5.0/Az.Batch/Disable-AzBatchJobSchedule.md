---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117985"
---
# <span data-ttu-id="f0c87-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f0c87-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f0c87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0c87-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c87-103">Desabilita um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="f0c87-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="f0c87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0c87-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0c87-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0c87-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c87-106">O cmdlet **Disable-AzBatch JobSchedule** desabilita um cronograma de trabalho do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="f0c87-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="f0c87-107">Se você desabilitar um cronograma, os trabalhos não serão criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="f0c87-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="f0c87-108">Você pode habilitar uma agenda desabilitada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f0c87-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="f0c87-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0c87-109">EXAMPLES</span></span>

### <span data-ttu-id="f0c87-110">Exemplo 1: Desabilitar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="f0c87-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="f0c87-111">Esse comando desabilita o cronograma de trabalho que tem o JobSchedule17 de ID.</span><span class="sxs-lookup"><span data-stu-id="f0c87-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f0c87-112">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="f0c87-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f0c87-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0c87-113">PARAMETERS</span></span>

### <span data-ttu-id="f0c87-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f0c87-114">-BatchContext</span></span>
<span data-ttu-id="f0c87-115">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="f0c87-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f0c87-116">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="f0c87-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f0c87-117">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f0c87-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f0c87-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f0c87-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f0c87-119">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f0c87-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f0c87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c87-120">-DefaultProfile</span></span>
<span data-ttu-id="f0c87-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f0c87-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c87-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f0c87-122">-Id</span></span>
<span data-ttu-id="f0c87-123">Especifica a ID do cronograma de trabalho que este cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="f0c87-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="f0c87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c87-124">CommonParameters</span></span>
<span data-ttu-id="f0c87-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c87-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0c87-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c87-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="f0c87-127">INPUTS</span></span>

### <span data-ttu-id="f0c87-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f0c87-128">System.String</span></span>

### <span data-ttu-id="f0c87-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f0c87-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f0c87-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="f0c87-130">OUTPUTS</span></span>

### <span data-ttu-id="f0c87-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="f0c87-131">System.Void</span></span>

## <span data-ttu-id="f0c87-132">Notas</span><span class="sxs-lookup"><span data-stu-id="f0c87-132">NOTES</span></span>

## <span data-ttu-id="f0c87-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0c87-133">RELATED LINKS</span></span>

[<span data-ttu-id="f0c87-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f0c87-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f0c87-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f0c87-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f0c87-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f0c87-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f0c87-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f0c87-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f0c87-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f0c87-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f0c87-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f0c87-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f0c87-140">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="f0c87-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
