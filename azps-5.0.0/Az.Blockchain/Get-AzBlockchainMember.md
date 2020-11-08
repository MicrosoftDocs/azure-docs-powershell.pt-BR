---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125500"
---
# <span data-ttu-id="d1fc1-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="d1fc1-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="d1fc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fc1-103">Obter detalhes sobre um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="d1fc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1fc1-104">SYNTAX</span></span>

### <span data-ttu-id="d1fc1-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1fc1-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1fc1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d1fc1-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1fc1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1fc1-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1fc1-108">Programação</span><span class="sxs-lookup"><span data-stu-id="d1fc1-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1fc1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1fc1-109">DESCRIPTION</span></span>
<span data-ttu-id="d1fc1-110">Obter detalhes sobre um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="d1fc1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1fc1-111">EXAMPLES</span></span>

### <span data-ttu-id="d1fc1-112">Exemplo 1: listar membros do blockchain</span><span class="sxs-lookup"><span data-stu-id="d1fc1-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="d1fc1-113">Esse comando lista os membros do blockchain em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="d1fc1-114">Exemplo 2: listar membros do blockchain</span><span class="sxs-lookup"><span data-stu-id="d1fc1-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="d1fc1-115">Esse comando lista os membros do blockchain em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="d1fc1-116">Exemplo 3: obter um membro de blockchain</span><span class="sxs-lookup"><span data-stu-id="d1fc1-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="d1fc1-117">Esse comando obtém um membro blockchain em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="d1fc1-118">Exemplo 4: obter um membro do blockchain</span><span class="sxs-lookup"><span data-stu-id="d1fc1-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="d1fc1-119">Esse comando obtém um membro blockchain em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="d1fc1-120">OS</span><span class="sxs-lookup"><span data-stu-id="d1fc1-120">PARAMETERS</span></span>

### <span data-ttu-id="d1fc1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fc1-121">-DefaultProfile</span></span>
<span data-ttu-id="d1fc1-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1fc1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1fc1-123">-InputObject</span></span>
<span data-ttu-id="d1fc1-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1fc1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1fc1-125">-Name</span></span>
<span data-ttu-id="d1fc1-126">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fc1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fc1-127">-ResourceGroupName</span></span>
<span data-ttu-id="d1fc1-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d1fc1-129">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d1fc1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1fc1-130">-SubscriptionId</span></span>
<span data-ttu-id="d1fc1-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d1fc1-132">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fc1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fc1-133">CommonParameters</span></span>
<span data-ttu-id="d1fc1-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fc1-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1fc1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fc1-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1fc1-136">INPUTS</span></span>

### <span data-ttu-id="d1fc1-137">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d1fc1-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d1fc1-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1fc1-138">OUTPUTS</span></span>

### <span data-ttu-id="d1fc1-139">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="d1fc1-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="d1fc1-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1fc1-140">NOTES</span></span>

<span data-ttu-id="d1fc1-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d1fc1-141">ALIASES</span></span>

<span data-ttu-id="d1fc1-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d1fc1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1fc1-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1fc1-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1fc1-145">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d1fc1-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1fc1-146">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d1fc1-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d1fc1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1fc1-148">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d1fc1-149">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d1fc1-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d1fc1-151">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d1fc1-152">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d1fc1-153">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d1fc1-154">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="d1fc1-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d1fc1-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1fc1-155">RELATED LINKS</span></span>

