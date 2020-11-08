---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125043"
---
# <span data-ttu-id="42294-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="42294-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="42294-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42294-102">SYNOPSIS</span></span>
<span data-ttu-id="42294-103">Exclua o nó da transação.</span><span class="sxs-lookup"><span data-stu-id="42294-103">Delete the transaction node.</span></span>

## <span data-ttu-id="42294-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42294-104">SYNTAX</span></span>

### <span data-ttu-id="42294-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="42294-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="42294-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="42294-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="42294-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42294-107">DESCRIPTION</span></span>
<span data-ttu-id="42294-108">Exclua o nó da transação.</span><span class="sxs-lookup"><span data-stu-id="42294-108">Delete the transaction node.</span></span>

## <span data-ttu-id="42294-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42294-109">EXAMPLES</span></span>

### <span data-ttu-id="42294-110">Exemplo 1: remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="42294-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="42294-111">Esse comando Remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="42294-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="42294-112">Exemplo 2: remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="42294-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="42294-113">Esse comando Remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="42294-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="42294-114">OS</span><span class="sxs-lookup"><span data-stu-id="42294-114">PARAMETERS</span></span>

### <span data-ttu-id="42294-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42294-115">-AsJob</span></span>
<span data-ttu-id="42294-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="42294-116">Run the command as a job</span></span>

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

### <span data-ttu-id="42294-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="42294-117">-BlockchainMemberName</span></span>
<span data-ttu-id="42294-118">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="42294-118">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42294-119">-DefaultProfile</span></span>
<span data-ttu-id="42294-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42294-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42294-121">-InputObject</span></span>
<span data-ttu-id="42294-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="42294-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42294-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="42294-123">-Name</span></span>
<span data-ttu-id="42294-124">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="42294-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="42294-125">-NoWait</span></span>
<span data-ttu-id="42294-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="42294-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="42294-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42294-127">-PassThru</span></span>
<span data-ttu-id="42294-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="42294-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="42294-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42294-129">-ResourceGroupName</span></span>
<span data-ttu-id="42294-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="42294-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="42294-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="42294-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42294-132">-SubscriptionId</span></span>
<span data-ttu-id="42294-133">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="42294-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="42294-134">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="42294-134">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42294-135">-Confirm</span></span>
<span data-ttu-id="42294-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42294-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42294-137">-WhatIf</span></span>
<span data-ttu-id="42294-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42294-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42294-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42294-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42294-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42294-140">CommonParameters</span></span>
<span data-ttu-id="42294-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42294-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42294-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42294-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42294-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42294-143">INPUTS</span></span>

### <span data-ttu-id="42294-144">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="42294-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="42294-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42294-145">OUTPUTS</span></span>

### <span data-ttu-id="42294-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42294-146">System.Boolean</span></span>

## <span data-ttu-id="42294-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42294-147">NOTES</span></span>

<span data-ttu-id="42294-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="42294-148">ALIASES</span></span>

<span data-ttu-id="42294-149">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="42294-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42294-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="42294-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42294-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="42294-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42294-152">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="42294-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="42294-153">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="42294-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="42294-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="42294-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="42294-155">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="42294-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="42294-156">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="42294-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="42294-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="42294-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="42294-158">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="42294-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="42294-159">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="42294-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="42294-160">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="42294-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="42294-161">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="42294-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="42294-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42294-162">RELATED LINKS</span></span>

