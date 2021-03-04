---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 53178cf8e9eb38024e264aaeb2378349ba3dfa03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887819"
---
# <span data-ttu-id="e586c-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="e586c-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="e586c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e586c-102">SYNOPSIS</span></span>
<span data-ttu-id="e586c-103">Obter os detalhes do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e586c-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="e586c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e586c-104">SYNTAX</span></span>

### <span data-ttu-id="e586c-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e586c-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e586c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e586c-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e586c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e586c-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e586c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e586c-108">DESCRIPTION</span></span>
<span data-ttu-id="e586c-109">Obter os detalhes do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e586c-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="e586c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e586c-110">EXAMPLES</span></span>

### <span data-ttu-id="e586c-111">Exemplo 1: Listar nós de transação para um membro do bloco de dados</span><span class="sxs-lookup"><span data-stu-id="e586c-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e586c-112">Este comando lista nós de transação para um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="e586c-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="e586c-113">Exemplo 2: Obter um nó de transação</span><span class="sxs-lookup"><span data-stu-id="e586c-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e586c-114">Este comando obtém um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e586c-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="e586c-115">Exemplo 3: Obter um nó de transação</span><span class="sxs-lookup"><span data-stu-id="e586c-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e586c-116">Este comando obtém um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e586c-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="e586c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e586c-117">PARAMETERS</span></span>

### <span data-ttu-id="e586c-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e586c-118">-BlockchainMemberName</span></span>
<span data-ttu-id="e586c-119">Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e586c-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e586c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e586c-120">-DefaultProfile</span></span>
<span data-ttu-id="e586c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e586c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e586c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e586c-122">-InputObject</span></span>
<span data-ttu-id="e586c-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e586c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e586c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e586c-124">-Name</span></span>
<span data-ttu-id="e586c-125">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e586c-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e586c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e586c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e586c-127">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e586c-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e586c-128">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e586c-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e586c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e586c-129">-SubscriptionId</span></span>
<span data-ttu-id="e586c-130">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e586c-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e586c-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e586c-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e586c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e586c-132">CommonParameters</span></span>
<span data-ttu-id="e586c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e586c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e586c-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e586c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e586c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e586c-135">INPUTS</span></span>

### <span data-ttu-id="e586c-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="e586c-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="e586c-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e586c-137">OUTPUTS</span></span>

### <span data-ttu-id="e586c-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="e586c-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="e586c-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="e586c-139">NOTES</span></span>

<span data-ttu-id="e586c-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e586c-140">ALIASES</span></span>

<span data-ttu-id="e586c-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e586c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e586c-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e586c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e586c-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e586c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e586c-144">INPUTOBJECT <IBlockchainIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e586c-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e586c-145">`[BlockchainMemberName <String>]`: Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e586c-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="e586c-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e586c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e586c-147">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="e586c-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="e586c-148">`[OperationId <String>]`: Id da operação.</span><span class="sxs-lookup"><span data-stu-id="e586c-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="e586c-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e586c-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e586c-150">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e586c-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e586c-151">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e586c-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e586c-152">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e586c-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="e586c-153">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e586c-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="e586c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e586c-154">RELATED LINKS</span></span>

