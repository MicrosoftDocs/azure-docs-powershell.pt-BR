---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955102"
---
# <span data-ttu-id="a0e30-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="a0e30-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="a0e30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0e30-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e30-103">Regenerar as chaves de API para um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="a0e30-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="a0e30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0e30-104">SYNTAX</span></span>

### <span data-ttu-id="a0e30-105">RegenerateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0e30-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0e30-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a0e30-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0e30-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0e30-107">DESCRIPTION</span></span>
<span data-ttu-id="a0e30-108">Regenerar as chaves de API para um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="a0e30-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="a0e30-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0e30-109">EXAMPLES</span></span>

### <span data-ttu-id="a0e30-110">Exemplo 1: regenerar as chaves de API para um membro do blockchain usando o nome</span><span class="sxs-lookup"><span data-stu-id="a0e30-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="a0e30-111">Esse comando regenera as chaves de API para um membro do blockchain usando o nome, o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0e30-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="a0e30-112">Exemplo 2: regenerar as chaves de API para um membro do blockchain usando idenity</span><span class="sxs-lookup"><span data-stu-id="a0e30-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="a0e30-113">Esse comando regenera as chaves de API para um membro blockchain usando a identidade.</span><span class="sxs-lookup"><span data-stu-id="a0e30-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="a0e30-114">OS</span><span class="sxs-lookup"><span data-stu-id="a0e30-114">PARAMETERS</span></span>

### <span data-ttu-id="a0e30-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="a0e30-115">-BlockchainMemberName</span></span>
<span data-ttu-id="a0e30-116">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a0e30-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="a0e30-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e30-117">-DefaultProfile</span></span>
<span data-ttu-id="a0e30-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e30-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0e30-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0e30-119">-InputObject</span></span>
<span data-ttu-id="a0e30-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a0e30-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0e30-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a0e30-121">-KeyName</span></span>
<span data-ttu-id="a0e30-122">Obtém ou define o nome da chave da API.</span><span class="sxs-lookup"><span data-stu-id="a0e30-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="a0e30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e30-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0e30-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a0e30-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a0e30-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="a0e30-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a0e30-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0e30-126">-SubscriptionId</span></span>
<span data-ttu-id="a0e30-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e30-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0e30-128">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a0e30-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0e30-129">-Valor</span><span class="sxs-lookup"><span data-stu-id="a0e30-129">-Value</span></span>
<span data-ttu-id="a0e30-130">Obtém ou define o valor da chave da API.</span><span class="sxs-lookup"><span data-stu-id="a0e30-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="a0e30-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0e30-131">-Confirm</span></span>
<span data-ttu-id="a0e30-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e30-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e30-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e30-133">-WhatIf</span></span>
<span data-ttu-id="a0e30-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0e30-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e30-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0e30-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e30-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e30-136">CommonParameters</span></span>
<span data-ttu-id="a0e30-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e30-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e30-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0e30-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e30-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0e30-139">INPUTS</span></span>

### <span data-ttu-id="a0e30-140">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="a0e30-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="a0e30-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0e30-141">OUTPUTS</span></span>

### <span data-ttu-id="a0e30-142">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="a0e30-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="a0e30-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0e30-143">NOTES</span></span>

<span data-ttu-id="a0e30-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a0e30-144">ALIASES</span></span>

<span data-ttu-id="a0e30-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a0e30-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0e30-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a0e30-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0e30-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0e30-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0e30-148">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a0e30-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0e30-149">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a0e30-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="a0e30-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a0e30-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0e30-151">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="a0e30-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="a0e30-152">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="a0e30-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="a0e30-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a0e30-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a0e30-154">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="a0e30-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a0e30-155">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e30-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="a0e30-156">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a0e30-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="a0e30-157">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="a0e30-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="a0e30-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0e30-158">RELATED LINKS</span></span>

