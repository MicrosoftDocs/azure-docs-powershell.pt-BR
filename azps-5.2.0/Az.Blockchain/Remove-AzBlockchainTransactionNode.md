---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263086"
---
# <span data-ttu-id="05fa5-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="05fa5-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="05fa5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="05fa5-103">Exclua o nó da transação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-103">Delete the transaction node.</span></span>

## <span data-ttu-id="05fa5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05fa5-104">SYNTAX</span></span>

### <span data-ttu-id="05fa5-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="05fa5-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="05fa5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05fa5-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05fa5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05fa5-107">DESCRIPTION</span></span>
<span data-ttu-id="05fa5-108">Exclua o nó da transação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-108">Delete the transaction node.</span></span>

## <span data-ttu-id="05fa5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05fa5-109">EXAMPLES</span></span>

### <span data-ttu-id="05fa5-110">Exemplo 1: remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="05fa5-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="05fa5-111">Esse comando Remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="05fa5-112">Exemplo 2: remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="05fa5-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="05fa5-113">Esse comando Remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="05fa5-114">OS</span><span class="sxs-lookup"><span data-stu-id="05fa5-114">PARAMETERS</span></span>

### <span data-ttu-id="05fa5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05fa5-115">-AsJob</span></span>
<span data-ttu-id="05fa5-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="05fa5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="05fa5-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="05fa5-117">-BlockchainMemberName</span></span>
<span data-ttu-id="05fa5-118">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="05fa5-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="05fa5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05fa5-119">-DefaultProfile</span></span>
<span data-ttu-id="05fa5-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05fa5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05fa5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05fa5-121">-InputObject</span></span>
<span data-ttu-id="05fa5-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="05fa5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05fa5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="05fa5-123">-Name</span></span>
<span data-ttu-id="05fa5-124">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-124">Transaction node name.</span></span>

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

### <span data-ttu-id="05fa5-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="05fa5-125">-NoWait</span></span>
<span data-ttu-id="05fa5-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="05fa5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="05fa5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05fa5-127">-PassThru</span></span>
<span data-ttu-id="05fa5-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="05fa5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="05fa5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05fa5-129">-ResourceGroupName</span></span>
<span data-ttu-id="05fa5-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="05fa5-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="05fa5-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="05fa5-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="05fa5-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05fa5-132">-SubscriptionId</span></span>
<span data-ttu-id="05fa5-133">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05fa5-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="05fa5-134">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="05fa5-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="05fa5-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05fa5-135">-Confirm</span></span>
<span data-ttu-id="05fa5-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05fa5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05fa5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05fa5-137">-WhatIf</span></span>
<span data-ttu-id="05fa5-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05fa5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05fa5-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05fa5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05fa5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05fa5-140">CommonParameters</span></span>
<span data-ttu-id="05fa5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05fa5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05fa5-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05fa5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05fa5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05fa5-143">INPUTS</span></span>

### <span data-ttu-id="05fa5-144">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="05fa5-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="05fa5-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05fa5-145">OUTPUTS</span></span>

### <span data-ttu-id="05fa5-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05fa5-146">System.Boolean</span></span>

## <span data-ttu-id="05fa5-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05fa5-147">NOTES</span></span>

<span data-ttu-id="05fa5-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="05fa5-148">ALIASES</span></span>

<span data-ttu-id="05fa5-149">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="05fa5-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05fa5-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="05fa5-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05fa5-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05fa5-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05fa5-152">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="05fa5-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05fa5-153">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="05fa5-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="05fa5-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="05fa5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05fa5-155">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="05fa5-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="05fa5-156">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="05fa5-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="05fa5-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="05fa5-158">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="05fa5-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="05fa5-159">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05fa5-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="05fa5-160">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="05fa5-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="05fa5-161">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="05fa5-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="05fa5-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05fa5-162">RELATED LINKS</span></span>

