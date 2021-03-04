---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893222"
---
# <span data-ttu-id="2458f-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="2458f-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="2458f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2458f-102">SYNOPSIS</span></span>
<span data-ttu-id="2458f-103">Atualizar o recurso Organization</span><span class="sxs-lookup"><span data-stu-id="2458f-103">Update Organization resource</span></span>

## <span data-ttu-id="2458f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2458f-104">SYNTAX</span></span>

### <span data-ttu-id="2458f-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2458f-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2458f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2458f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2458f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2458f-107">DESCRIPTION</span></span>
<span data-ttu-id="2458f-108">Atualizar o recurso Organization</span><span class="sxs-lookup"><span data-stu-id="2458f-108">Update Organization resource</span></span>

## <span data-ttu-id="2458f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2458f-109">EXAMPLES</span></span>

### <span data-ttu-id="2458f-110">Exemplo 1: atualizar uma organização confluente pelo nome</span><span class="sxs-lookup"><span data-stu-id="2458f-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="2458f-111">Este comando atualiza uma organização confluente pelo nome.</span><span class="sxs-lookup"><span data-stu-id="2458f-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="2458f-112">Exemplo 2: atualizar uma organização confluente por pipeline</span><span class="sxs-lookup"><span data-stu-id="2458f-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="2458f-113">Este comando atualiza uma organização confluente por pipeline.</span><span class="sxs-lookup"><span data-stu-id="2458f-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="2458f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2458f-114">PARAMETERS</span></span>

### <span data-ttu-id="2458f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2458f-115">-DefaultProfile</span></span>
<span data-ttu-id="2458f-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2458f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2458f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2458f-117">-InputObject</span></span>
<span data-ttu-id="2458f-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2458f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2458f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2458f-119">-Name</span></span>
<span data-ttu-id="2458f-120">Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="2458f-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2458f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2458f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2458f-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2458f-122">Resource group name</span></span>

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

### <span data-ttu-id="2458f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2458f-123">-SubscriptionId</span></span>
<span data-ttu-id="2458f-124">ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="2458f-124">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="2458f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2458f-125">-Tag</span></span>
<span data-ttu-id="2458f-126">ARM de recursos</span><span class="sxs-lookup"><span data-stu-id="2458f-126">ARM resource tags</span></span>

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

### <span data-ttu-id="2458f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2458f-127">-Confirm</span></span>
<span data-ttu-id="2458f-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2458f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2458f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2458f-129">-WhatIf</span></span>
<span data-ttu-id="2458f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2458f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2458f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2458f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2458f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2458f-132">CommonParameters</span></span>
<span data-ttu-id="2458f-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2458f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2458f-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2458f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2458f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2458f-135">INPUTS</span></span>

### <span data-ttu-id="2458f-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="2458f-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="2458f-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2458f-137">OUTPUTS</span></span>

### <span data-ttu-id="2458f-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="2458f-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="2458f-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="2458f-139">NOTES</span></span>

<span data-ttu-id="2458f-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2458f-140">ALIASES</span></span>

<span data-ttu-id="2458f-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2458f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2458f-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2458f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2458f-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2458f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2458f-144">INPUTOBJECT <IConfluentIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="2458f-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2458f-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2458f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2458f-146">`[OrganizationName <String>]`: Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="2458f-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="2458f-147">`[ResourceGroupName <String>]`: Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2458f-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="2458f-148">`[SubscriptionId <String>]`: ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="2458f-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="2458f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2458f-149">RELATED LINKS</span></span>

