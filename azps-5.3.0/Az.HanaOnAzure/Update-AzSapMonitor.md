---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429264"
---
# <span data-ttu-id="09948-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="09948-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="09948-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09948-102">SYNOPSIS</span></span>
<span data-ttu-id="09948-103">Patches o campo Tags de um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do monitor.</span><span class="sxs-lookup"><span data-stu-id="09948-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="09948-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09948-104">SYNTAX</span></span>

### <span data-ttu-id="09948-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="09948-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09948-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09948-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09948-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09948-107">DESCRIPTION</span></span>
<span data-ttu-id="09948-108">Patches o campo Tags de um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do monitor.</span><span class="sxs-lookup"><span data-stu-id="09948-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="09948-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09948-109">EXAMPLES</span></span>

### <span data-ttu-id="09948-110">Exemplo 1: atualizar um monitor SAP por nome</span><span class="sxs-lookup"><span data-stu-id="09948-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="09948-111">Esses comandos atualizam um monitor SAP por nome.</span><span class="sxs-lookup"><span data-stu-id="09948-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="09948-112">Exemplo 2: atualizar um monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="09948-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="09948-113">Esses comandos atualizam um monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="09948-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="09948-114">OS</span><span class="sxs-lookup"><span data-stu-id="09948-114">PARAMETERS</span></span>

### <span data-ttu-id="09948-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09948-115">-DefaultProfile</span></span>
<span data-ttu-id="09948-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09948-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09948-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09948-117">-InputObject</span></span>
<span data-ttu-id="09948-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="09948-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09948-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="09948-119">-Name</span></span>
<span data-ttu-id="09948-120">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="09948-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09948-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09948-121">-ResourceGroupName</span></span>
<span data-ttu-id="09948-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09948-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="09948-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09948-123">-SubscriptionId</span></span>
<span data-ttu-id="09948-124">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="09948-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="09948-125">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="09948-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09948-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="09948-126">-Tag</span></span>
<span data-ttu-id="09948-127">Campo Tags do recurso.</span><span class="sxs-lookup"><span data-stu-id="09948-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="09948-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09948-128">-Confirm</span></span>
<span data-ttu-id="09948-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09948-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09948-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09948-130">-WhatIf</span></span>
<span data-ttu-id="09948-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09948-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09948-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09948-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09948-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09948-133">CommonParameters</span></span>
<span data-ttu-id="09948-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09948-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09948-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09948-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09948-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09948-136">INPUTS</span></span>

### <span data-ttu-id="09948-137">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="09948-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="09948-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09948-138">OUTPUTS</span></span>

### <span data-ttu-id="09948-139">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="09948-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="09948-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09948-140">NOTES</span></span>

<span data-ttu-id="09948-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="09948-141">ALIASES</span></span>

<span data-ttu-id="09948-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="09948-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09948-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="09948-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09948-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09948-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09948-145">INPUTobject <IHanaOnAzureIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="09948-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09948-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="09948-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09948-147">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="09948-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="09948-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="09948-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="09948-149">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="09948-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="09948-150">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09948-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="09948-151">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="09948-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="09948-152">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="09948-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="09948-153">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="09948-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="09948-154">Recurso pai sendo estendido por identidades gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="09948-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="09948-155">`[SubscriptionId <String>]`: ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="09948-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="09948-156">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="09948-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="09948-157">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="09948-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="09948-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09948-158">RELATED LINKS</span></span>

