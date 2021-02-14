---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116947"
---
# <span data-ttu-id="47089-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="47089-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="47089-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47089-102">SYNOPSIS</span></span>
<span data-ttu-id="47089-103">Obter os detalhes do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="47089-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="47089-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47089-104">SYNTAX</span></span>

### <span data-ttu-id="47089-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47089-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47089-106">Obter</span><span class="sxs-lookup"><span data-stu-id="47089-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47089-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47089-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47089-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="47089-108">DESCRIPTION</span></span>
<span data-ttu-id="47089-109">Obter os detalhes do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="47089-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="47089-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47089-110">EXAMPLES</span></span>

### <span data-ttu-id="47089-111">Exemplo 1: Nós de transação de lista para um membro da lista</span><span class="sxs-lookup"><span data-stu-id="47089-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="47089-112">Este comando lista nós de transação para um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="47089-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="47089-113">Exemplo 2: Obter um nó de transação</span><span class="sxs-lookup"><span data-stu-id="47089-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="47089-114">Esse comando obtém um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="47089-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="47089-115">Exemplo 3: Obter um nó de transação</span><span class="sxs-lookup"><span data-stu-id="47089-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="47089-116">Esse comando obtém um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="47089-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="47089-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47089-117">PARAMETERS</span></span>

### <span data-ttu-id="47089-118">-OmedoMember</span><span class="sxs-lookup"><span data-stu-id="47089-118">-BlockchainMemberName</span></span>
<span data-ttu-id="47089-119">Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="47089-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="47089-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47089-120">-DefaultProfile</span></span>
<span data-ttu-id="47089-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47089-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47089-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47089-122">-InputObject</span></span>
<span data-ttu-id="47089-123">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="47089-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47089-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="47089-124">-Name</span></span>
<span data-ttu-id="47089-125">Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="47089-125">Transaction node name.</span></span>

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

### <span data-ttu-id="47089-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47089-126">-ResourceGroupName</span></span>
<span data-ttu-id="47089-127">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="47089-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="47089-128">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="47089-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="47089-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47089-129">-SubscriptionId</span></span>
<span data-ttu-id="47089-130">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47089-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47089-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="47089-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47089-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47089-132">CommonParameters</span></span>
<span data-ttu-id="47089-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47089-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47089-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47089-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47089-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="47089-135">INPUTS</span></span>

### <span data-ttu-id="47089-136">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="47089-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="47089-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="47089-137">OUTPUTS</span></span>

### <span data-ttu-id="47089-138">Microsoft.Azure.PowerShell.Cmdlets.Ltd.Model.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="47089-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="47089-139">Notas</span><span class="sxs-lookup"><span data-stu-id="47089-139">NOTES</span></span>

<span data-ttu-id="47089-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="47089-140">ALIASES</span></span>

<span data-ttu-id="47089-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="47089-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47089-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="47089-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47089-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47089-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47089-144">INPUTOBJECT: <IBlockchainIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="47089-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47089-145">`[BlockchainMemberName <String>]`: Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="47089-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="47089-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="47089-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47089-147">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="47089-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="47089-148">`[OperationId <String>]`: ID da Operação.</span><span class="sxs-lookup"><span data-stu-id="47089-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="47089-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="47089-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="47089-150">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="47089-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="47089-151">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47089-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="47089-152">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="47089-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="47089-153">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="47089-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="47089-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47089-154">RELATED LINKS</span></span>

