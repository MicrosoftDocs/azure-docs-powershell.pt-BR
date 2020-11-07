---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955100"
---
# <span data-ttu-id="fcc77-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="fcc77-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="fcc77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcc77-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc77-103">Regenerar as chaves de API do membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="fcc77-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="fcc77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcc77-104">SYNTAX</span></span>

### <span data-ttu-id="fcc77-105">RegenerateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="fcc77-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fcc77-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fcc77-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fcc77-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcc77-107">DESCRIPTION</span></span>
<span data-ttu-id="fcc77-108">Regenerar as chaves de API do membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="fcc77-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="fcc77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcc77-109">EXAMPLES</span></span>

### <span data-ttu-id="fcc77-110">Exemplo 1: regenerar chaves de API para um nó de transação usando name.</span><span class="sxs-lookup"><span data-stu-id="fcc77-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="fcc77-111">Esse comando gera chaves de API para um nó de transação usando o nome, o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcc77-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="fcc77-112">Exemplo 2: regenerar chaves de API para um nó de transação</span><span class="sxs-lookup"><span data-stu-id="fcc77-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="fcc77-113">Esse comando gera chaves de API para um nó de transação usando idenity.</span><span class="sxs-lookup"><span data-stu-id="fcc77-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="fcc77-114">OS</span><span class="sxs-lookup"><span data-stu-id="fcc77-114">PARAMETERS</span></span>

### <span data-ttu-id="fcc77-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="fcc77-115">-BlockchainMemberName</span></span>
<span data-ttu-id="fcc77-116">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="fcc77-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="fcc77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc77-117">-DefaultProfile</span></span>
<span data-ttu-id="fcc77-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcc77-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcc77-119">-InputObject</span></span>
<span data-ttu-id="fcc77-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fcc77-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fcc77-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fcc77-121">-KeyName</span></span>
<span data-ttu-id="fcc77-122">Obtém ou define o nome da chave da API.</span><span class="sxs-lookup"><span data-stu-id="fcc77-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="fcc77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc77-123">-ResourceGroupName</span></span>
<span data-ttu-id="fcc77-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="fcc77-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fcc77-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="fcc77-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fcc77-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fcc77-126">-SubscriptionId</span></span>
<span data-ttu-id="fcc77-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc77-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fcc77-128">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fcc77-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fcc77-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="fcc77-129">-TransactionNodeName</span></span>
<span data-ttu-id="fcc77-130">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="fcc77-130">Transaction node name.</span></span>

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

### <span data-ttu-id="fcc77-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="fcc77-131">-Value</span></span>
<span data-ttu-id="fcc77-132">Obtém ou define o valor da chave da API.</span><span class="sxs-lookup"><span data-stu-id="fcc77-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="fcc77-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcc77-133">-Confirm</span></span>
<span data-ttu-id="fcc77-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcc77-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc77-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc77-135">-WhatIf</span></span>
<span data-ttu-id="fcc77-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcc77-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc77-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcc77-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc77-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc77-138">CommonParameters</span></span>
<span data-ttu-id="fcc77-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc77-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc77-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcc77-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc77-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcc77-141">INPUTS</span></span>

### <span data-ttu-id="fcc77-142">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="fcc77-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="fcc77-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcc77-143">OUTPUTS</span></span>

### <span data-ttu-id="fcc77-144">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="fcc77-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="fcc77-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcc77-145">NOTES</span></span>

<span data-ttu-id="fcc77-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fcc77-146">ALIASES</span></span>

<span data-ttu-id="fcc77-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fcc77-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fcc77-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fcc77-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcc77-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fcc77-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fcc77-150">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fcc77-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fcc77-151">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="fcc77-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="fcc77-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fcc77-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fcc77-153">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="fcc77-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="fcc77-154">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="fcc77-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="fcc77-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="fcc77-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fcc77-156">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="fcc77-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fcc77-157">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc77-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="fcc77-158">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fcc77-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="fcc77-159">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="fcc77-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="fcc77-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcc77-160">RELATED LINKS</span></span>

