---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427843"
---
# <span data-ttu-id="284a5-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="284a5-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="284a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="284a5-102">SYNOPSIS</span></span>
<span data-ttu-id="284a5-103">Atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="284a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="284a5-104">SYNTAX</span></span>

### <span data-ttu-id="284a5-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="284a5-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="284a5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="284a5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="284a5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="284a5-107">DESCRIPTION</span></span>
<span data-ttu-id="284a5-108">Atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="284a5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="284a5-109">EXAMPLES</span></span>

### <span data-ttu-id="284a5-110">Exemplo 1: atualizar o tamanho do cluster por nome</span><span class="sxs-lookup"><span data-stu-id="284a5-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="284a5-111">Atualizar o tamanho do cluster por nome</span><span class="sxs-lookup"><span data-stu-id="284a5-111">Update cluster size by name</span></span>

### <span data-ttu-id="284a5-112">Exemplo 2: atualizar o tamanho do cluster por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="284a5-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="284a5-113">Atualizar o tamanho do cluster por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="284a5-113">Update cluster size by input object</span></span>

## <span data-ttu-id="284a5-114">OS</span><span class="sxs-lookup"><span data-stu-id="284a5-114">PARAMETERS</span></span>

### <span data-ttu-id="284a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="284a5-115">-AsJob</span></span>
<span data-ttu-id="284a5-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="284a5-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="284a5-117">-ClusterSize</span></span>
<span data-ttu-id="284a5-118">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="284a5-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="284a5-119">-DefaultProfile</span></span>
<span data-ttu-id="284a5-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="284a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="284a5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="284a5-121">-InputObject</span></span>
<span data-ttu-id="284a5-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="284a5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="284a5-123">-Name</span></span>
<span data-ttu-id="284a5-124">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="284a5-125">-NoWait</span></span>
<span data-ttu-id="284a5-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="284a5-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="284a5-127">-PrivateCloudName</span></span>
<span data-ttu-id="284a5-128">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="284a5-129">-ResourceGroupName</span></span>
<span data-ttu-id="284a5-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="284a5-130">The name of the resource group.</span></span>
<span data-ttu-id="284a5-131">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="284a5-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="284a5-132">-SubscriptionId</span></span>
<span data-ttu-id="284a5-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="284a5-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="284a5-134">-Confirm</span></span>
<span data-ttu-id="284a5-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="284a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="284a5-136">-WhatIf</span></span>
<span data-ttu-id="284a5-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="284a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="284a5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="284a5-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284a5-139">CommonParameters</span></span>
<span data-ttu-id="284a5-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="284a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284a5-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="284a5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284a5-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="284a5-142">INPUTS</span></span>

### <span data-ttu-id="284a5-143">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="284a5-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="284a5-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="284a5-144">OUTPUTS</span></span>

### <span data-ttu-id="284a5-145">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="284a5-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="284a5-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="284a5-146">NOTES</span></span>

<span data-ttu-id="284a5-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="284a5-147">ALIASES</span></span>

<span data-ttu-id="284a5-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="284a5-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="284a5-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="284a5-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="284a5-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="284a5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="284a5-151">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="284a5-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="284a5-152">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="284a5-153">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="284a5-154">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="284a5-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="284a5-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="284a5-156">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="284a5-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="284a5-157">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="284a5-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="284a5-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="284a5-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="284a5-159">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="284a5-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="284a5-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="284a5-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="284a5-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="284a5-161">RELATED LINKS</span></span>

