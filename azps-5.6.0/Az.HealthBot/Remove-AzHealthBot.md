---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893304"
---
# <span data-ttu-id="6d5d4-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="6d5d4-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="6d5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5d4-103">Excluir um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="6d5d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d5d4-104">SYNTAX</span></span>

### <span data-ttu-id="6d5d4-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d5d4-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d5d4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5d4-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d5d4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d5d4-107">DESCRIPTION</span></span>
<span data-ttu-id="6d5d4-108">Excluir um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="6d5d4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d5d4-109">EXAMPLES</span></span>

### <span data-ttu-id="6d5d4-110">Exemplo 1: Excluir HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="6d5d4-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="6d5d4-111">Excluir HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="6d5d4-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="6d5d4-112">Exemplo 2: Excluir HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5d4-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="6d5d4-113">Excluir HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5d4-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="6d5d4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d5d4-114">PARAMETERS</span></span>

### <span data-ttu-id="6d5d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d5d4-115">-AsJob</span></span>
<span data-ttu-id="6d5d4-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6d5d4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6d5d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5d4-117">-DefaultProfile</span></span>
<span data-ttu-id="6d5d4-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5d4-119">-InputObject</span></span>
<span data-ttu-id="6d5d4-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5d4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6d5d4-121">-Name</span></span>
<span data-ttu-id="6d5d4-122">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-122">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="6d5d4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d5d4-123">-NoWait</span></span>
<span data-ttu-id="6d5d4-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6d5d4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d5d4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d5d4-125">-PassThru</span></span>
<span data-ttu-id="6d5d4-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6d5d4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d5d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d5d4-128">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="6d5d4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d5d4-129">-SubscriptionId</span></span>
<span data-ttu-id="6d5d4-130">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6d5d4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d5d4-131">-Confirm</span></span>
<span data-ttu-id="6d5d4-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5d4-133">-WhatIf</span></span>
<span data-ttu-id="6d5d4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5d4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5d4-136">CommonParameters</span></span>
<span data-ttu-id="6d5d4-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5d4-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d5d4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5d4-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d5d4-139">INPUTS</span></span>

### <span data-ttu-id="6d5d4-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5d4-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="6d5d4-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d5d4-141">OUTPUTS</span></span>

### <span data-ttu-id="6d5d4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d5d4-142">System.Boolean</span></span>

## <span data-ttu-id="6d5d4-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d5d4-143">NOTES</span></span>

<span data-ttu-id="6d5d4-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6d5d4-144">ALIASES</span></span>

<span data-ttu-id="6d5d4-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6d5d4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d5d4-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d5d4-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d5d4-148">INPUTOBJECT <IHealthBotIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="6d5d4-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d5d4-149">`[BotName <String>]`: O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="6d5d4-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6d5d4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d5d4-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="6d5d4-152">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5d4-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6d5d4-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d5d4-153">RELATED LINKS</span></span>

