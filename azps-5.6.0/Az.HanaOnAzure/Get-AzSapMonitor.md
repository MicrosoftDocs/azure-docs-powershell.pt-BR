---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 0de9aa6dd623efa379a6123570e766d30c850ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893324"
---
# <span data-ttu-id="b0486-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="b0486-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="b0486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0486-102">SYNOPSIS</span></span>
<span data-ttu-id="b0486-103">Obtém propriedades de um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b0486-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="b0486-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b0486-104">SYNTAX</span></span>

### <span data-ttu-id="b0486-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b0486-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0486-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b0486-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0486-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0486-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b0486-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b0486-108">DESCRIPTION</span></span>
<span data-ttu-id="b0486-109">Obtém propriedades de um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b0486-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="b0486-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0486-110">EXAMPLES</span></span>

### <span data-ttu-id="b0486-111">Exemplo 1: Obter todos os monitores SAP em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="b0486-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b0486-112">Este comando obtém monitores SAP sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b0486-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="b0486-113">Exemplo 2: Obter um monitor SAP pelo nome</span><span class="sxs-lookup"><span data-stu-id="b0486-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b0486-114">Este comando obtém um monitor SAP pelo nome.</span><span class="sxs-lookup"><span data-stu-id="b0486-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="b0486-115">Exemplo 3: Obter um monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="b0486-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b0486-116">Esse comando obtém um monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="b0486-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="b0486-117">Exemplo 4: Obter um monitor SAP por pipeline</span><span class="sxs-lookup"><span data-stu-id="b0486-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b0486-118">Esse comando obtém um monitor SAP por pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0486-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="b0486-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b0486-119">PARAMETERS</span></span>

### <span data-ttu-id="b0486-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0486-120">-DefaultProfile</span></span>
<span data-ttu-id="b0486-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0486-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0486-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0486-122">-InputObject</span></span>
<span data-ttu-id="b0486-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b0486-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b0486-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b0486-124">-Name</span></span>
<span data-ttu-id="b0486-125">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="b0486-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0486-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0486-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0486-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0486-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0486-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0486-128">-SubscriptionId</span></span>
<span data-ttu-id="b0486-129">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b0486-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0486-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b0486-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b0486-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0486-131">CommonParameters</span></span>
<span data-ttu-id="b0486-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0486-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0486-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0486-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0486-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0486-134">INPUTS</span></span>

### <span data-ttu-id="b0486-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="b0486-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="b0486-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b0486-136">OUTPUTS</span></span>

### <span data-ttu-id="b0486-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="b0486-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="b0486-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="b0486-138">NOTES</span></span>

<span data-ttu-id="b0486-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b0486-139">ALIASES</span></span>

<span data-ttu-id="b0486-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b0486-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0486-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b0486-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0486-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0486-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0486-143">INPUTOBJECT <IHanaOnAzureIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b0486-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0486-144">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b0486-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0486-145">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="b0486-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="b0486-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="b0486-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="b0486-147">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="b0486-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="b0486-148">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0486-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b0486-149">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="b0486-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="b0486-150">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="b0486-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="b0486-151">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="b0486-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="b0486-152">Recurso pai sendo estendido por Identidades Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="b0486-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="b0486-153">`[SubscriptionId <String>]`: ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b0486-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0486-154">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b0486-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b0486-155">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="b0486-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="b0486-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0486-156">RELATED LINKS</span></span>

