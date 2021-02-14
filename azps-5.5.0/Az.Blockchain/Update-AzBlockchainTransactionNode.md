---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111190"
---
# <span data-ttu-id="62c7a-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="62c7a-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="62c7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="62c7a-103">Atualize o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-103">Update the transaction node.</span></span>

## <span data-ttu-id="62c7a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62c7a-104">SYNTAX</span></span>

### <span data-ttu-id="62c7a-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62c7a-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62c7a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="62c7a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62c7a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="62c7a-107">DESCRIPTION</span></span>
<span data-ttu-id="62c7a-108">Atualize o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-108">Update the transaction node.</span></span>

## <span data-ttu-id="62c7a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62c7a-109">EXAMPLES</span></span>

### <span data-ttu-id="62c7a-110">Exemplo 1: Atualizar um nó de transcação</span><span class="sxs-lookup"><span data-stu-id="62c7a-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="62c7a-111">Esse comando atualiza um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="62c7a-112">Exemplo 2: Atualizar um nó de transcação</span><span class="sxs-lookup"><span data-stu-id="62c7a-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="62c7a-113">Esse comando atualiza um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="62c7a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62c7a-114">PARAMETERS</span></span>

### <span data-ttu-id="62c7a-115">-OmedoMember</span><span class="sxs-lookup"><span data-stu-id="62c7a-115">-BlockchainMemberName</span></span>
<span data-ttu-id="62c7a-116">Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="62c7a-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c7a-117">-DefaultProfile</span></span>
<span data-ttu-id="62c7a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62c7a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c7a-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="62c7a-119">-FirewallRule</span></span>
<span data-ttu-id="62c7a-120">Obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="62c7a-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="62c7a-121">Para construir, consulte a seção ANOTAÇÕES para propriedades FIREWALLRULE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="62c7a-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62c7a-122">-InputObject</span></span>
<span data-ttu-id="62c7a-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="62c7a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="62c7a-124">-Name</span></span>
<span data-ttu-id="62c7a-125">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="62c7a-126">-Password</span></span>
<span data-ttu-id="62c7a-127">Define a senha básica de auth do ponto de extremidade dns do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-127">Sets the transaction node dns endpoint basic auth password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c7a-128">-ResourceGroupName</span></span>
<span data-ttu-id="62c7a-129">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="62c7a-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="62c7a-130">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="62c7a-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62c7a-131">-SubscriptionId</span></span>
<span data-ttu-id="62c7a-132">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="62c7a-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="62c7a-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="62c7a-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c7a-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62c7a-134">-Confirm</span></span>
<span data-ttu-id="62c7a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62c7a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c7a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c7a-136">-WhatIf</span></span>
<span data-ttu-id="62c7a-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62c7a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c7a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62c7a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c7a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c7a-139">CommonParameters</span></span>
<span data-ttu-id="62c7a-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c7a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c7a-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62c7a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c7a-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="62c7a-142">INPUTS</span></span>

### <span data-ttu-id="62c7a-143">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="62c7a-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="62c7a-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="62c7a-144">OUTPUTS</span></span>

### <span data-ttu-id="62c7a-145">Microsoft.Azure.PowerShell.Cmdlets.Ltd.Model.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="62c7a-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="62c7a-146">Notas</span><span class="sxs-lookup"><span data-stu-id="62c7a-146">NOTES</span></span>

<span data-ttu-id="62c7a-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="62c7a-147">ALIASES</span></span>

<span data-ttu-id="62c7a-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="62c7a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62c7a-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="62c7a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62c7a-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62c7a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62c7a-151">FIREWALLRULE <IFirewallRule[]>: obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="62c7a-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="62c7a-152">`[EndIPAddress <String>]`: obtém ou define o endereço IP final do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="62c7a-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="62c7a-153">`[RuleName <String>]`: Obtém ou define o nome das regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="62c7a-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="62c7a-154">`[StartIPAddress <String>]`: obtém ou define o endereço IP inicial do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="62c7a-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="62c7a-155">INPUTOBJECT: <IBlockchainIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="62c7a-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62c7a-156">`[BlockchainMemberName <String>]`: Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="62c7a-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="62c7a-157">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="62c7a-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62c7a-158">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="62c7a-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="62c7a-159">`[OperationId <String>]`: ID da Operação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="62c7a-160">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="62c7a-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="62c7a-161">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="62c7a-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="62c7a-162">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="62c7a-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="62c7a-163">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="62c7a-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="62c7a-164">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="62c7a-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="62c7a-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62c7a-165">RELATED LINKS</span></span>

