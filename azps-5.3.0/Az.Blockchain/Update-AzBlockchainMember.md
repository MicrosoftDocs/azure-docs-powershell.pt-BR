---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430370"
---
# <span data-ttu-id="ff0fc-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="ff0fc-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="ff0fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0fc-103">Atualizar um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-103">Update a blockchain member.</span></span>

## <span data-ttu-id="ff0fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff0fc-104">SYNTAX</span></span>

### <span data-ttu-id="ff0fc-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff0fc-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ff0fc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ff0fc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0fc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff0fc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff0fc-108">Atualizar um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-108">Update a blockchain member.</span></span>

## <span data-ttu-id="ff0fc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff0fc-109">EXAMPLES</span></span>

### <span data-ttu-id="ff0fc-110">Exemplo 1: atualizar um membro do blockchain</span><span class="sxs-lookup"><span data-stu-id="ff0fc-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="ff0fc-111">Esse comando atualiza um membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="ff0fc-112">Exemplo 2: atualizar um membro do blockchain</span><span class="sxs-lookup"><span data-stu-id="ff0fc-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="ff0fc-113">Esse comando atualiza um membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="ff0fc-114">OS</span><span class="sxs-lookup"><span data-stu-id="ff0fc-114">PARAMETERS</span></span>

### <span data-ttu-id="ff0fc-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="ff0fc-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="ff0fc-116">Define a senha da conta de gerenciamento do consórcio gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="ff0fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0fc-117">-DefaultProfile</span></span>
<span data-ttu-id="ff0fc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0fc-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ff0fc-119">-FirewallRule</span></span>
<span data-ttu-id="ff0fc-120">Obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="ff0fc-121">Para construir, consulte a seção notas para propriedades FIREWALLRULE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff0fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff0fc-122">-InputObject</span></span>
<span data-ttu-id="ff0fc-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff0fc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff0fc-124">-Name</span></span>
<span data-ttu-id="ff0fc-125">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff0fc-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="ff0fc-126">-Password</span></span>
<span data-ttu-id="ff0fc-127">Define a senha de autenticação básica do ponto de extremidade de DNS do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="ff0fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="ff0fc-129">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ff0fc-130">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff0fc-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff0fc-131">-SubscriptionId</span></span>
<span data-ttu-id="ff0fc-132">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff0fc-133">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ff0fc-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="ff0fc-134">-Tag</span></span>
<span data-ttu-id="ff0fc-135">Marcas do serviço que é uma lista de pares de valores chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff0fc-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff0fc-136">-Confirm</span></span>
<span data-ttu-id="ff0fc-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0fc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0fc-138">-WhatIf</span></span>
<span data-ttu-id="ff0fc-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff0fc-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0fc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0fc-141">CommonParameters</span></span>
<span data-ttu-id="ff0fc-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0fc-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff0fc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0fc-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff0fc-144">INPUTS</span></span>

### <span data-ttu-id="ff0fc-145">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="ff0fc-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="ff0fc-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff0fc-146">OUTPUTS</span></span>

### <span data-ttu-id="ff0fc-147">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="ff0fc-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="ff0fc-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff0fc-148">NOTES</span></span>

<span data-ttu-id="ff0fc-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ff0fc-149">ALIASES</span></span>

<span data-ttu-id="ff0fc-150">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ff0fc-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff0fc-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff0fc-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff0fc-153">FIREWALLRULE <IFirewallRule [] >: Obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="ff0fc-154">`[EndIPAddress <String>]`: Obtém ou define o endereço IP final do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="ff0fc-155">`[RuleName <String>]`: Obtém ou define o nome das regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="ff0fc-156">`[StartIPAddress <String>]`: Obtém ou define o endereço IP inicial do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="ff0fc-157">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ff0fc-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff0fc-158">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="ff0fc-159">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ff0fc-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff0fc-160">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="ff0fc-161">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="ff0fc-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ff0fc-163">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ff0fc-164">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ff0fc-165">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="ff0fc-166">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="ff0fc-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="ff0fc-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff0fc-167">RELATED LINKS</span></span>

