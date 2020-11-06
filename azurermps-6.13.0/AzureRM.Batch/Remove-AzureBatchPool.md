---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 4cfb497b98d20b5cf3741c90934e9e104b93ddcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427296"
---
# <span data-ttu-id="b9473-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9473-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="b9473-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9473-102">SYNOPSIS</span></span>
<span data-ttu-id="b9473-103">Exclui o pool de lotes especificado.</span><span class="sxs-lookup"><span data-stu-id="b9473-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9473-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9473-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9473-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9473-105">DESCRIPTION</span></span>
<span data-ttu-id="b9473-106">O cmdlet **Remove-AzureBatchPool** exclui o pool de lotes do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="b9473-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="b9473-107">Você será solicitado a confirmar, a menos que use o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="b9473-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="b9473-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9473-108">EXAMPLES</span></span>

### <span data-ttu-id="b9473-109">Exemplo 1: excluir um pool de lotes por ID do pool</span><span class="sxs-lookup"><span data-stu-id="b9473-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="b9473-110">Esse comando exclui o pool com ID mypool.</span><span class="sxs-lookup"><span data-stu-id="b9473-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="b9473-111">O usuário será solicitado a confirmar a confirmação antes que a operação de exclusão ocorra.</span><span class="sxs-lookup"><span data-stu-id="b9473-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="b9473-112">Exemplo 2: excluir todos os pools de lotes por força</span><span class="sxs-lookup"><span data-stu-id="b9473-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="b9473-113">Esse comando exclui todos os pools de lotes.</span><span class="sxs-lookup"><span data-stu-id="b9473-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="b9473-114">Como o parâmetro *Force* está presente, o prompt de confirmação é suprimido.</span><span class="sxs-lookup"><span data-stu-id="b9473-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="b9473-115">OS</span><span class="sxs-lookup"><span data-stu-id="b9473-115">PARAMETERS</span></span>

### <span data-ttu-id="b9473-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b9473-116">-BatchContext</span></span>
<span data-ttu-id="b9473-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b9473-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b9473-118">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b9473-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b9473-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="b9473-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b9473-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b9473-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b9473-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b9473-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b9473-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9473-122">-DefaultProfile</span></span>
<span data-ttu-id="b9473-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9473-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9473-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b9473-124">-Force</span></span>
<span data-ttu-id="b9473-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9473-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9473-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b9473-126">-Id</span></span>
<span data-ttu-id="b9473-127">Especifica a ID do pool a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="b9473-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="b9473-128">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="b9473-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b9473-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9473-129">-Confirm</span></span>
<span data-ttu-id="b9473-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9473-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9473-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9473-131">-WhatIf</span></span>
<span data-ttu-id="b9473-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9473-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9473-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9473-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9473-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9473-134">CommonParameters</span></span>
<span data-ttu-id="b9473-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9473-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9473-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9473-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9473-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9473-137">INPUTS</span></span>

### <span data-ttu-id="b9473-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9473-138">System.String</span></span>

### <span data-ttu-id="b9473-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b9473-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b9473-140">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9473-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b9473-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9473-141">OUTPUTS</span></span>

### <span data-ttu-id="b9473-142">System. void</span><span class="sxs-lookup"><span data-stu-id="b9473-142">System.Void</span></span>

## <span data-ttu-id="b9473-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9473-143">NOTES</span></span>

## <span data-ttu-id="b9473-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9473-144">RELATED LINKS</span></span>

[<span data-ttu-id="b9473-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b9473-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b9473-146">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9473-146">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="b9473-147">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9473-147">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="b9473-148">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="b9473-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


