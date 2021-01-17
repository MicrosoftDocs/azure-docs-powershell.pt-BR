---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434480"
---
# <span data-ttu-id="36fd3-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="36fd3-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="36fd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="36fd3-103">Criar ou atualizar o nó da transação.</span><span class="sxs-lookup"><span data-stu-id="36fd3-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="36fd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36fd3-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36fd3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="36fd3-106">Criar ou atualizar o nó da transação.</span><span class="sxs-lookup"><span data-stu-id="36fd3-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="36fd3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36fd3-107">EXAMPLES</span></span>

### <span data-ttu-id="36fd3-108">Exemplo 1: criar um nó de transação blockchain</span><span class="sxs-lookup"><span data-stu-id="36fd3-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="36fd3-109">Esse comando cria um nó de transação blockchain.</span><span class="sxs-lookup"><span data-stu-id="36fd3-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="36fd3-110">OS</span><span class="sxs-lookup"><span data-stu-id="36fd3-110">PARAMETERS</span></span>

### <span data-ttu-id="36fd3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36fd3-111">-AsJob</span></span>
<span data-ttu-id="36fd3-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="36fd3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="36fd3-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="36fd3-113">-BlockchainMemberName</span></span>
<span data-ttu-id="36fd3-114">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="36fd3-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="36fd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fd3-115">-DefaultProfile</span></span>
<span data-ttu-id="36fd3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36fd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36fd3-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="36fd3-117">-FirewallRule</span></span>
<span data-ttu-id="36fd3-118">Obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="36fd3-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="36fd3-119">Para construir, consulte a seção notas para propriedades FIREWALLRULE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="36fd3-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="36fd3-120">-Local</span><span class="sxs-lookup"><span data-stu-id="36fd3-120">-Location</span></span>
<span data-ttu-id="36fd3-121">Obtém ou define o local do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="36fd3-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="36fd3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="36fd3-122">-Name</span></span>
<span data-ttu-id="36fd3-123">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="36fd3-123">Transaction node name.</span></span>

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

### <span data-ttu-id="36fd3-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="36fd3-124">-NoWait</span></span>
<span data-ttu-id="36fd3-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="36fd3-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="36fd3-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="36fd3-126">-Password</span></span>
<span data-ttu-id="36fd3-127">Define a senha de autenticação básica do ponto de extremidade de DNS do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="36fd3-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="36fd3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36fd3-128">-ResourceGroupName</span></span>
<span data-ttu-id="36fd3-129">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="36fd3-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="36fd3-130">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="36fd3-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="36fd3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36fd3-131">-SubscriptionId</span></span>
<span data-ttu-id="36fd3-132">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="36fd3-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="36fd3-133">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="36fd3-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="36fd3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36fd3-134">-Confirm</span></span>
<span data-ttu-id="36fd3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36fd3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fd3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fd3-136">-WhatIf</span></span>
<span data-ttu-id="36fd3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36fd3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36fd3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36fd3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fd3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fd3-139">CommonParameters</span></span>
<span data-ttu-id="36fd3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36fd3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fd3-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36fd3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fd3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36fd3-142">INPUTS</span></span>

## <span data-ttu-id="36fd3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36fd3-143">OUTPUTS</span></span>

### <span data-ttu-id="36fd3-144">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="36fd3-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="36fd3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36fd3-145">NOTES</span></span>

<span data-ttu-id="36fd3-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36fd3-146">ALIASES</span></span>

<span data-ttu-id="36fd3-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="36fd3-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36fd3-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="36fd3-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36fd3-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36fd3-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36fd3-150">FIREWALLRULE <IFirewallRule [] >: Obtém ou define as regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="36fd3-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="36fd3-151">`[EndIPAddress <String>]`: Obtém ou define o endereço IP final do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="36fd3-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="36fd3-152">`[RuleName <String>]`: Obtém ou define o nome das regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="36fd3-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="36fd3-153">`[StartIPAddress <String>]`: Obtém ou define o endereço IP inicial do intervalo de regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="36fd3-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="36fd3-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36fd3-154">RELATED LINKS</span></span>

