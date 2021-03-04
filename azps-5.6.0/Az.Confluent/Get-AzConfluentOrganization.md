---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893226"
---
# <span data-ttu-id="4b534-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="4b534-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="4b534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b534-102">SYNOPSIS</span></span>
<span data-ttu-id="4b534-103">Obter as propriedades de um recurso Organization específico.</span><span class="sxs-lookup"><span data-stu-id="4b534-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="4b534-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4b534-104">SYNTAX</span></span>

### <span data-ttu-id="4b534-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b534-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b534-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4b534-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b534-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b534-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b534-108">List1</span><span class="sxs-lookup"><span data-stu-id="4b534-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4b534-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4b534-109">DESCRIPTION</span></span>
<span data-ttu-id="4b534-110">Obter as propriedades de um recurso Organization específico.</span><span class="sxs-lookup"><span data-stu-id="4b534-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="4b534-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b534-111">EXAMPLES</span></span>

### <span data-ttu-id="4b534-112">Exemplo 1: Listar todas as organizações confluentes em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="4b534-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="4b534-113">Este comando lista todas as organizações confluentes sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="4b534-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="4b534-114">Exemplo 2: Listar todas as organizações confluentes em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b534-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="4b534-115">Este comando lista todas as organizações confluentes em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b534-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="4b534-116">Exemplo 3: Obter uma organização confluente pelo nome</span><span class="sxs-lookup"><span data-stu-id="4b534-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="4b534-117">Esse comando obtém uma organização confluente pelo nome.</span><span class="sxs-lookup"><span data-stu-id="4b534-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="4b534-118">Exemplo 4: Obter uma organização confluente por pipeline</span><span class="sxs-lookup"><span data-stu-id="4b534-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="4b534-119">Esse comando obtém uma organização confluente por pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b534-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="4b534-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4b534-120">PARAMETERS</span></span>

### <span data-ttu-id="4b534-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b534-121">-DefaultProfile</span></span>
<span data-ttu-id="4b534-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b534-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b534-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b534-123">-InputObject</span></span>
<span data-ttu-id="4b534-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4b534-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b534-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4b534-125">-Name</span></span>
<span data-ttu-id="4b534-126">Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="4b534-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b534-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b534-127">-ResourceGroupName</span></span>
<span data-ttu-id="4b534-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b534-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b534-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b534-129">-SubscriptionId</span></span>
<span data-ttu-id="4b534-130">ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4b534-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b534-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b534-131">CommonParameters</span></span>
<span data-ttu-id="4b534-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b534-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b534-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b534-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b534-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b534-134">INPUTS</span></span>

### <span data-ttu-id="4b534-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="4b534-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="4b534-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4b534-136">OUTPUTS</span></span>

### <span data-ttu-id="4b534-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="4b534-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="4b534-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="4b534-138">NOTES</span></span>

<span data-ttu-id="4b534-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4b534-139">ALIASES</span></span>

<span data-ttu-id="4b534-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="4b534-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b534-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4b534-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b534-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b534-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b534-143">INPUTOBJECT <IConfluentIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="4b534-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b534-144">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4b534-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b534-145">`[OrganizationName <String>]`: Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="4b534-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="4b534-146">`[ResourceGroupName <String>]`: Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b534-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="4b534-147">`[SubscriptionId <String>]`: ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4b534-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="4b534-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b534-148">RELATED LINKS</span></span>

