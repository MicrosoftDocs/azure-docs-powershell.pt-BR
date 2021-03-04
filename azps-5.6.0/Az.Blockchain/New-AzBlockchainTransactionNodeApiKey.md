---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885745"
---
# <span data-ttu-id="e8e42-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="e8e42-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="e8e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8e42-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e42-103">Regenerar as chaves da API para o membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="e8e42-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="e8e42-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8e42-104">SYNTAX</span></span>

### <span data-ttu-id="e8e42-105">RegenerateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8e42-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e8e42-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e8e42-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8e42-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8e42-107">DESCRIPTION</span></span>
<span data-ttu-id="e8e42-108">Regenerar as chaves da API para o membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="e8e42-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="e8e42-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8e42-109">EXAMPLES</span></span>

### <span data-ttu-id="e8e42-110">Exemplo 1: Regenerar chaves de Api para um nó de transação usando o nome.</span><span class="sxs-lookup"><span data-stu-id="e8e42-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="e8e42-111">Este comando gera chaves de Api para um nó de transação usando nome, grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8e42-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="e8e42-112">Exemplo 2: Regenerar chaves de Api para um nó de transação</span><span class="sxs-lookup"><span data-stu-id="e8e42-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="e8e42-113">Este comando gera chaves de Api para um nó de transação usando idenity.</span><span class="sxs-lookup"><span data-stu-id="e8e42-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="e8e42-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8e42-114">PARAMETERS</span></span>

### <span data-ttu-id="e8e42-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e8e42-115">-BlockchainMemberName</span></span>
<span data-ttu-id="e8e42-116">Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e8e42-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e42-117">-DefaultProfile</span></span>
<span data-ttu-id="e8e42-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e42-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e42-119">-InputObject</span></span>
<span data-ttu-id="e8e42-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e8e42-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e42-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e8e42-121">-KeyName</span></span>
<span data-ttu-id="e8e42-122">Obtém ou define o nome da chave da API.</span><span class="sxs-lookup"><span data-stu-id="e8e42-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="e8e42-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e42-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8e42-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e8e42-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e8e42-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e8e42-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e42-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8e42-126">-SubscriptionId</span></span>
<span data-ttu-id="e8e42-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e42-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e8e42-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e8e42-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e42-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="e8e42-129">-TransactionNodeName</span></span>
<span data-ttu-id="e8e42-130">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e8e42-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e42-131">-Value</span><span class="sxs-lookup"><span data-stu-id="e8e42-131">-Value</span></span>
<span data-ttu-id="e8e42-132">Obtém ou define o valor da chave da API.</span><span class="sxs-lookup"><span data-stu-id="e8e42-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="e8e42-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8e42-133">-Confirm</span></span>
<span data-ttu-id="e8e42-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8e42-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e42-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e42-135">-WhatIf</span></span>
<span data-ttu-id="e8e42-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8e42-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8e42-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8e42-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e42-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e42-138">CommonParameters</span></span>
<span data-ttu-id="e8e42-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e42-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e42-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8e42-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e42-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8e42-141">INPUTS</span></span>

### <span data-ttu-id="e8e42-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="e8e42-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="e8e42-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8e42-143">OUTPUTS</span></span>

### <span data-ttu-id="e8e42-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="e8e42-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="e8e42-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8e42-145">NOTES</span></span>

<span data-ttu-id="e8e42-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e8e42-146">ALIASES</span></span>

<span data-ttu-id="e8e42-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e8e42-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8e42-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e8e42-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8e42-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e8e42-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8e42-150">INPUTOBJECT <IBlockchainIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e8e42-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8e42-151">`[BlockchainMemberName <String>]`: Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e8e42-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="e8e42-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e8e42-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8e42-153">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="e8e42-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="e8e42-154">`[OperationId <String>]`: Id da operação.</span><span class="sxs-lookup"><span data-stu-id="e8e42-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="e8e42-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e8e42-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e8e42-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e8e42-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e8e42-157">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e42-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e8e42-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e8e42-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="e8e42-159">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e8e42-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="e8e42-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8e42-160">RELATED LINKS</span></span>

