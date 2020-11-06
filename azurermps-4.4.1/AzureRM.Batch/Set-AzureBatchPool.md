---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431804"
---
# <span data-ttu-id="38aa0-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="38aa0-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="38aa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="38aa0-103">Atualiza as propriedades de um pool.</span><span class="sxs-lookup"><span data-stu-id="38aa0-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38aa0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38aa0-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38aa0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="38aa0-106">O cmdlet **set-AzureBatchPool** atualiza as propriedades de um pool no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="38aa0-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="38aa0-107">Use o cmdlet Get-AzureBatchPool para obter um objeto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="38aa0-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="38aa0-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="38aa0-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="38aa0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38aa0-109">EXAMPLES</span></span>

### <span data-ttu-id="38aa0-110">Exemplo 1: atualizar um pool</span><span class="sxs-lookup"><span data-stu-id="38aa0-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="38aa0-111">O primeiro comando obtém um pool usando **Get-AzureBatchPool** e, em seguida, armazena-o na variável $pool.</span><span class="sxs-lookup"><span data-stu-id="38aa0-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="38aa0-112">Os próximos três comandos modificam a especificação Start Task no objeto $Pool.</span><span class="sxs-lookup"><span data-stu-id="38aa0-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="38aa0-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Pool.</span><span class="sxs-lookup"><span data-stu-id="38aa0-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="38aa0-114">OS</span><span class="sxs-lookup"><span data-stu-id="38aa0-114">PARAMETERS</span></span>

### <span data-ttu-id="38aa0-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="38aa0-115">-BatchContext</span></span>
<span data-ttu-id="38aa0-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="38aa0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="38aa0-117">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="38aa0-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="38aa0-118">-Pool</span><span class="sxs-lookup"><span data-stu-id="38aa0-118">-Pool</span></span>
<span data-ttu-id="38aa0-119">Especifica o **PSCloudPool** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="38aa0-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38aa0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38aa0-120">-DefaultProfile</span></span>
<span data-ttu-id="38aa0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38aa0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38aa0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38aa0-122">CommonParameters</span></span>
<span data-ttu-id="38aa0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38aa0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38aa0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38aa0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38aa0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38aa0-125">INPUTS</span></span>

### <span data-ttu-id="38aa0-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="38aa0-126">BatchAccountContext</span></span>
<span data-ttu-id="38aa0-127">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="38aa0-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="38aa0-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="38aa0-128">PSCloudPool</span></span>
<span data-ttu-id="38aa0-129">O parâmetro ' Pool ' aceita o valor do tipo ' PSCloudPool ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="38aa0-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="38aa0-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38aa0-130">OUTPUTS</span></span>

## <span data-ttu-id="38aa0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38aa0-131">NOTES</span></span>

## <span data-ttu-id="38aa0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38aa0-132">RELATED LINKS</span></span>

[<span data-ttu-id="38aa0-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="38aa0-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="38aa0-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="38aa0-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="38aa0-135">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="38aa0-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="38aa0-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="38aa0-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="38aa0-137">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="38aa0-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


