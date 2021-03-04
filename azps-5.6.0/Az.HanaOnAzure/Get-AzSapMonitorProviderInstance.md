---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 66f5a875f05b9c5d2fcdcc8a63eba9d149a9ba7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893323"
---
# <span data-ttu-id="dc453-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="dc453-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="dc453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc453-102">SYNOPSIS</span></span>
<span data-ttu-id="dc453-103">Obtém propriedades de uma instância do provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dc453-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="dc453-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc453-104">SYNTAX</span></span>

### <span data-ttu-id="dc453-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc453-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc453-106">Obter</span><span class="sxs-lookup"><span data-stu-id="dc453-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc453-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc453-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc453-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc453-108">DESCRIPTION</span></span>
<span data-ttu-id="dc453-109">Obtém propriedades de uma instância do provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dc453-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="dc453-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc453-110">EXAMPLES</span></span>

### <span data-ttu-id="dc453-111">Exemplo 1: Obter todas as instâncias em um monitor SAP</span><span class="sxs-lookup"><span data-stu-id="dc453-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="dc453-112">Esse comando obtém todas as instâncias em um monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="dc453-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="dc453-113">Exemplo 2: Obter uma instâncias do monitor SAP pelo nome</span><span class="sxs-lookup"><span data-stu-id="dc453-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="dc453-114">Este comando obtém uma instâncias do monitor SAP pelo nome.</span><span class="sxs-lookup"><span data-stu-id="dc453-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="dc453-115">Exemplo 3: Obter uma instâncias do monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="dc453-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="dc453-116">Este comando obtém uma instâncias do monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="dc453-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="dc453-117">Exemplo 4: Obter uma instâncias do monitor SAP por pipeline</span><span class="sxs-lookup"><span data-stu-id="dc453-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="dc453-118">Este comando obtém uma instâncias do monitor SAP por pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc453-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="dc453-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc453-119">PARAMETERS</span></span>

### <span data-ttu-id="dc453-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc453-120">-DefaultProfile</span></span>
<span data-ttu-id="dc453-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc453-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc453-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc453-122">-InputObject</span></span>
<span data-ttu-id="dc453-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dc453-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc453-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dc453-124">-Name</span></span>
<span data-ttu-id="dc453-125">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="dc453-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc453-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc453-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc453-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc453-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc453-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="dc453-128">-SapMonitorName</span></span>
<span data-ttu-id="dc453-129">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="dc453-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc453-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc453-130">-SubscriptionId</span></span>
<span data-ttu-id="dc453-131">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dc453-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc453-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="dc453-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc453-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc453-133">CommonParameters</span></span>
<span data-ttu-id="dc453-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc453-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc453-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc453-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc453-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc453-136">INPUTS</span></span>

### <span data-ttu-id="dc453-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="dc453-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="dc453-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc453-138">OUTPUTS</span></span>

### <span data-ttu-id="dc453-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="dc453-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="dc453-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc453-140">NOTES</span></span>

<span data-ttu-id="dc453-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dc453-141">ALIASES</span></span>

<span data-ttu-id="dc453-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="dc453-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc453-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dc453-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc453-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc453-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc453-145">INPUTOBJECT <IHanaOnAzureIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="dc453-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc453-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="dc453-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc453-147">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="dc453-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="dc453-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="dc453-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="dc453-149">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="dc453-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="dc453-150">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc453-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dc453-151">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="dc453-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="dc453-152">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="dc453-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="dc453-153">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="dc453-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="dc453-154">Recurso pai sendo estendido por Identidades Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="dc453-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="dc453-155">`[SubscriptionId <String>]`: ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dc453-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dc453-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="dc453-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dc453-157">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="dc453-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="dc453-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc453-158">RELATED LINKS</span></span>

