---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111202"
---
# <span data-ttu-id="8adbb-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="8adbb-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="8adbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8adbb-102">SYNOPSIS</span></span>
<span data-ttu-id="8adbb-103">Excluir o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-103">Delete the transaction node.</span></span>

## <span data-ttu-id="8adbb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8adbb-104">SYNTAX</span></span>

### <span data-ttu-id="8adbb-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8adbb-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8adbb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8adbb-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8adbb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8adbb-107">DESCRIPTION</span></span>
<span data-ttu-id="8adbb-108">Excluir o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-108">Delete the transaction node.</span></span>

## <span data-ttu-id="8adbb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8adbb-109">EXAMPLES</span></span>

### <span data-ttu-id="8adbb-110">Exemplo 1: Remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="8adbb-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="8adbb-111">Esse comando remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="8adbb-112">Exemplo 2: Remover um nó de transação</span><span class="sxs-lookup"><span data-stu-id="8adbb-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="8adbb-113">Esse comando remove um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="8adbb-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8adbb-114">PARAMETERS</span></span>

### <span data-ttu-id="8adbb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8adbb-115">-AsJob</span></span>
<span data-ttu-id="8adbb-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8adbb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8adbb-117">-OmedoMember</span><span class="sxs-lookup"><span data-stu-id="8adbb-117">-BlockchainMemberName</span></span>
<span data-ttu-id="8adbb-118">Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="8adbb-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="8adbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8adbb-119">-DefaultProfile</span></span>
<span data-ttu-id="8adbb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8adbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8adbb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8adbb-121">-InputObject</span></span>
<span data-ttu-id="8adbb-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8adbb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8adbb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8adbb-123">-Name</span></span>
<span data-ttu-id="8adbb-124">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-124">Transaction node name.</span></span>

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

### <span data-ttu-id="8adbb-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8adbb-125">-NoWait</span></span>
<span data-ttu-id="8adbb-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="8adbb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8adbb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8adbb-127">-PassThru</span></span>
<span data-ttu-id="8adbb-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8adbb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8adbb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8adbb-129">-ResourceGroupName</span></span>
<span data-ttu-id="8adbb-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="8adbb-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8adbb-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="8adbb-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8adbb-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8adbb-132">-SubscriptionId</span></span>
<span data-ttu-id="8adbb-133">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8adbb-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8adbb-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8adbb-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8adbb-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8adbb-135">-Confirm</span></span>
<span data-ttu-id="8adbb-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8adbb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8adbb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8adbb-137">-WhatIf</span></span>
<span data-ttu-id="8adbb-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8adbb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8adbb-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8adbb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8adbb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8adbb-140">CommonParameters</span></span>
<span data-ttu-id="8adbb-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8adbb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8adbb-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8adbb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8adbb-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="8adbb-143">INPUTS</span></span>

### <span data-ttu-id="8adbb-144">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8adbb-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8adbb-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="8adbb-145">OUTPUTS</span></span>

### <span data-ttu-id="8adbb-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8adbb-146">System.Boolean</span></span>

## <span data-ttu-id="8adbb-147">Notas</span><span class="sxs-lookup"><span data-stu-id="8adbb-147">NOTES</span></span>

<span data-ttu-id="8adbb-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="8adbb-148">ALIASES</span></span>

<span data-ttu-id="8adbb-149">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8adbb-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8adbb-150">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8adbb-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8adbb-151">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8adbb-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8adbb-152">INPUTOBJECT: <IBlockchainIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8adbb-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8adbb-153">`[BlockchainMemberName <String>]`: Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="8adbb-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8adbb-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8adbb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8adbb-155">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="8adbb-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8adbb-156">`[OperationId <String>]`: ID da Operação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8adbb-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="8adbb-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8adbb-158">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="8adbb-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8adbb-159">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8adbb-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8adbb-160">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8adbb-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8adbb-161">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="8adbb-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8adbb-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8adbb-162">RELATED LINKS</span></span>

