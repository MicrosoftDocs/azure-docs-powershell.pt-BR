---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431800"
---
# <span data-ttu-id="13389-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="13389-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="13389-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13389-102">SYNOPSIS</span></span>
<span data-ttu-id="13389-103">Começa a redimensionar um pool.</span><span class="sxs-lookup"><span data-stu-id="13389-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13389-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13389-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13389-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13389-105">DESCRIPTION</span></span>
<span data-ttu-id="13389-106">O cmdlet **Start-AzureBatchPoolResize** inicia uma operação de redimensionamento em lotes do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="13389-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="13389-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13389-107">EXAMPLES</span></span>

### <span data-ttu-id="13389-108">Exemplo 1: redimensionar um pool para 12 nós</span><span class="sxs-lookup"><span data-stu-id="13389-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="13389-109">Esse comando inicia uma operação de redimensionamento no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="13389-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="13389-110">O destino para a operação é 12 nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="13389-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="13389-111">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="13389-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="13389-112">Exemplo 2: redimensionar um pool usando uma opção de desalocação</span><span class="sxs-lookup"><span data-stu-id="13389-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="13389-113">Esse cmdlet redimensiona um pool para cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="13389-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="13389-114">O comando obtém o pool com a ID ContosoPool06 usando o cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="13389-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="13389-115">O comando passa esse objeto de pool para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="13389-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13389-116">O comando inicia uma operação de redimensionamento no pool.</span><span class="sxs-lookup"><span data-stu-id="13389-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="13389-117">O destino é cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="13389-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="13389-118">O comando especifica o período de tempo limite de uma hora.</span><span class="sxs-lookup"><span data-stu-id="13389-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="13389-119">O comando especifica uma opção de desalocação de Terminate.</span><span class="sxs-lookup"><span data-stu-id="13389-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="13389-120">OS</span><span class="sxs-lookup"><span data-stu-id="13389-120">PARAMETERS</span></span>

### <span data-ttu-id="13389-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="13389-121">-BatchContext</span></span>
<span data-ttu-id="13389-122">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="13389-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="13389-123">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="13389-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="13389-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="13389-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="13389-125">Especifica uma opção de desalocação para a operação de redimensionamento que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="13389-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13389-126">-ID</span><span class="sxs-lookup"><span data-stu-id="13389-126">-Id</span></span>
<span data-ttu-id="13389-127">Especifica a ID do pool que esse cmdlet redimensiona.</span><span class="sxs-lookup"><span data-stu-id="13389-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="13389-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="13389-128">-ResizeTimeout</span></span>
<span data-ttu-id="13389-129">Especifica um período de tempo limite para a operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="13389-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="13389-130">Se o pool não atingir o tamanho de destino até o momento, a operação de redimensionamento será interrompida.</span><span class="sxs-lookup"><span data-stu-id="13389-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13389-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="13389-131">-TargetDedicated</span></span>
<span data-ttu-id="13389-132">Especifica o número de destino dos nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="13389-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13389-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13389-133">-DefaultProfile</span></span>
<span data-ttu-id="13389-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13389-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13389-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13389-135">CommonParameters</span></span>
<span data-ttu-id="13389-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13389-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13389-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13389-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13389-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13389-138">INPUTS</span></span>

### <span data-ttu-id="13389-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="13389-139">BatchAccountContext</span></span>
<span data-ttu-id="13389-140">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="13389-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="13389-141">String</span><span class="sxs-lookup"><span data-stu-id="13389-141">String</span></span>
<span data-ttu-id="13389-142">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="13389-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="13389-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13389-143">OUTPUTS</span></span>

## <span data-ttu-id="13389-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13389-144">NOTES</span></span>

## <span data-ttu-id="13389-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13389-145">RELATED LINKS</span></span>

[<span data-ttu-id="13389-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="13389-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="13389-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="13389-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="13389-148">Parar-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="13389-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="13389-149">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="13389-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


