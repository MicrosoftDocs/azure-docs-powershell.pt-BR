---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434479"
---
# <span data-ttu-id="aadd3-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="aadd3-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="aadd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aadd3-102">SYNOPSIS</span></span>
<span data-ttu-id="aadd3-103">Excluir um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="aadd3-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="aadd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aadd3-104">SYNTAX</span></span>

### <span data-ttu-id="aadd3-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="aadd3-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aadd3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aadd3-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aadd3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aadd3-107">DESCRIPTION</span></span>
<span data-ttu-id="aadd3-108">Excluir um membro do blockchain.</span><span class="sxs-lookup"><span data-stu-id="aadd3-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="aadd3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aadd3-109">EXAMPLES</span></span>

### <span data-ttu-id="aadd3-110">Exemplo 1: remover um membro do blockchain</span><span class="sxs-lookup"><span data-stu-id="aadd3-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="aadd3-111">Esse comando Remove um membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="aadd3-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="aadd3-112">Exemplo 2: remover um membro do blockchain</span><span class="sxs-lookup"><span data-stu-id="aadd3-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="aadd3-113">Esse comando Remove um membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="aadd3-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="aadd3-114">OS</span><span class="sxs-lookup"><span data-stu-id="aadd3-114">PARAMETERS</span></span>

### <span data-ttu-id="aadd3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aadd3-115">-AsJob</span></span>
<span data-ttu-id="aadd3-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="aadd3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aadd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadd3-117">-DefaultProfile</span></span>
<span data-ttu-id="aadd3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aadd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aadd3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aadd3-119">-InputObject</span></span>
<span data-ttu-id="aadd3-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aadd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aadd3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="aadd3-121">-Name</span></span>
<span data-ttu-id="aadd3-122">Nome do membro Blockchain</span><span class="sxs-lookup"><span data-stu-id="aadd3-122">Blockchain member name</span></span>

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

### <span data-ttu-id="aadd3-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aadd3-123">-NoWait</span></span>
<span data-ttu-id="aadd3-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="aadd3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aadd3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aadd3-125">-PassThru</span></span>
<span data-ttu-id="aadd3-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="aadd3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aadd3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aadd3-127">-ResourceGroupName</span></span>
<span data-ttu-id="aadd3-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="aadd3-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aadd3-129">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="aadd3-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aadd3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aadd3-130">-SubscriptionId</span></span>
<span data-ttu-id="aadd3-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aadd3-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aadd3-132">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aadd3-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aadd3-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aadd3-133">-Confirm</span></span>
<span data-ttu-id="aadd3-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aadd3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aadd3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aadd3-135">-WhatIf</span></span>
<span data-ttu-id="aadd3-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aadd3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aadd3-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aadd3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aadd3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadd3-138">CommonParameters</span></span>
<span data-ttu-id="aadd3-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aadd3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadd3-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aadd3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadd3-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aadd3-141">INPUTS</span></span>

### <span data-ttu-id="aadd3-142">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="aadd3-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="aadd3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aadd3-143">OUTPUTS</span></span>

### <span data-ttu-id="aadd3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aadd3-144">System.Boolean</span></span>

## <span data-ttu-id="aadd3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aadd3-145">NOTES</span></span>

<span data-ttu-id="aadd3-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aadd3-146">ALIASES</span></span>

<span data-ttu-id="aadd3-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="aadd3-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aadd3-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="aadd3-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aadd3-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aadd3-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aadd3-150">INPUTobject <IBlockchainIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="aadd3-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aadd3-151">`[BlockchainMemberName <String>]`: Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="aadd3-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="aadd3-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="aadd3-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aadd3-153">`[Location <String>]`: Nome do local.</span><span class="sxs-lookup"><span data-stu-id="aadd3-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="aadd3-154">`[OperationId <String>]`: ID da operação.</span><span class="sxs-lookup"><span data-stu-id="aadd3-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="aadd3-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="aadd3-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="aadd3-156">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="aadd3-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="aadd3-157">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aadd3-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="aadd3-158">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aadd3-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="aadd3-159">`[TransactionNodeName <String>]`: Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="aadd3-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="aadd3-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aadd3-160">RELATED LINKS</span></span>

