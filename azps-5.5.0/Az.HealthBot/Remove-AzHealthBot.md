---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 1a3125939e1640a6bd734ee8f75f36a4c34196ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118458"
---
# <span data-ttu-id="5df63-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="5df63-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="5df63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5df63-102">SYNOPSIS</span></span>
<span data-ttu-id="5df63-103">Excluir um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="5df63-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="5df63-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5df63-104">SYNTAX</span></span>

### <span data-ttu-id="5df63-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5df63-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5df63-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5df63-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5df63-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5df63-107">DESCRIPTION</span></span>
<span data-ttu-id="5df63-108">Excluir um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="5df63-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="5df63-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5df63-109">EXAMPLES</span></span>

### <span data-ttu-id="5df63-110">Exemplo 1: Excluir HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="5df63-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="5df63-111">Excluir HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="5df63-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="5df63-112">Exemplo 2: Excluir HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="5df63-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="5df63-113">Excluir HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="5df63-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="5df63-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5df63-114">PARAMETERS</span></span>

### <span data-ttu-id="5df63-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5df63-115">-AsJob</span></span>
<span data-ttu-id="5df63-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5df63-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5df63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df63-117">-DefaultProfile</span></span>
<span data-ttu-id="5df63-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5df63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5df63-119">-InputObject</span></span>
<span data-ttu-id="5df63-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="5df63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5df63-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5df63-121">-Name</span></span>
<span data-ttu-id="5df63-122">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="5df63-122">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="5df63-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5df63-123">-NoWait</span></span>
<span data-ttu-id="5df63-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="5df63-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5df63-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5df63-125">-PassThru</span></span>
<span data-ttu-id="5df63-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="5df63-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5df63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df63-127">-ResourceGroupName</span></span>
<span data-ttu-id="5df63-128">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="5df63-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="5df63-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5df63-129">-SubscriptionId</span></span>
<span data-ttu-id="5df63-130">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5df63-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5df63-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5df63-131">-Confirm</span></span>
<span data-ttu-id="5df63-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5df63-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df63-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df63-133">-WhatIf</span></span>
<span data-ttu-id="5df63-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5df63-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df63-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5df63-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df63-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df63-136">CommonParameters</span></span>
<span data-ttu-id="5df63-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df63-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df63-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5df63-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df63-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="5df63-139">INPUTS</span></span>

### <span data-ttu-id="5df63-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="5df63-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="5df63-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="5df63-141">OUTPUTS</span></span>

### <span data-ttu-id="5df63-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5df63-142">System.Boolean</span></span>

## <span data-ttu-id="5df63-143">Notas</span><span class="sxs-lookup"><span data-stu-id="5df63-143">NOTES</span></span>

<span data-ttu-id="5df63-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="5df63-144">ALIASES</span></span>

<span data-ttu-id="5df63-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="5df63-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5df63-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5df63-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5df63-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5df63-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5df63-148">INPUTOBJECT: <IHealthBotIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="5df63-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5df63-149">`[BotName <String>]`: o nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="5df63-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="5df63-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5df63-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5df63-151">`[ResourceGroupName <String>]`: o nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="5df63-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="5df63-152">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5df63-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5df63-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5df63-153">RELATED LINKS</span></span>

