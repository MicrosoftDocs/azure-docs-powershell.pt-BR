---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282107"
---
# <span data-ttu-id="acaa1-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="acaa1-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="acaa1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="acaa1-103">Obter uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-103">Get a private cloud</span></span>

## <span data-ttu-id="acaa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acaa1-104">SYNTAX</span></span>

### <span data-ttu-id="acaa1-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="acaa1-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="acaa1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="acaa1-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="acaa1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="acaa1-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="acaa1-108">Programação</span><span class="sxs-lookup"><span data-stu-id="acaa1-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="acaa1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acaa1-109">DESCRIPTION</span></span>
<span data-ttu-id="acaa1-110">Obter uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-110">Get a private cloud</span></span>

## <span data-ttu-id="acaa1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acaa1-111">EXAMPLES</span></span>

### <span data-ttu-id="acaa1-112">Exemplo 1: lista de nuvem privada em assinatura</span><span class="sxs-lookup"><span data-stu-id="acaa1-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="acaa1-113">Lista de nuvem privada em assinatura</span><span class="sxs-lookup"><span data-stu-id="acaa1-113">List private cloud under subscription</span></span>

### <span data-ttu-id="acaa1-114">Exemplo 2: lista de nuvem privada em grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="acaa1-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="acaa1-115">Lista de nuvem privada em grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="acaa1-115">List private cloud under resource group</span></span>

### <span data-ttu-id="acaa1-116">Exemplo 3: obter nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="acaa1-117">Obter nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-117">Get private cloud</span></span>

## <span data-ttu-id="acaa1-118">OS</span><span class="sxs-lookup"><span data-stu-id="acaa1-118">PARAMETERS</span></span>

### <span data-ttu-id="acaa1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acaa1-119">-DefaultProfile</span></span>
<span data-ttu-id="acaa1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acaa1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acaa1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acaa1-121">-InputObject</span></span>
<span data-ttu-id="acaa1-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="acaa1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acaa1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="acaa1-123">-Name</span></span>
<span data-ttu-id="acaa1-124">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acaa1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acaa1-125">-ResourceGroupName</span></span>
<span data-ttu-id="acaa1-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acaa1-126">The name of the resource group.</span></span>
<span data-ttu-id="acaa1-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="acaa1-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="acaa1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acaa1-128">-SubscriptionId</span></span>
<span data-ttu-id="acaa1-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="acaa1-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="acaa1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acaa1-130">CommonParameters</span></span>
<span data-ttu-id="acaa1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acaa1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acaa1-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acaa1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acaa1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acaa1-133">INPUTS</span></span>

### <span data-ttu-id="acaa1-134">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="acaa1-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="acaa1-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acaa1-135">OUTPUTS</span></span>

### <span data-ttu-id="acaa1-136">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="acaa1-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="acaa1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acaa1-137">NOTES</span></span>

<span data-ttu-id="acaa1-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="acaa1-138">ALIASES</span></span>

<span data-ttu-id="acaa1-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="acaa1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acaa1-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="acaa1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acaa1-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="acaa1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acaa1-142">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="acaa1-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="acaa1-143">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="acaa1-144">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="acaa1-145">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="acaa1-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="acaa1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="acaa1-147">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="acaa1-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="acaa1-148">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="acaa1-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="acaa1-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acaa1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="acaa1-150">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="acaa1-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="acaa1-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="acaa1-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="acaa1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acaa1-152">RELATED LINKS</span></span>

