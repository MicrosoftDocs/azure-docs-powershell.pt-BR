---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116599"
---
# <span data-ttu-id="4197e-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4197e-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="4197e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4197e-102">SYNOPSIS</span></span>
<span data-ttu-id="4197e-103">Exclui o pool de lotes especificado.</span><span class="sxs-lookup"><span data-stu-id="4197e-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="4197e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4197e-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4197e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4197e-105">DESCRIPTION</span></span>
<span data-ttu-id="4197e-106">O **cmdlet Remove-AzBatchPool** exclui o pool especificado do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4197e-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="4197e-107">Você será solicitado a confirmar, a menos que use o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="4197e-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="4197e-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4197e-108">EXAMPLES</span></span>

### <span data-ttu-id="4197e-109">Exemplo 1: Excluir um pool de lotes por ID do pool</span><span class="sxs-lookup"><span data-stu-id="4197e-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="4197e-110">Esse comando exclui o pool com o ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="4197e-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="4197e-111">O usuário será solicitado a confirmar antes que a operação de exclusão seja realizada.</span><span class="sxs-lookup"><span data-stu-id="4197e-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="4197e-112">Exemplo 2: Excluir todos os pools em lotes por força</span><span class="sxs-lookup"><span data-stu-id="4197e-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="4197e-113">Esse comando exclui todos os pools em lotes.</span><span class="sxs-lookup"><span data-stu-id="4197e-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="4197e-114">Como o *parâmetro Forçar* está presente, o prompt de confirmação é suprimido.</span><span class="sxs-lookup"><span data-stu-id="4197e-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="4197e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4197e-115">PARAMETERS</span></span>

### <span data-ttu-id="4197e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4197e-116">-BatchContext</span></span>
<span data-ttu-id="4197e-117">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="4197e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4197e-118">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="4197e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4197e-119">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="4197e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4197e-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="4197e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4197e-121">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4197e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4197e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4197e-122">-DefaultProfile</span></span>
<span data-ttu-id="4197e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4197e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4197e-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4197e-124">-Force</span></span>
<span data-ttu-id="4197e-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4197e-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4197e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4197e-126">-Id</span></span>
<span data-ttu-id="4197e-127">Especifica a ID do pool a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4197e-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="4197e-128">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="4197e-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="4197e-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4197e-129">-Confirm</span></span>
<span data-ttu-id="4197e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4197e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4197e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4197e-131">-WhatIf</span></span>
<span data-ttu-id="4197e-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4197e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4197e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4197e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4197e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4197e-134">CommonParameters</span></span>
<span data-ttu-id="4197e-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4197e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4197e-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4197e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4197e-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="4197e-137">INPUTS</span></span>

### <span data-ttu-id="4197e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4197e-138">System.String</span></span>

### <span data-ttu-id="4197e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4197e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4197e-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="4197e-140">OUTPUTS</span></span>

### <span data-ttu-id="4197e-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="4197e-141">System.Void</span></span>

## <span data-ttu-id="4197e-142">Notas</span><span class="sxs-lookup"><span data-stu-id="4197e-142">NOTES</span></span>

## <span data-ttu-id="4197e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4197e-143">RELATED LINKS</span></span>

[<span data-ttu-id="4197e-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4197e-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4197e-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4197e-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="4197e-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4197e-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="4197e-147">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="4197e-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
