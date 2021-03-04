---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: 15af3a6bb7e80020cd014bfbdd8ff944cafd187a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892821"
---
# <span data-ttu-id="64327-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="64327-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="64327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64327-102">SYNOPSIS</span></span>
<span data-ttu-id="64327-103">Criar um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64327-103">Create a blockchain member.</span></span>

## <span data-ttu-id="64327-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="64327-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64327-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="64327-105">DESCRIPTION</span></span>
<span data-ttu-id="64327-106">Criar um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64327-106">Create a blockchain member.</span></span>

## <span data-ttu-id="64327-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64327-107">EXAMPLES</span></span>

### <span data-ttu-id="64327-108">Exemplo 1: Criar um novo membro do bloco de dados</span><span class="sxs-lookup"><span data-stu-id="64327-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="64327-109">Este comando cria um novo membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64327-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="64327-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="64327-110">PARAMETERS</span></span>

### <span data-ttu-id="64327-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64327-111">-AsJob</span></span>
<span data-ttu-id="64327-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="64327-112">Run the command as a job</span></span>

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

### <span data-ttu-id="64327-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="64327-113">-Consortium</span></span>
<span data-ttu-id="64327-114">Obtém ou define o consorciado para o membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64327-114">Gets or sets the consortium for the blockchain member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="64327-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="64327-116">Define a senha da conta de gerenciamento de um consorciado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="64327-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="64327-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="64327-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="64327-118">Obtém o nome de exibição do membro no consorciado.</span><span class="sxs-lookup"><span data-stu-id="64327-118">Gets the display name of the member in the consortium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="64327-119">-ConsortiumRole</span></span>
<span data-ttu-id="64327-120">Obtém a função do membro no consorciado.</span><span class="sxs-lookup"><span data-stu-id="64327-120">Gets the role of the member in the consortium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64327-121">-DefaultProfile</span></span>
<span data-ttu-id="64327-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64327-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64327-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="64327-123">-FirewallRule</span></span>
<span data-ttu-id="64327-124">Obtém ou define regras de firewall Para construir, consulte a seção NOTES para propriedades FIREWALLRULE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="64327-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="64327-125">-Location</span><span class="sxs-lookup"><span data-stu-id="64327-125">-Location</span></span>
<span data-ttu-id="64327-126">A localização GEOGRÁFICA do serviço de blockchain.</span><span class="sxs-lookup"><span data-stu-id="64327-126">The GEO location of the blockchain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-127">-Name</span><span class="sxs-lookup"><span data-stu-id="64327-127">-Name</span></span>
<span data-ttu-id="64327-128">Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="64327-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64327-129">-NoWait</span></span>
<span data-ttu-id="64327-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="64327-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64327-131">-Password</span><span class="sxs-lookup"><span data-stu-id="64327-131">-Password</span></span>
<span data-ttu-id="64327-132">Define a senha básica de auth do membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64327-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="64327-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="64327-133">-Protocol</span></span>
<span data-ttu-id="64327-134">Obtém ou define o protocolo de blockchain.</span><span class="sxs-lookup"><span data-stu-id="64327-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64327-135">-ResourceGroupName</span></span>
<span data-ttu-id="64327-136">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="64327-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="64327-137">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="64327-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="64327-138">-Sku</span></span>
<span data-ttu-id="64327-139">Obtém ou define o nome Sku</span><span class="sxs-lookup"><span data-stu-id="64327-139">Gets or sets Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="64327-140">-SkuTier</span></span>
<span data-ttu-id="64327-141">Obtém ou define a camada Sku</span><span class="sxs-lookup"><span data-stu-id="64327-141">Gets or sets Sku tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64327-142">-SubscriptionId</span></span>
<span data-ttu-id="64327-143">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64327-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="64327-144">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="64327-144">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="64327-145">-Tag</span></span>
<span data-ttu-id="64327-146">Marcas do serviço que é uma lista de pares de valores-chave que descreve o recurso.</span><span class="sxs-lookup"><span data-stu-id="64327-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="64327-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="64327-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="64327-148">Obtém ou define a capacidade dos nós.</span><span class="sxs-lookup"><span data-stu-id="64327-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64327-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64327-149">-Confirm</span></span>
<span data-ttu-id="64327-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64327-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64327-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64327-151">-WhatIf</span></span>
<span data-ttu-id="64327-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64327-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64327-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64327-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64327-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64327-154">CommonParameters</span></span>
<span data-ttu-id="64327-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64327-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64327-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64327-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64327-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64327-157">INPUTS</span></span>

## <span data-ttu-id="64327-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="64327-158">OUTPUTS</span></span>

### <span data-ttu-id="64327-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="64327-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="64327-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="64327-160">NOTES</span></span>

<span data-ttu-id="64327-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="64327-161">ALIASES</span></span>

<span data-ttu-id="64327-162">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="64327-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64327-163">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="64327-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64327-164">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64327-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64327-165">FIREWALLRULE <IFirewallRule[]>: obtém ou define regras de firewall</span><span class="sxs-lookup"><span data-stu-id="64327-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="64327-166">`[EndIPAddress <String>]`: Obtém ou define o endereço IP final do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="64327-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="64327-167">`[RuleName <String>]`: Obtém ou define o nome das regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="64327-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="64327-168">`[StartIPAddress <String>]`: Obtém ou define o endereço IP inicial do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="64327-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="64327-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64327-169">RELATED LINKS</span></span>

