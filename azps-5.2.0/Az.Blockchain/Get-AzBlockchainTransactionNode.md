---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259693"
---
# <span data-ttu-id="97e4e-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="97e4e-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="97e4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="97e4e-103">Obtenha os detalhes do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="97e4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97e4e-104">SYNTAX</span></span>

### <span data-ttu-id="97e4e-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="97e4e-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97e4e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="97e4e-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97e4e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97e4e-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="97e4e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97e4e-108">DESCRIPTION</span></span>
<span data-ttu-id="97e4e-109">Obtenha os detalhes do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="97e4e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97e4e-110">EXAMPLES</span></span>

### <span data-ttu-id="97e4e-111">Exemplo 1: listar nós de transação para um membro de blockchain</span><span class="sxs-lookup"><span data-stu-id="97e4e-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="97e4e-112">Esse comando lista os nós de transação para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="97e4e-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="97e4e-113">Exemplo 2: obter um nó de transação</span><span class="sxs-lookup"><span data-stu-id="97e4e-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="97e4e-114">Esse comando obtém um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="97e4e-115">Exemplo 3: obter um nó de transação</span><span class="sxs-lookup"><span data-stu-id="97e4e-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="97e4e-116">Esse comando obtém um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="97e4e-117">OS</span><span class="sxs-lookup"><span data-stu-id="97e4e-117">PARAMETERS</span></span>

### <span data-ttu-id="97e4e-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="97e4e-118">-BlockchainMemberName</span></span>
<span data-ttu-id="97e4e-119">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="97e4e-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="97e4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e4e-120">-DefaultProfile</span></span>
<span data-ttu-id="97e4e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97e4e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e4e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97e4e-122">-InputObject</span></span>
<span data-ttu-id="97e4e-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="97e4e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97e4e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="97e4e-124">-Name</span></span>
<span data-ttu-id="97e4e-125">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-125">Transaction node name.</span></span>

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

### <span data-ttu-id="97e4e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e4e-126">-ResourceGroupName</span></span>
<span data-ttu-id="97e4e-127">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="97e4e-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="97e4e-128">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="97e4e-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="97e4e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97e4e-129">-SubscriptionId</span></span>
<span data-ttu-id="97e4e-130">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97e4e-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="97e4e-131">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="97e4e-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="97e4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e4e-132">CommonParameters</span></span>
<span data-ttu-id="97e4e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e4e-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97e4e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e4e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97e4e-135">INPUTS</span></span>

### <span data-ttu-id="97e4e-136">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="97e4e-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="97e4e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97e4e-137">OUTPUTS</span></span>

### <span data-ttu-id="97e4e-138">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="97e4e-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="97e4e-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97e4e-139">NOTES</span></span>

<span data-ttu-id="97e4e-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97e4e-140">ALIASES</span></span>

<span data-ttu-id="97e4e-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="97e4e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97e4e-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="97e4e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97e4e-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97e4e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97e4e-144">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="97e4e-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97e4e-145">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="97e4e-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="97e4e-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="97e4e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97e4e-147">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="97e4e-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="97e4e-148">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="97e4e-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="97e4e-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="97e4e-150">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="97e4e-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="97e4e-151">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97e4e-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="97e4e-152">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="97e4e-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="97e4e-153">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="97e4e-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="97e4e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97e4e-154">RELATED LINKS</span></span>

