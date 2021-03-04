---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: 78d3d6449eb5a487c6c4a8a60a732c30fa502600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887026"
---
# <span data-ttu-id="e2039-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="e2039-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="e2039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2039-102">SYNOPSIS</span></span>
<span data-ttu-id="e2039-103">Crie ou atualize o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e2039-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="e2039-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2039-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2039-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2039-105">DESCRIPTION</span></span>
<span data-ttu-id="e2039-106">Crie ou atualize o nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e2039-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="e2039-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2039-107">EXAMPLES</span></span>

### <span data-ttu-id="e2039-108">Exemplo 1: Criar um nó de transação de blockchain</span><span class="sxs-lookup"><span data-stu-id="e2039-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e2039-109">Este comando cria um nó de transação de bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="e2039-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="e2039-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2039-110">PARAMETERS</span></span>

### <span data-ttu-id="e2039-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2039-111">-AsJob</span></span>
<span data-ttu-id="e2039-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e2039-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e2039-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e2039-113">-BlockchainMemberName</span></span>
<span data-ttu-id="e2039-114">Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e2039-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="e2039-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2039-115">-DefaultProfile</span></span>
<span data-ttu-id="e2039-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2039-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2039-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="e2039-117">-FirewallRule</span></span>
<span data-ttu-id="e2039-118">Obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="e2039-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="e2039-119">Para construir, consulte a seção NOTES para propriedades FIREWALLRULE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e2039-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2039-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e2039-120">-Location</span></span>
<span data-ttu-id="e2039-121">Obtém ou define o local do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="e2039-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="e2039-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e2039-122">-Name</span></span>
<span data-ttu-id="e2039-123">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e2039-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2039-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e2039-124">-NoWait</span></span>
<span data-ttu-id="e2039-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e2039-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e2039-126">-Password</span><span class="sxs-lookup"><span data-stu-id="e2039-126">-Password</span></span>
<span data-ttu-id="e2039-127">Define a senha básica do ponto de extremidade dns do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e2039-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="e2039-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2039-128">-ResourceGroupName</span></span>
<span data-ttu-id="e2039-129">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e2039-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e2039-130">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e2039-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e2039-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2039-131">-SubscriptionId</span></span>
<span data-ttu-id="e2039-132">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e2039-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2039-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e2039-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2039-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2039-134">-Confirm</span></span>
<span data-ttu-id="e2039-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2039-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2039-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2039-136">-WhatIf</span></span>
<span data-ttu-id="e2039-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2039-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2039-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2039-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2039-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2039-139">CommonParameters</span></span>
<span data-ttu-id="e2039-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2039-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2039-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2039-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2039-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2039-142">INPUTS</span></span>

## <span data-ttu-id="e2039-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2039-143">OUTPUTS</span></span>

### <span data-ttu-id="e2039-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="e2039-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="e2039-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2039-145">NOTES</span></span>

<span data-ttu-id="e2039-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2039-146">ALIASES</span></span>

<span data-ttu-id="e2039-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e2039-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2039-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e2039-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2039-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2039-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2039-150">FIREWALLRULE <IFirewallRule[]>: obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="e2039-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="e2039-151">`[EndIPAddress <String>]`: Obtém ou define o endereço IP final do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="e2039-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="e2039-152">`[RuleName <String>]`: Obtém ou define o nome das regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="e2039-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="e2039-153">`[StartIPAddress <String>]`: Obtém ou define o endereço IP inicial do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="e2039-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="e2039-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2039-154">RELATED LINKS</span></span>

