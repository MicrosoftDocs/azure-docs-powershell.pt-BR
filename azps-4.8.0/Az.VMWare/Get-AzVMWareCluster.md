---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947441"
---
# <span data-ttu-id="92f86-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="92f86-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="92f86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92f86-102">SYNOPSIS</span></span>
<span data-ttu-id="92f86-103">Obter um cluster por nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="92f86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92f86-104">SYNTAX</span></span>

### <span data-ttu-id="92f86-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="92f86-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92f86-106">Obter</span><span class="sxs-lookup"><span data-stu-id="92f86-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92f86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92f86-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="92f86-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92f86-108">DESCRIPTION</span></span>
<span data-ttu-id="92f86-109">Obter um cluster por nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="92f86-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92f86-110">EXAMPLES</span></span>

### <span data-ttu-id="92f86-111">Exemplo 1: obter cluster</span><span class="sxs-lookup"><span data-stu-id="92f86-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="92f86-112">Obter cluster</span><span class="sxs-lookup"><span data-stu-id="92f86-112">Get cluster</span></span>

### <span data-ttu-id="92f86-113">Exemplo 2: listar clusters</span><span class="sxs-lookup"><span data-stu-id="92f86-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="92f86-114">Agrupamentos de lista</span><span class="sxs-lookup"><span data-stu-id="92f86-114">List clusters</span></span>

## <span data-ttu-id="92f86-115">OS</span><span class="sxs-lookup"><span data-stu-id="92f86-115">PARAMETERS</span></span>

### <span data-ttu-id="92f86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f86-116">-DefaultProfile</span></span>
<span data-ttu-id="92f86-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92f86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f86-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92f86-118">-InputObject</span></span>
<span data-ttu-id="92f86-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="92f86-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92f86-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="92f86-120">-Name</span></span>
<span data-ttu-id="92f86-121">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f86-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="92f86-122">-PrivateCloudName</span></span>
<span data-ttu-id="92f86-123">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="92f86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f86-124">-ResourceGroupName</span></span>
<span data-ttu-id="92f86-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92f86-125">The name of the resource group.</span></span>
<span data-ttu-id="92f86-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92f86-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="92f86-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92f86-127">-SubscriptionId</span></span>
<span data-ttu-id="92f86-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="92f86-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="92f86-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f86-129">CommonParameters</span></span>
<span data-ttu-id="92f86-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f86-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f86-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92f86-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f86-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92f86-132">INPUTS</span></span>

### <span data-ttu-id="92f86-133">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="92f86-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="92f86-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92f86-134">OUTPUTS</span></span>

### <span data-ttu-id="92f86-135">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="92f86-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="92f86-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92f86-136">NOTES</span></span>

<span data-ttu-id="92f86-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="92f86-137">ALIASES</span></span>

<span data-ttu-id="92f86-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="92f86-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92f86-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="92f86-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92f86-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92f86-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92f86-141">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="92f86-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92f86-142">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="92f86-143">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="92f86-144">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="92f86-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="92f86-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92f86-146">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="92f86-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="92f86-147">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="92f86-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="92f86-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92f86-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92f86-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92f86-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="92f86-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="92f86-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="92f86-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92f86-151">RELATED LINKS</span></span>

