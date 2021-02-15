---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112207"
---
# <span data-ttu-id="f119a-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f119a-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="f119a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f119a-102">SYNOPSIS</span></span>
<span data-ttu-id="f119a-103">Obter detalhes sobre um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="f119a-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="f119a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f119a-104">SYNTAX</span></span>

### <span data-ttu-id="f119a-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f119a-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f119a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f119a-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f119a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f119a-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f119a-108">Lista</span><span class="sxs-lookup"><span data-stu-id="f119a-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f119a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f119a-109">DESCRIPTION</span></span>
<span data-ttu-id="f119a-110">Obter detalhes sobre um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="f119a-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="f119a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f119a-111">EXAMPLES</span></span>

### <span data-ttu-id="f119a-112">Exemplo 1: Listar membros da família</span><span class="sxs-lookup"><span data-stu-id="f119a-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f119a-113">Este comando lista os membros de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f119a-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="f119a-114">Exemplo 2: Listar membros</span><span class="sxs-lookup"><span data-stu-id="f119a-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f119a-115">Este comando lista os membros de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f119a-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="f119a-116">Exemplo 3: Obter um membro da família</span><span class="sxs-lookup"><span data-stu-id="f119a-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f119a-117">Esse comando obtém um membro da empresa sob um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f119a-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="f119a-118">Exemplo 4: Obter um membro da família</span><span class="sxs-lookup"><span data-stu-id="f119a-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f119a-119">Esse comando obtém um membro da empresa sob um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f119a-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="f119a-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f119a-120">PARAMETERS</span></span>

### <span data-ttu-id="f119a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f119a-121">-DefaultProfile</span></span>
<span data-ttu-id="f119a-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f119a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f119a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f119a-123">-InputObject</span></span>
<span data-ttu-id="f119a-124">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f119a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f119a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f119a-125">-Name</span></span>
<span data-ttu-id="f119a-126">Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="f119a-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="f119a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f119a-127">-ResourceGroupName</span></span>
<span data-ttu-id="f119a-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f119a-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f119a-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="f119a-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f119a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f119a-130">-SubscriptionId</span></span>
<span data-ttu-id="f119a-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f119a-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f119a-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f119a-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f119a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f119a-133">CommonParameters</span></span>
<span data-ttu-id="f119a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f119a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f119a-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f119a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f119a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="f119a-136">INPUTS</span></span>

### <span data-ttu-id="f119a-137">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="f119a-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="f119a-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="f119a-138">OUTPUTS</span></span>

### <span data-ttu-id="f119a-139">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f119a-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="f119a-140">Notas</span><span class="sxs-lookup"><span data-stu-id="f119a-140">NOTES</span></span>

<span data-ttu-id="f119a-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="f119a-141">ALIASES</span></span>

<span data-ttu-id="f119a-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f119a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f119a-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f119a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f119a-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f119a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f119a-145">INPUTOBJECT: <IBlockchainIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f119a-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f119a-146">`[BlockchainMemberName <String>]`: Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="f119a-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="f119a-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f119a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f119a-148">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="f119a-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="f119a-149">`[OperationId <String>]`: ID da Operação.</span><span class="sxs-lookup"><span data-stu-id="f119a-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="f119a-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f119a-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f119a-151">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="f119a-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f119a-152">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f119a-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="f119a-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f119a-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="f119a-154">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="f119a-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="f119a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f119a-155">RELATED LINKS</span></span>

