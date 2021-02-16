---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117920"
---
# <span data-ttu-id="0a652-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="0a652-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="0a652-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a652-102">SYNOPSIS</span></span>
<span data-ttu-id="0a652-103">Exclua um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="0a652-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="0a652-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a652-104">SYNTAX</span></span>

### <span data-ttu-id="0a652-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0a652-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0a652-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a652-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a652-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a652-107">DESCRIPTION</span></span>
<span data-ttu-id="0a652-108">Exclua um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="0a652-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="0a652-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a652-109">EXAMPLES</span></span>

### <span data-ttu-id="0a652-110">Exemplo 1: Remover um membro da casa</span><span class="sxs-lookup"><span data-stu-id="0a652-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="0a652-111">Este comando remove um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="0a652-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="0a652-112">Exemplo 2: Remover um membro da família</span><span class="sxs-lookup"><span data-stu-id="0a652-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="0a652-113">Este comando remove um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="0a652-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="0a652-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a652-114">PARAMETERS</span></span>

### <span data-ttu-id="0a652-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a652-115">-AsJob</span></span>
<span data-ttu-id="0a652-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="0a652-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0a652-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a652-117">-DefaultProfile</span></span>
<span data-ttu-id="0a652-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a652-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a652-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a652-119">-InputObject</span></span>
<span data-ttu-id="0a652-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0a652-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a652-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a652-121">-Name</span></span>
<span data-ttu-id="0a652-122">Nome do membro Dal med</span><span class="sxs-lookup"><span data-stu-id="0a652-122">Blockchain member name</span></span>

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

### <span data-ttu-id="0a652-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a652-123">-NoWait</span></span>
<span data-ttu-id="0a652-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="0a652-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a652-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a652-125">-PassThru</span></span>
<span data-ttu-id="0a652-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="0a652-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0a652-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a652-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a652-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0a652-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0a652-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="0a652-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0a652-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a652-130">-SubscriptionId</span></span>
<span data-ttu-id="0a652-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a652-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0a652-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0a652-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a652-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a652-133">-Confirm</span></span>
<span data-ttu-id="0a652-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a652-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a652-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a652-135">-WhatIf</span></span>
<span data-ttu-id="0a652-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a652-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a652-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a652-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a652-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a652-138">CommonParameters</span></span>
<span data-ttu-id="0a652-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a652-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a652-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a652-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a652-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a652-141">INPUTS</span></span>

### <span data-ttu-id="0a652-142">Microsoft.Azure.PowerShell.Cmdlets.Block.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="0a652-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="0a652-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a652-143">OUTPUTS</span></span>

### <span data-ttu-id="0a652-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a652-144">System.Boolean</span></span>

## <span data-ttu-id="0a652-145">Notas</span><span class="sxs-lookup"><span data-stu-id="0a652-145">NOTES</span></span>

<span data-ttu-id="0a652-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="0a652-146">ALIASES</span></span>

<span data-ttu-id="0a652-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0a652-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a652-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0a652-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a652-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a652-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a652-150">INPUTOBJECT: <IBlockchainIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="0a652-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a652-151">`[BlockchainMemberName <String>]`: Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="0a652-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="0a652-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="0a652-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a652-153">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="0a652-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="0a652-154">`[OperationId <String>]`: ID da Operação.</span><span class="sxs-lookup"><span data-stu-id="0a652-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="0a652-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0a652-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0a652-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="0a652-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0a652-157">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a652-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="0a652-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0a652-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="0a652-159">`[TransactionNodeName <String>]`: Nome do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="0a652-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="0a652-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a652-160">RELATED LINKS</span></span>

