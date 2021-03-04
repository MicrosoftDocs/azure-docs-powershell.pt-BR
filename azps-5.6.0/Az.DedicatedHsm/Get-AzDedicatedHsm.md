---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887187"
---
# <span data-ttu-id="12659-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="12659-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="12659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12659-102">SYNOPSIS</span></span>
<span data-ttu-id="12659-103">Obtém o HSM dedicado especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="12659-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="12659-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12659-104">SYNTAX</span></span>

### <span data-ttu-id="12659-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12659-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="12659-106">Obter</span><span class="sxs-lookup"><span data-stu-id="12659-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12659-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12659-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12659-108">Listar</span><span class="sxs-lookup"><span data-stu-id="12659-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="12659-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12659-109">DESCRIPTION</span></span>
<span data-ttu-id="12659-110">Obtém o HSM dedicado especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="12659-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="12659-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12659-111">EXAMPLES</span></span>

### <span data-ttu-id="12659-112">Exemplo 1: Obter todos os HSM dedicados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="12659-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="12659-113">Este comando obtém todos os HSM Dedicados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="12659-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="12659-114">Exemplo 2: Obter todos os HSM dedicados em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12659-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="12659-115">Esse comando obtém todo o HSM Dedicado em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12659-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="12659-116">Exemplo 3: Obter um HSM dedicado pelo nome</span><span class="sxs-lookup"><span data-stu-id="12659-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="12659-117">Este comando obtém um HSM dedicado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="12659-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="12659-118">Exemplo 4: Obter um HSM dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="12659-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="12659-119">Este comando obtém um HSM dedicado por objeto.</span><span class="sxs-lookup"><span data-stu-id="12659-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="12659-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12659-120">PARAMETERS</span></span>

### <span data-ttu-id="12659-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12659-121">-DefaultProfile</span></span>
<span data-ttu-id="12659-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12659-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12659-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12659-123">-InputObject</span></span>
<span data-ttu-id="12659-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="12659-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12659-125">-Name</span><span class="sxs-lookup"><span data-stu-id="12659-125">-Name</span></span>
<span data-ttu-id="12659-126">O nome do HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="12659-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="12659-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12659-127">-ResourceGroupName</span></span>
<span data-ttu-id="12659-128">O nome do Grupo de Recursos ao qual o hsm dedicado pertence.</span><span class="sxs-lookup"><span data-stu-id="12659-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="12659-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12659-129">-SubscriptionId</span></span>
<span data-ttu-id="12659-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12659-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12659-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="12659-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12659-132">-Top</span><span class="sxs-lookup"><span data-stu-id="12659-132">-Top</span></span>
<span data-ttu-id="12659-133">Número máximo de resultados a retornar.</span><span class="sxs-lookup"><span data-stu-id="12659-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12659-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12659-134">CommonParameters</span></span>
<span data-ttu-id="12659-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12659-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12659-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12659-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12659-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12659-137">INPUTS</span></span>

### <span data-ttu-id="12659-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="12659-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="12659-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12659-139">OUTPUTS</span></span>

### <span data-ttu-id="12659-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="12659-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="12659-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="12659-141">NOTES</span></span>

<span data-ttu-id="12659-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="12659-142">ALIASES</span></span>

<span data-ttu-id="12659-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="12659-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12659-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="12659-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12659-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12659-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12659-146">INPUTOBJECT <IDedicatedHsmIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="12659-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12659-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="12659-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12659-148">`[Name <String>]`: Nome do Hsm dedicado</span><span class="sxs-lookup"><span data-stu-id="12659-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="12659-149">`[ResourceGroupName <String>]`: O nome do Grupo de Recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="12659-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="12659-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12659-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12659-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="12659-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12659-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12659-152">RELATED LINKS</span></span>

