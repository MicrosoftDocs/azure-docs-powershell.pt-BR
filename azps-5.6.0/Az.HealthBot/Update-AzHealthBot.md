---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: a0dc204bb6dc1a91031a87fd113c525f282f090e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893303"
---
# <span data-ttu-id="e3be2-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="e3be2-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="e3be2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3be2-102">SYNOPSIS</span></span>
<span data-ttu-id="e3be2-103">Patch a HealthBot.</span><span class="sxs-lookup"><span data-stu-id="e3be2-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="e3be2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3be2-104">SYNTAX</span></span>

### <span data-ttu-id="e3be2-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3be2-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3be2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e3be2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3be2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3be2-107">DESCRIPTION</span></span>
<span data-ttu-id="e3be2-108">Patch a HealthBot.</span><span class="sxs-lookup"><span data-stu-id="e3be2-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="e3be2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3be2-109">EXAMPLES</span></span>

### <span data-ttu-id="e3be2-110">Exemplo 1: atualizar HealthBot por Resourcegroupname e Name</span><span class="sxs-lookup"><span data-stu-id="e3be2-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="e3be2-111">atualizar HealthBot por Resourcegroupname e Name</span><span class="sxs-lookup"><span data-stu-id="e3be2-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="e3be2-112">Exemplo 2: atualizar HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="e3be2-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="e3be2-113">atualizar HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="e3be2-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="e3be2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3be2-114">PARAMETERS</span></span>

### <span data-ttu-id="e3be2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3be2-115">-DefaultProfile</span></span>
<span data-ttu-id="e3be2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3be2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3be2-117">-InputObject</span></span>
<span data-ttu-id="e3be2-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e3be2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e3be2-119">-Name</span></span>
<span data-ttu-id="e3be2-120">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="e3be2-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3be2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3be2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3be2-122">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3be2-122">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3be2-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="e3be2-123">-Sku</span></span>
<span data-ttu-id="e3be2-124">O nome do SKU HealthBot</span><span class="sxs-lookup"><span data-stu-id="e3be2-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3be2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3be2-125">-SubscriptionId</span></span>
<span data-ttu-id="e3be2-126">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be2-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3be2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3be2-127">-Tag</span></span>
<span data-ttu-id="e3be2-128">Marcas para um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="e3be2-128">Tags for a HealthBot.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3be2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3be2-129">-Confirm</span></span>
<span data-ttu-id="e3be2-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3be2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3be2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3be2-131">-WhatIf</span></span>
<span data-ttu-id="e3be2-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3be2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3be2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3be2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3be2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3be2-134">CommonParameters</span></span>
<span data-ttu-id="e3be2-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3be2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3be2-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3be2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3be2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3be2-137">INPUTS</span></span>

### <span data-ttu-id="e3be2-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="e3be2-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="e3be2-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3be2-139">OUTPUTS</span></span>

### <span data-ttu-id="e3be2-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="e3be2-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="e3be2-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3be2-141">NOTES</span></span>

<span data-ttu-id="e3be2-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e3be2-142">ALIASES</span></span>

<span data-ttu-id="e3be2-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e3be2-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3be2-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e3be2-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3be2-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3be2-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3be2-146">INPUTOBJECT <IHealthBotIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e3be2-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3be2-147">`[BotName <String>]`: O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="e3be2-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="e3be2-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e3be2-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3be2-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3be2-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="e3be2-150">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be2-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e3be2-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3be2-151">RELATED LINKS</span></span>

