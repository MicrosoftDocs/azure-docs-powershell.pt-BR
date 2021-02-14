---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111205"
---
# <span data-ttu-id="96921-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="96921-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="96921-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96921-102">SYNOPSIS</span></span>
<span data-ttu-id="96921-103">Regenerar as teclas da API de um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="96921-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="96921-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96921-104">SYNTAX</span></span>

### <span data-ttu-id="96921-105">RegenerateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96921-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96921-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="96921-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96921-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="96921-107">DESCRIPTION</span></span>
<span data-ttu-id="96921-108">Regenerar as teclas da API de um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="96921-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="96921-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96921-109">EXAMPLES</span></span>

### <span data-ttu-id="96921-110">Exemplo 1: Chaves da Api regenerar para um membro da família Ao usar o nome</span><span class="sxs-lookup"><span data-stu-id="96921-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="96921-111">Este comando regenera as teclas da Api para um membro da casa usando nome, grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96921-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="96921-112">Exemplo 2: Chaves da Api regenerar para um membro da família Ao usar idenity</span><span class="sxs-lookup"><span data-stu-id="96921-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="96921-113">Esse comando regenera as teclas da Api para um membro da empresa usando a identidade.</span><span class="sxs-lookup"><span data-stu-id="96921-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="96921-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96921-114">PARAMETERS</span></span>

### <span data-ttu-id="96921-115">-NomedoMember</span><span class="sxs-lookup"><span data-stu-id="96921-115">-BlockchainMemberName</span></span>
<span data-ttu-id="96921-116">Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="96921-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="96921-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96921-117">-DefaultProfile</span></span>
<span data-ttu-id="96921-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96921-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96921-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96921-119">-InputObject</span></span>
<span data-ttu-id="96921-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="96921-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96921-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="96921-121">-KeyName</span></span>
<span data-ttu-id="96921-122">Obtém ou define o nome da chave da API.</span><span class="sxs-lookup"><span data-stu-id="96921-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="96921-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96921-123">-ResourceGroupName</span></span>
<span data-ttu-id="96921-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="96921-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="96921-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="96921-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="96921-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96921-126">-SubscriptionId</span></span>
<span data-ttu-id="96921-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96921-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="96921-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="96921-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96921-129">-Valor</span><span class="sxs-lookup"><span data-stu-id="96921-129">-Value</span></span>
<span data-ttu-id="96921-130">Obtém ou define o valor da chave da API.</span><span class="sxs-lookup"><span data-stu-id="96921-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="96921-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96921-131">-Confirm</span></span>
<span data-ttu-id="96921-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96921-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96921-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96921-133">-WhatIf</span></span>
<span data-ttu-id="96921-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96921-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96921-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96921-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96921-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96921-136">CommonParameters</span></span>
<span data-ttu-id="96921-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96921-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96921-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96921-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96921-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="96921-139">INPUTS</span></span>

### <span data-ttu-id="96921-140">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="96921-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="96921-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="96921-141">OUTPUTS</span></span>

### <span data-ttu-id="96921-142">Microsoft.Azure.PowerShell.Cmdlets.Bluetooth.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="96921-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="96921-143">Notas</span><span class="sxs-lookup"><span data-stu-id="96921-143">NOTES</span></span>

<span data-ttu-id="96921-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="96921-144">ALIASES</span></span>

<span data-ttu-id="96921-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="96921-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96921-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="96921-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96921-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96921-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96921-148">INPUTOBJECT: <IBlockchainIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="96921-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96921-149">`[BlockchainMemberName <String>]`: Nome do membro Dal.</span><span class="sxs-lookup"><span data-stu-id="96921-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="96921-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="96921-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96921-151">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="96921-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="96921-152">`[OperationId <String>]`: ID da Operação.</span><span class="sxs-lookup"><span data-stu-id="96921-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="96921-153">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="96921-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="96921-154">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="96921-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="96921-155">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96921-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="96921-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="96921-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="96921-157">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="96921-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="96921-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96921-158">RELATED LINKS</span></span>

