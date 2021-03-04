---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889836"
---
# <span data-ttu-id="f2462-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="f2462-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="f2462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2462-102">SYNOPSIS</span></span>
<span data-ttu-id="f2462-103">Obter um cluster pelo nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="f2462-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2462-104">SYNTAX</span></span>

### <span data-ttu-id="f2462-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2462-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2462-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f2462-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2462-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2462-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2462-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2462-108">DESCRIPTION</span></span>
<span data-ttu-id="f2462-109">Obter um cluster pelo nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="f2462-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2462-110">EXAMPLES</span></span>

### <span data-ttu-id="f2462-111">Exemplo 1: Obter cluster</span><span class="sxs-lookup"><span data-stu-id="f2462-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f2462-112">Obter cluster</span><span class="sxs-lookup"><span data-stu-id="f2462-112">Get cluster</span></span>

### <span data-ttu-id="f2462-113">Exemplo 2: Listar clusters</span><span class="sxs-lookup"><span data-stu-id="f2462-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f2462-114">Listar clusters</span><span class="sxs-lookup"><span data-stu-id="f2462-114">List clusters</span></span>

## <span data-ttu-id="f2462-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2462-115">PARAMETERS</span></span>

### <span data-ttu-id="f2462-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2462-116">-DefaultProfile</span></span>
<span data-ttu-id="f2462-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2462-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2462-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2462-118">-InputObject</span></span>
<span data-ttu-id="f2462-119">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f2462-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2462-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f2462-120">-Name</span></span>
<span data-ttu-id="f2462-121">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="f2462-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f2462-122">-PrivateCloudName</span></span>
<span data-ttu-id="f2462-123">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="f2462-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2462-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2462-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2462-125">The name of the resource group.</span></span>
<span data-ttu-id="f2462-126">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f2462-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f2462-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2462-127">-SubscriptionId</span></span>
<span data-ttu-id="f2462-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f2462-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f2462-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2462-129">CommonParameters</span></span>
<span data-ttu-id="f2462-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2462-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2462-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2462-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2462-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2462-132">INPUTS</span></span>

### <span data-ttu-id="f2462-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f2462-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f2462-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2462-134">OUTPUTS</span></span>

### <span data-ttu-id="f2462-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="f2462-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="f2462-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2462-136">NOTES</span></span>

<span data-ttu-id="f2462-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f2462-137">ALIASES</span></span>

<span data-ttu-id="f2462-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="f2462-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2462-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f2462-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2462-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2462-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2462-141">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="f2462-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2462-142">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f2462-143">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f2462-144">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f2462-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f2462-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2462-146">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="f2462-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f2462-147">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f2462-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f2462-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2462-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f2462-149">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f2462-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f2462-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f2462-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f2462-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2462-151">RELATED LINKS</span></span>

