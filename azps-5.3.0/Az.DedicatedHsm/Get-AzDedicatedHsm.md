---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432877"
---
# <span data-ttu-id="45612-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="45612-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="45612-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45612-102">SYNOPSIS</span></span>
<span data-ttu-id="45612-103">Obtém o HSM dedicado do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="45612-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="45612-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45612-104">SYNTAX</span></span>

### <span data-ttu-id="45612-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="45612-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="45612-106">Obter</span><span class="sxs-lookup"><span data-stu-id="45612-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45612-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45612-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45612-108">Programação</span><span class="sxs-lookup"><span data-stu-id="45612-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="45612-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45612-109">DESCRIPTION</span></span>
<span data-ttu-id="45612-110">Obtém o HSM dedicado do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="45612-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="45612-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45612-111">EXAMPLES</span></span>

### <span data-ttu-id="45612-112">Exemplo 1: obter todo o HSM dedicado sob uma assinatura</span><span class="sxs-lookup"><span data-stu-id="45612-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="45612-113">Este comando obtém todo o HSM dedicado sob uma assinatura</span><span class="sxs-lookup"><span data-stu-id="45612-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="45612-114">Exemplo 2: obter todo o HSM dedicado em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45612-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="45612-115">Esse comando obtém todo o HSM dedicado em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45612-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="45612-116">Exemplo 3: obter um HSM exclusivo por nome</span><span class="sxs-lookup"><span data-stu-id="45612-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="45612-117">Esse comando obtém um HSM exclusivo por nome.</span><span class="sxs-lookup"><span data-stu-id="45612-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="45612-118">Exemplo 4: obter um HSM exclusivo por objeto</span><span class="sxs-lookup"><span data-stu-id="45612-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="45612-119">Esse comando obtém um HSM exclusivo por objeto.</span><span class="sxs-lookup"><span data-stu-id="45612-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="45612-120">OS</span><span class="sxs-lookup"><span data-stu-id="45612-120">PARAMETERS</span></span>

### <span data-ttu-id="45612-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45612-121">-DefaultProfile</span></span>
<span data-ttu-id="45612-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45612-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45612-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45612-123">-InputObject</span></span>
<span data-ttu-id="45612-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="45612-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45612-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="45612-125">-Name</span></span>
<span data-ttu-id="45612-126">O nome do HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="45612-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="45612-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45612-127">-ResourceGroupName</span></span>
<span data-ttu-id="45612-128">O nome do grupo de recursos ao qual o HSM dedicado pertence.</span><span class="sxs-lookup"><span data-stu-id="45612-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="45612-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45612-129">-SubscriptionId</span></span>
<span data-ttu-id="45612-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="45612-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="45612-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="45612-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="45612-132">-Início</span><span class="sxs-lookup"><span data-stu-id="45612-132">-Top</span></span>
<span data-ttu-id="45612-133">Número máximo de resultados a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="45612-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="45612-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45612-134">CommonParameters</span></span>
<span data-ttu-id="45612-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45612-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45612-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45612-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45612-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45612-137">INPUTS</span></span>

### <span data-ttu-id="45612-138">Microsoft. Azure. PowerShell. cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="45612-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="45612-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45612-139">OUTPUTS</span></span>

### <span data-ttu-id="45612-140">Microsoft. Azure. PowerShell. cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="45612-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="45612-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45612-141">NOTES</span></span>

<span data-ttu-id="45612-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="45612-142">ALIASES</span></span>

<span data-ttu-id="45612-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="45612-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45612-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="45612-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45612-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45612-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45612-146">INPUTobject <IDedicatedHsmIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="45612-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45612-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="45612-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45612-148">`[Name <String>]`: Nome do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="45612-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="45612-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="45612-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="45612-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="45612-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="45612-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="45612-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="45612-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45612-152">RELATED LINKS</span></span>

