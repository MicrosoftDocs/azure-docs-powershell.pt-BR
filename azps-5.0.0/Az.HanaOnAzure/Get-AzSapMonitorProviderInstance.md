---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115342"
---
# <span data-ttu-id="1cbf2-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="1cbf2-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="1cbf2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cbf2-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbf2-103">Obtém as propriedades de uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="1cbf2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cbf2-104">SYNTAX</span></span>

### <span data-ttu-id="1cbf2-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="1cbf2-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cbf2-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1cbf2-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cbf2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1cbf2-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cbf2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cbf2-108">DESCRIPTION</span></span>
<span data-ttu-id="1cbf2-109">Obtém as propriedades de uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="1cbf2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cbf2-110">EXAMPLES</span></span>

### <span data-ttu-id="1cbf2-111">Exemplo 1: obter todas as instâncias em um monitor SAP</span><span class="sxs-lookup"><span data-stu-id="1cbf2-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="1cbf2-112">Esse comando obtém todas as instâncias em um monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="1cbf2-113">Exemplo 2: obter uma instância do monitor SAP por nome</span><span class="sxs-lookup"><span data-stu-id="1cbf2-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="1cbf2-114">Esse comando obtém uma instância do monitor SAP por nome.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="1cbf2-115">Exemplo 3: obter uma instância do monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="1cbf2-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="1cbf2-116">Esse comando obtém uma instância do monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="1cbf2-117">Exemplo 4: obter uma instância do monitor SAP por pipeline</span><span class="sxs-lookup"><span data-stu-id="1cbf2-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="1cbf2-118">Esse comando obtém uma instância do monitor SAP por pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="1cbf2-119">OS</span><span class="sxs-lookup"><span data-stu-id="1cbf2-119">PARAMETERS</span></span>

### <span data-ttu-id="1cbf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbf2-120">-DefaultProfile</span></span>
<span data-ttu-id="1cbf2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cbf2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cbf2-122">-InputObject</span></span>
<span data-ttu-id="1cbf2-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1cbf2-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cbf2-124">-Name</span></span>
<span data-ttu-id="1cbf2-125">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="1cbf2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbf2-126">-ResourceGroupName</span></span>
<span data-ttu-id="1cbf2-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="1cbf2-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="1cbf2-128">-SapMonitorName</span></span>
<span data-ttu-id="1cbf2-129">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="1cbf2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cbf2-130">-SubscriptionId</span></span>
<span data-ttu-id="1cbf2-131">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1cbf2-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1cbf2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbf2-133">CommonParameters</span></span>
<span data-ttu-id="1cbf2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbf2-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cbf2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbf2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cbf2-136">INPUTS</span></span>

### <span data-ttu-id="1cbf2-137">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="1cbf2-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="1cbf2-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cbf2-138">OUTPUTS</span></span>

### <span data-ttu-id="1cbf2-139">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="1cbf2-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="1cbf2-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cbf2-140">NOTES</span></span>

<span data-ttu-id="1cbf2-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1cbf2-141">ALIASES</span></span>

<span data-ttu-id="1cbf2-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="1cbf2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1cbf2-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1cbf2-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1cbf2-145">INPUTobject <IHanaOnAzureIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="1cbf2-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1cbf2-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1cbf2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1cbf2-147">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="1cbf2-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="1cbf2-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="1cbf2-149">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="1cbf2-150">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1cbf2-151">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="1cbf2-152">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="1cbf2-153">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="1cbf2-154">Recurso pai sendo estendido por identidades gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="1cbf2-155">`[SubscriptionId <String>]`: ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1cbf2-156">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1cbf2-157">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="1cbf2-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="1cbf2-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cbf2-158">RELATED LINKS</span></span>

