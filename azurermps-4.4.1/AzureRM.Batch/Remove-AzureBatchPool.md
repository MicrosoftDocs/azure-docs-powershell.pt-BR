---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431137"
---
# <span data-ttu-id="7ebbd-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7ebbd-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="7ebbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ebbd-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebbd-103">Exclui o pool de lotes especificado.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ebbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ebbd-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ebbd-105">DESCRIPTION</span></span>
<span data-ttu-id="7ebbd-106">O cmdlet **Remove-AzureBatchPool** exclui o pool de lotes do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="7ebbd-107">Você será solicitado a confirmar, a menos que use o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="7ebbd-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="7ebbd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ebbd-108">EXAMPLES</span></span>

### <span data-ttu-id="7ebbd-109">Exemplo 1: excluir um pool de lotes por ID do pool</span><span class="sxs-lookup"><span data-stu-id="7ebbd-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="7ebbd-110">Esse comando exclui o pool com ID mypool.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="7ebbd-111">O usuário será solicitado a confirmar a confirmação antes que a operação de exclusão ocorra.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="7ebbd-112">Exemplo 2: excluir todos os pools de lotes por força</span><span class="sxs-lookup"><span data-stu-id="7ebbd-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="7ebbd-113">Esse comando exclui todos os pools de lotes.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="7ebbd-114">Como o parâmetro *Force* está presente, o prompt de confirmação é suprimido.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="7ebbd-115">OS</span><span class="sxs-lookup"><span data-stu-id="7ebbd-115">PARAMETERS</span></span>

### <span data-ttu-id="7ebbd-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7ebbd-116">-BatchContext</span></span>
<span data-ttu-id="7ebbd-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7ebbd-118">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7ebbd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7ebbd-119">-Force</span></span>
<span data-ttu-id="7ebbd-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebbd-121">-ID</span><span class="sxs-lookup"><span data-stu-id="7ebbd-121">-Id</span></span>
<span data-ttu-id="7ebbd-122">Especifica a ID do pool a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="7ebbd-123">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-123">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="7ebbd-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ebbd-124">-Confirm</span></span>
<span data-ttu-id="7ebbd-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebbd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebbd-126">-WhatIf</span></span>
<span data-ttu-id="7ebbd-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebbd-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebbd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebbd-129">-DefaultProfile</span></span>
<span data-ttu-id="7ebbd-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ebbd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebbd-131">CommonParameters</span></span>
<span data-ttu-id="7ebbd-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebbd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebbd-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebbd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebbd-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ebbd-134">INPUTS</span></span>

### <span data-ttu-id="7ebbd-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7ebbd-135">BatchAccountContext</span></span>
<span data-ttu-id="7ebbd-136">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7ebbd-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="7ebbd-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ebbd-137">OUTPUTS</span></span>

## <span data-ttu-id="7ebbd-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ebbd-138">NOTES</span></span>

## <span data-ttu-id="7ebbd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ebbd-139">RELATED LINKS</span></span>

[<span data-ttu-id="7ebbd-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7ebbd-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7ebbd-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7ebbd-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="7ebbd-142">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7ebbd-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="7ebbd-143">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="7ebbd-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


