---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: ab1293bf147424bb9a7315cb541b9bf22fe4a357
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115531"
---
# <span data-ttu-id="b4bfd-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bfd-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="b4bfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bfd-103">Cria um cronograma de trabalho no serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="b4bfd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4bfd-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4bfd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="b4bfd-106">O cmdlet **New-AzBatch JobSchedule** cria um cronograma de trabalho no serviço Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="b4bfd-107">O *parâmetro BatchAccountContext* especifica a conta na qual esse cmdlet cria o cronograma.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="b4bfd-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4bfd-108">EXAMPLES</span></span>

### <span data-ttu-id="b4bfd-109">Exemplo 1: Criar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="b4bfd-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="b4bfd-110">Este exemplo cria um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-110">This example creates a job schedule.</span></span>
<span data-ttu-id="b4bfd-111">Os cinco primeiros comandos criam e modificam **objetos PSSchedule,** **PSJobSpecification** e **PSPoolInformation.**</span><span class="sxs-lookup"><span data-stu-id="b4bfd-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="b4bfd-112">Os comandos usam o cmdlet New-Object e a sintaxe padrão do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="b4bfd-113">Os comandos armazenam esses objetos nas variáveis $Schedule e $JobSpecification dados.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="b4bfd-114">O comando final cria um cronograma de trabalho com a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="b4bfd-115">Esse cronograma cria trabalhos com um intervalo de recorrência de um dia.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="b4bfd-116">Os trabalhos são executados no pool que tem a ID ContosoPool06, conforme especificado no quinto comando.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="b4bfd-117">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b4bfd-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4bfd-118">PARAMETERS</span></span>

### <span data-ttu-id="b4bfd-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4bfd-119">-BatchContext</span></span>
<span data-ttu-id="b4bfd-120">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4bfd-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4bfd-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4bfd-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4bfd-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4bfd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bfd-125">-DefaultProfile</span></span>
<span data-ttu-id="b4bfd-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4bfd-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4bfd-127">-DisplayName</span></span>
<span data-ttu-id="b4bfd-128">Especifica um nome de exibição para o cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-128">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bfd-129">-ID</span><span class="sxs-lookup"><span data-stu-id="b4bfd-129">-Id</span></span>
<span data-ttu-id="b4bfd-130">Especifica a ID do cronograma de trabalho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bfd-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="b4bfd-131">-JobSpecification</span></span>
<span data-ttu-id="b4bfd-132">Especifica os detalhes dos trabalhos que este cmdlet inclui no cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bfd-133">-Metadados</span><span class="sxs-lookup"><span data-stu-id="b4bfd-133">-Metadata</span></span>
<span data-ttu-id="b4bfd-134">Especifica metadados, como pares de chave/valor, para adicionar ao cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="b4bfd-135">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-135">The key is the metadata name.</span></span>
<span data-ttu-id="b4bfd-136">O valor é o valor de metadados.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-136">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bfd-137">-Agendar</span><span class="sxs-lookup"><span data-stu-id="b4bfd-137">-Schedule</span></span>
<span data-ttu-id="b4bfd-138">Especifica o cronograma que determina quando criar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bfd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bfd-139">CommonParameters</span></span>
<span data-ttu-id="b4bfd-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bfd-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4bfd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bfd-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4bfd-142">INPUTS</span></span>

### <span data-ttu-id="b4bfd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b4bfd-143">System.String</span></span>

### <span data-ttu-id="b4bfd-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4bfd-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4bfd-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4bfd-145">OUTPUTS</span></span>

### <span data-ttu-id="b4bfd-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="b4bfd-146">System.Void</span></span>

## <span data-ttu-id="b4bfd-147">Notas</span><span class="sxs-lookup"><span data-stu-id="b4bfd-147">NOTES</span></span>

## <span data-ttu-id="b4bfd-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4bfd-148">RELATED LINKS</span></span>

[<span data-ttu-id="b4bfd-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bfd-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="b4bfd-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bfd-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="b4bfd-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4bfd-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b4bfd-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bfd-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="b4bfd-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bfd-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="b4bfd-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bfd-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="b4bfd-155">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="b4bfd-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
