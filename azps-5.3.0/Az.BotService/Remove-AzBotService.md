---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430350"
---
# <span data-ttu-id="e395a-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="e395a-101">Remove-AzBotService</span></span>

## <span data-ttu-id="e395a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e395a-102">SYNOPSIS</span></span>
<span data-ttu-id="e395a-103">Exclui um serviço de bot do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e395a-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="e395a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e395a-104">SYNTAX</span></span>

### <span data-ttu-id="e395a-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="e395a-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e395a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e395a-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e395a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e395a-107">DESCRIPTION</span></span>
<span data-ttu-id="e395a-108">Exclui um serviço de bot do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e395a-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="e395a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e395a-109">EXAMPLES</span></span>

### <span data-ttu-id="e395a-110">Exemplo 1: excluir o BotService por nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e395a-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="e395a-111">Excluir o BotService por nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e395a-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="e395a-112">Exemplo 2: excluir o BotService por InputObject</span><span class="sxs-lookup"><span data-stu-id="e395a-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="e395a-113">Excluir o BotService por InputObject</span><span class="sxs-lookup"><span data-stu-id="e395a-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="e395a-114">OS</span><span class="sxs-lookup"><span data-stu-id="e395a-114">PARAMETERS</span></span>

### <span data-ttu-id="e395a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e395a-115">-DefaultProfile</span></span>
<span data-ttu-id="e395a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e395a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e395a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e395a-117">-InputObject</span></span>
<span data-ttu-id="e395a-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e395a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e395a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e395a-119">-Name</span></span>
<span data-ttu-id="e395a-120">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="e395a-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e395a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e395a-121">-PassThru</span></span>
<span data-ttu-id="e395a-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e395a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e395a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e395a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e395a-124">O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="e395a-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="e395a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e395a-125">-SubscriptionId</span></span>
<span data-ttu-id="e395a-126">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e395a-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e395a-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e395a-127">-Confirm</span></span>
<span data-ttu-id="e395a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e395a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e395a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e395a-129">-WhatIf</span></span>
<span data-ttu-id="e395a-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e395a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e395a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e395a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e395a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e395a-132">CommonParameters</span></span>
<span data-ttu-id="e395a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e395a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e395a-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e395a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e395a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e395a-135">INPUTS</span></span>

### <span data-ttu-id="e395a-136">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e395a-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="e395a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e395a-137">OUTPUTS</span></span>

### <span data-ttu-id="e395a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e395a-138">System.Boolean</span></span>

## <span data-ttu-id="e395a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e395a-139">NOTES</span></span>

<span data-ttu-id="e395a-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e395a-140">ALIASES</span></span>

<span data-ttu-id="e395a-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e395a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e395a-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e395a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e395a-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e395a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e395a-144">INPUTobject <IBotServiceIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e395a-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e395a-145">`[ChannelName <ChannelName?>]`: O nome do recurso de canal.</span><span class="sxs-lookup"><span data-stu-id="e395a-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="e395a-146">`[ConnectionName <String>]`: O nome do recurso de configuração de conexão do serviço bot</span><span class="sxs-lookup"><span data-stu-id="e395a-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="e395a-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e395a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e395a-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="e395a-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="e395a-149">`[ResourceName <String>]`: O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="e395a-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="e395a-150">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e395a-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e395a-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e395a-151">RELATED LINKS</span></span>

