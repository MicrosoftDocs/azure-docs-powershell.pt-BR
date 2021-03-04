---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 77b4d7800d556fc43aee4e47ebc243d006a0f484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885746"
---
# <span data-ttu-id="e5a8b-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="e5a8b-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="e5a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a8b-103">Regenerar as chaves da API de um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="e5a8b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5a8b-104">SYNTAX</span></span>

### <span data-ttu-id="e5a8b-105">RegenerateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5a8b-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5a8b-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e5a8b-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5a8b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5a8b-107">DESCRIPTION</span></span>
<span data-ttu-id="e5a8b-108">Regenerar as chaves da API de um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="e5a8b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5a8b-109">EXAMPLES</span></span>

### <span data-ttu-id="e5a8b-110">Exemplo 1: Regenerar chaves de Api para um membro do bloco de dados usando o nome</span><span class="sxs-lookup"><span data-stu-id="e5a8b-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="e5a8b-111">Este comando regenera as chaves da Api para um membro do bloco de dados usando nome, grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="e5a8b-112">Exemplo 2: Regenerar chaves de Api para um membro do bloco de dados usando a idenidade</span><span class="sxs-lookup"><span data-stu-id="e5a8b-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="e5a8b-113">Este comando regenera chaves de Api para um membro do bloco de dados usando identidade.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="e5a8b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5a8b-114">PARAMETERS</span></span>

### <span data-ttu-id="e5a8b-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e5a8b-115">-BlockchainMemberName</span></span>
<span data-ttu-id="e5a8b-116">Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="e5a8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a8b-117">-DefaultProfile</span></span>
<span data-ttu-id="e5a8b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a8b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5a8b-119">-InputObject</span></span>
<span data-ttu-id="e5a8b-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5a8b-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e5a8b-121">-KeyName</span></span>
<span data-ttu-id="e5a8b-122">Obtém ou define o nome da chave da API.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="e5a8b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a8b-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5a8b-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e5a8b-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e5a8b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5a8b-126">-SubscriptionId</span></span>
<span data-ttu-id="e5a8b-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5a8b-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5a8b-129">-Value</span><span class="sxs-lookup"><span data-stu-id="e5a8b-129">-Value</span></span>
<span data-ttu-id="e5a8b-130">Obtém ou define o valor da chave da API.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="e5a8b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5a8b-131">-Confirm</span></span>
<span data-ttu-id="e5a8b-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a8b-133">-WhatIf</span></span>
<span data-ttu-id="e5a8b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a8b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a8b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a8b-136">CommonParameters</span></span>
<span data-ttu-id="e5a8b-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a8b-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5a8b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a8b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5a8b-139">INPUTS</span></span>

### <span data-ttu-id="e5a8b-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="e5a8b-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="e5a8b-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5a8b-141">OUTPUTS</span></span>

### <span data-ttu-id="e5a8b-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="e5a8b-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="e5a8b-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5a8b-143">NOTES</span></span>

<span data-ttu-id="e5a8b-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e5a8b-144">ALIASES</span></span>

<span data-ttu-id="e5a8b-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e5a8b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5a8b-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5a8b-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5a8b-148">INPUTOBJECT <IBlockchainIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e5a8b-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5a8b-149">`[BlockchainMemberName <String>]`: Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="e5a8b-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e5a8b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5a8b-151">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="e5a8b-152">`[OperationId <String>]`: Id da operação.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="e5a8b-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e5a8b-154">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e5a8b-155">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e5a8b-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="e5a8b-157">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="e5a8b-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5a8b-158">RELATED LINKS</span></span>

