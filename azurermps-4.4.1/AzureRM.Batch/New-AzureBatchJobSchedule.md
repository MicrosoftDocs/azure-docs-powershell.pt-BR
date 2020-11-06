---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431150"
---
# <span data-ttu-id="0282b-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0282b-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="0282b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0282b-102">SYNOPSIS</span></span>
<span data-ttu-id="0282b-103">Cria um plano de trabalho no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="0282b-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0282b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0282b-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0282b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0282b-105">DESCRIPTION</span></span>
<span data-ttu-id="0282b-106">O cmdlet **New-AzureBatchJobSchedule** cria um cronograma de trabalho no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="0282b-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="0282b-107">O parâmetro *BatchAccountContext* especifica a conta na qual esse cmdlet cria o cronograma.</span><span class="sxs-lookup"><span data-stu-id="0282b-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="0282b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0282b-108">EXAMPLES</span></span>

### <span data-ttu-id="0282b-109">Exemplo 1: criar um plano de trabalho</span><span class="sxs-lookup"><span data-stu-id="0282b-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="0282b-110">Este exemplo cria um plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0282b-110">This example creates a job schedule.</span></span>

<span data-ttu-id="0282b-111">Os cinco primeiros comandos criam e modificam objetos **PSSchedule** , **PSJobSpecification** e **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="0282b-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="0282b-112">Os comandos usam o cmdlet New-Object e a sintaxe padrão do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="0282b-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="0282b-113">Os comandos armazenam esses objetos nas variáveis $Schedule e $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="0282b-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="0282b-114">O comando final cria um plano de trabalho com a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="0282b-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0282b-115">Esse cronograma cria trabalhos com um intervalo de recorrência de um dia.</span><span class="sxs-lookup"><span data-stu-id="0282b-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="0282b-116">Os trabalhos são executados no pool que tem a ID ContosoPool06, conforme especificado no quinto comando.</span><span class="sxs-lookup"><span data-stu-id="0282b-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="0282b-117">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="0282b-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0282b-118">OS</span><span class="sxs-lookup"><span data-stu-id="0282b-118">PARAMETERS</span></span>

### <span data-ttu-id="0282b-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0282b-119">-BatchContext</span></span>
<span data-ttu-id="0282b-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="0282b-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0282b-121">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="0282b-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0282b-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0282b-122">-DisplayName</span></span>
<span data-ttu-id="0282b-123">Especifica um nome de exibição para o plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0282b-123">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="0282b-124">-ID</span><span class="sxs-lookup"><span data-stu-id="0282b-124">-Id</span></span>
<span data-ttu-id="0282b-125">Especifica a ID do agendamento de trabalho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="0282b-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0282b-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="0282b-126">-JobSpecification</span></span>
<span data-ttu-id="0282b-127">Especifica os detalhes dos trabalhos que este cmdlet inclui no cronograma do trabalho.</span><span class="sxs-lookup"><span data-stu-id="0282b-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="0282b-128">-Metadados</span><span class="sxs-lookup"><span data-stu-id="0282b-128">-Metadata</span></span>
<span data-ttu-id="0282b-129">Especifica os metadados, como pares de chave/valor, a serem adicionados ao plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0282b-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="0282b-130">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="0282b-130">The key is the metadata name.</span></span>
<span data-ttu-id="0282b-131">O valor é o valor dos metadados.</span><span class="sxs-lookup"><span data-stu-id="0282b-131">The value is the metadata value.</span></span>

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

### <span data-ttu-id="0282b-132">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="0282b-132">-Schedule</span></span>
<span data-ttu-id="0282b-133">Especifica o cronograma que determina quando criar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="0282b-133">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="0282b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0282b-134">-DefaultProfile</span></span>
<span data-ttu-id="0282b-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0282b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0282b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0282b-136">CommonParameters</span></span>
<span data-ttu-id="0282b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0282b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0282b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0282b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0282b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0282b-139">INPUTS</span></span>

### <span data-ttu-id="0282b-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0282b-140">BatchAccountContext</span></span>
<span data-ttu-id="0282b-141">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0282b-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="0282b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0282b-142">OUTPUTS</span></span>

## <span data-ttu-id="0282b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0282b-143">NOTES</span></span>

## <span data-ttu-id="0282b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0282b-144">RELATED LINKS</span></span>

[<span data-ttu-id="0282b-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0282b-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0282b-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0282b-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0282b-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0282b-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0282b-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0282b-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="0282b-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0282b-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="0282b-150">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0282b-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="0282b-151">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="0282b-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


