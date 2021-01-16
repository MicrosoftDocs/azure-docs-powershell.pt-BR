---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262233"
---
# <span data-ttu-id="d5a88-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="d5a88-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="d5a88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5a88-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a88-103">Obtém as propriedades de um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d5a88-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="d5a88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a88-104">SYNTAX</span></span>

### <span data-ttu-id="d5a88-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5a88-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d5a88-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d5a88-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d5a88-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d5a88-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d5a88-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5a88-108">DESCRIPTION</span></span>
<span data-ttu-id="d5a88-109">Obtém as propriedades de um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d5a88-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="d5a88-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5a88-110">EXAMPLES</span></span>

### <span data-ttu-id="d5a88-111">Exemplo 1: obter todos os monitores SAP sob uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d5a88-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d5a88-112">Este comando obtém monitores da SAP sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d5a88-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="d5a88-113">Exemplo 2: obter um monitor SAP por nome</span><span class="sxs-lookup"><span data-stu-id="d5a88-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d5a88-114">Esse comando obtém um monitor SAP por nome.</span><span class="sxs-lookup"><span data-stu-id="d5a88-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="d5a88-115">Exemplo 3: obter um monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="d5a88-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d5a88-116">Esse comando obtém um monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="d5a88-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="d5a88-117">Exemplo 4: obter um monitor SAP por pipeline</span><span class="sxs-lookup"><span data-stu-id="d5a88-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d5a88-118">Esse comando obtém um monitor SAP por pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5a88-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="d5a88-119">OS</span><span class="sxs-lookup"><span data-stu-id="d5a88-119">PARAMETERS</span></span>

### <span data-ttu-id="d5a88-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a88-120">-DefaultProfile</span></span>
<span data-ttu-id="d5a88-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a88-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a88-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5a88-122">-InputObject</span></span>
<span data-ttu-id="d5a88-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d5a88-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5a88-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5a88-124">-Name</span></span>
<span data-ttu-id="d5a88-125">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="d5a88-125">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="d5a88-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a88-126">-ResourceGroupName</span></span>
<span data-ttu-id="d5a88-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5a88-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="d5a88-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5a88-128">-SubscriptionId</span></span>
<span data-ttu-id="d5a88-129">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a88-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5a88-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5a88-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5a88-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a88-131">CommonParameters</span></span>
<span data-ttu-id="d5a88-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a88-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a88-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5a88-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a88-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5a88-134">INPUTS</span></span>

### <span data-ttu-id="d5a88-135">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="d5a88-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="d5a88-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5a88-136">OUTPUTS</span></span>

### <span data-ttu-id="d5a88-137">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="d5a88-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="d5a88-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5a88-138">NOTES</span></span>

<span data-ttu-id="d5a88-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d5a88-139">ALIASES</span></span>

<span data-ttu-id="d5a88-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d5a88-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5a88-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d5a88-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5a88-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5a88-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5a88-143">INPUTobject <IHanaOnAzureIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d5a88-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5a88-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d5a88-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5a88-145">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="d5a88-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="d5a88-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="d5a88-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="d5a88-147">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="d5a88-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="d5a88-148">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5a88-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d5a88-149">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="d5a88-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="d5a88-150">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="d5a88-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="d5a88-151">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="d5a88-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="d5a88-152">Recurso pai sendo estendido por identidades gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="d5a88-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="d5a88-153">`[SubscriptionId <String>]`: ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a88-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d5a88-154">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5a88-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d5a88-155">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="d5a88-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="d5a88-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5a88-156">RELATED LINKS</span></span>

