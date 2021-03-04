---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: 3de49353a19afbce6ed8996fc5dd7cdeccca1627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890653"
---
# <span data-ttu-id="9104a-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="9104a-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="9104a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9104a-102">SYNOPSIS</span></span>
<span data-ttu-id="9104a-103">Exclua o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="9104a-103">Delete the transaction node.</span></span>

## <span data-ttu-id="9104a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9104a-104">SYNTAX</span></span>

### <span data-ttu-id="9104a-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9104a-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9104a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9104a-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9104a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9104a-107">DESCRIPTION</span></span>
<span data-ttu-id="9104a-108">Exclua o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="9104a-108">Delete the transaction node.</span></span>

## <span data-ttu-id="9104a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9104a-109">EXAMPLES</span></span>

### <span data-ttu-id="9104a-110">Exemplo 1: Remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="9104a-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="9104a-111">Este comando remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="9104a-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="9104a-112">Exemplo 2: Remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="9104a-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="9104a-113">Este comando remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="9104a-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="9104a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9104a-114">PARAMETERS</span></span>

### <span data-ttu-id="9104a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9104a-115">-AsJob</span></span>
<span data-ttu-id="9104a-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9104a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9104a-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="9104a-117">-BlockchainMemberName</span></span>
<span data-ttu-id="9104a-118">Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="9104a-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="9104a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9104a-119">-DefaultProfile</span></span>
<span data-ttu-id="9104a-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9104a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9104a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9104a-121">-InputObject</span></span>
<span data-ttu-id="9104a-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9104a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9104a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9104a-123">-Name</span></span>
<span data-ttu-id="9104a-124">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="9104a-124">Transaction node name.</span></span>

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

### <span data-ttu-id="9104a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9104a-125">-NoWait</span></span>
<span data-ttu-id="9104a-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9104a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9104a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9104a-127">-PassThru</span></span>
<span data-ttu-id="9104a-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9104a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9104a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9104a-129">-ResourceGroupName</span></span>
<span data-ttu-id="9104a-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="9104a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9104a-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="9104a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9104a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9104a-132">-SubscriptionId</span></span>
<span data-ttu-id="9104a-133">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9104a-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9104a-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9104a-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9104a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9104a-135">-Confirm</span></span>
<span data-ttu-id="9104a-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9104a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9104a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9104a-137">-WhatIf</span></span>
<span data-ttu-id="9104a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9104a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9104a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9104a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9104a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9104a-140">CommonParameters</span></span>
<span data-ttu-id="9104a-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9104a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9104a-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9104a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9104a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9104a-143">INPUTS</span></span>

### <span data-ttu-id="9104a-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="9104a-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="9104a-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9104a-145">OUTPUTS</span></span>

### <span data-ttu-id="9104a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9104a-146">System.Boolean</span></span>

## <span data-ttu-id="9104a-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="9104a-147">NOTES</span></span>

<span data-ttu-id="9104a-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9104a-148">ALIASES</span></span>

<span data-ttu-id="9104a-149">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="9104a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9104a-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9104a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9104a-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9104a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9104a-152">INPUTOBJECT <IBlockchainIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="9104a-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9104a-153">`[BlockchainMemberName <String>]`: Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="9104a-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="9104a-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9104a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9104a-155">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="9104a-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="9104a-156">`[OperationId <String>]`: Id da operação.</span><span class="sxs-lookup"><span data-stu-id="9104a-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="9104a-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="9104a-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9104a-158">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="9104a-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9104a-159">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9104a-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9104a-160">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9104a-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="9104a-161">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="9104a-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="9104a-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9104a-162">RELATED LINKS</span></span>

