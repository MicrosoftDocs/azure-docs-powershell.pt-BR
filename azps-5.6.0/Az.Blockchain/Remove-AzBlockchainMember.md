---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 54678dd00a0edae4af3a90c84e1c930c1c032e84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887902"
---
# <span data-ttu-id="40c9b-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="40c9b-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="40c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="40c9b-103">Exclua um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="40c9b-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="40c9b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="40c9b-104">SYNTAX</span></span>

### <span data-ttu-id="40c9b-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="40c9b-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40c9b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40c9b-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40c9b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="40c9b-107">DESCRIPTION</span></span>
<span data-ttu-id="40c9b-108">Exclua um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="40c9b-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="40c9b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40c9b-109">EXAMPLES</span></span>

### <span data-ttu-id="40c9b-110">Exemplo 1: Remover um membro do bloco de dados</span><span class="sxs-lookup"><span data-stu-id="40c9b-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="40c9b-111">Este comando remove um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="40c9b-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="40c9b-112">Exemplo 2: Remover um membro do bloco de dados</span><span class="sxs-lookup"><span data-stu-id="40c9b-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="40c9b-113">Este comando remove um membro do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="40c9b-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="40c9b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="40c9b-114">PARAMETERS</span></span>

### <span data-ttu-id="40c9b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40c9b-115">-AsJob</span></span>
<span data-ttu-id="40c9b-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="40c9b-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c9b-117">-DefaultProfile</span></span>
<span data-ttu-id="40c9b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40c9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c9b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40c9b-119">-InputObject</span></span>
<span data-ttu-id="40c9b-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="40c9b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="40c9b-121">-Name</span></span>
<span data-ttu-id="40c9b-122">Nome de membro do Bloco de Trabalho</span><span class="sxs-lookup"><span data-stu-id="40c9b-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="40c9b-123">-NoWait</span></span>
<span data-ttu-id="40c9b-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="40c9b-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40c9b-125">-PassThru</span></span>
<span data-ttu-id="40c9b-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="40c9b-126">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="40c9b-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="40c9b-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="40c9b-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="40c9b-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40c9b-130">-SubscriptionId</span></span>
<span data-ttu-id="40c9b-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40c9b-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="40c9b-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="40c9b-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c9b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40c9b-133">-Confirm</span></span>
<span data-ttu-id="40c9b-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40c9b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c9b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c9b-135">-WhatIf</span></span>
<span data-ttu-id="40c9b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40c9b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c9b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40c9b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c9b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c9b-138">CommonParameters</span></span>
<span data-ttu-id="40c9b-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c9b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c9b-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40c9b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c9b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40c9b-141">INPUTS</span></span>

### <span data-ttu-id="40c9b-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="40c9b-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="40c9b-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="40c9b-143">OUTPUTS</span></span>

### <span data-ttu-id="40c9b-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40c9b-144">System.Boolean</span></span>

## <span data-ttu-id="40c9b-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="40c9b-145">NOTES</span></span>

<span data-ttu-id="40c9b-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="40c9b-146">ALIASES</span></span>

<span data-ttu-id="40c9b-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="40c9b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40c9b-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="40c9b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40c9b-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40c9b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40c9b-150">INPUTOBJECT <IBlockchainIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="40c9b-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40c9b-151">`[BlockchainMemberName <String>]`: Nome de membro da cadeia de dados.</span><span class="sxs-lookup"><span data-stu-id="40c9b-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="40c9b-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="40c9b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40c9b-153">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="40c9b-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="40c9b-154">`[OperationId <String>]`: Id da operação.</span><span class="sxs-lookup"><span data-stu-id="40c9b-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="40c9b-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="40c9b-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="40c9b-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="40c9b-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="40c9b-157">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40c9b-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="40c9b-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="40c9b-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="40c9b-159">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="40c9b-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="40c9b-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40c9b-160">RELATED LINKS</span></span>

