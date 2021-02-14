---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115515"
---
# <span data-ttu-id="38ed0-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="38ed0-101">Remove-AzBotService</span></span>

## <span data-ttu-id="38ed0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="38ed0-103">Exclui um Serviço de Bot do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38ed0-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="38ed0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38ed0-104">SYNTAX</span></span>

### <span data-ttu-id="38ed0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38ed0-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38ed0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38ed0-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38ed0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="38ed0-107">DESCRIPTION</span></span>
<span data-ttu-id="38ed0-108">Exclui um Serviço de Bot do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38ed0-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="38ed0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="38ed0-110">Exemplo 1: Excluir o BotService by Name e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ed0-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="38ed0-111">Excluir o BotService by Name e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ed0-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="38ed0-112">Exemplo 2: Excluir o BotService by InputObject</span><span class="sxs-lookup"><span data-stu-id="38ed0-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="38ed0-113">Excluir o BotService by InputObject</span><span class="sxs-lookup"><span data-stu-id="38ed0-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="38ed0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38ed0-114">PARAMETERS</span></span>

### <span data-ttu-id="38ed0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ed0-115">-DefaultProfile</span></span>
<span data-ttu-id="38ed0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ed0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38ed0-117">-InputObject</span></span>
<span data-ttu-id="38ed0-118">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="38ed0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38ed0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="38ed0-119">-Name</span></span>
<span data-ttu-id="38ed0-120">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="38ed0-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="38ed0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ed0-121">-PassThru</span></span>
<span data-ttu-id="38ed0-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="38ed0-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="38ed0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ed0-123">-ResourceGroupName</span></span>
<span data-ttu-id="38ed0-124">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="38ed0-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="38ed0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38ed0-125">-SubscriptionId</span></span>
<span data-ttu-id="38ed0-126">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed0-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="38ed0-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="38ed0-127">-Confirm</span></span>
<span data-ttu-id="38ed0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ed0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ed0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ed0-129">-WhatIf</span></span>
<span data-ttu-id="38ed0-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="38ed0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ed0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38ed0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ed0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ed0-132">CommonParameters</span></span>
<span data-ttu-id="38ed0-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ed0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ed0-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38ed0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ed0-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="38ed0-135">INPUTS</span></span>

### <span data-ttu-id="38ed0-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="38ed0-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="38ed0-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="38ed0-137">OUTPUTS</span></span>

### <span data-ttu-id="38ed0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38ed0-138">System.Boolean</span></span>

## <span data-ttu-id="38ed0-139">Notas</span><span class="sxs-lookup"><span data-stu-id="38ed0-139">NOTES</span></span>

<span data-ttu-id="38ed0-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="38ed0-140">ALIASES</span></span>

<span data-ttu-id="38ed0-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="38ed0-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38ed0-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="38ed0-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38ed0-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38ed0-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38ed0-144">INPUTOBJECT: <IBotServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="38ed0-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38ed0-145">`[ChannelName <ChannelName?>]`: o nome do recurso Canal.</span><span class="sxs-lookup"><span data-stu-id="38ed0-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="38ed0-146">`[ConnectionName <String>]`: o nome do recurso Configuração de Conexão de Serviço de Bot</span><span class="sxs-lookup"><span data-stu-id="38ed0-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="38ed0-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="38ed0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38ed0-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="38ed0-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="38ed0-149">`[ResourceName <String>]`: o nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="38ed0-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="38ed0-150">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed0-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="38ed0-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38ed0-151">RELATED LINKS</span></span>

