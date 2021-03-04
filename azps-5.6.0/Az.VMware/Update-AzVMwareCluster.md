---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: f708d1b752c0d8106d7a8f9f7613fa74b6b19937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890035"
---
# <span data-ttu-id="56d22-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="56d22-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="56d22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56d22-102">SYNOPSIS</span></span>
<span data-ttu-id="56d22-103">Atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="56d22-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56d22-104">SYNTAX</span></span>

### <span data-ttu-id="56d22-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56d22-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56d22-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="56d22-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56d22-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56d22-107">DESCRIPTION</span></span>
<span data-ttu-id="56d22-108">Atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="56d22-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56d22-109">EXAMPLES</span></span>

### <span data-ttu-id="56d22-110">Exemplo 1: Atualizar o tamanho do cluster pelo nome</span><span class="sxs-lookup"><span data-stu-id="56d22-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="56d22-111">Atualizar o tamanho do cluster pelo nome</span><span class="sxs-lookup"><span data-stu-id="56d22-111">Update cluster size by name</span></span>

### <span data-ttu-id="56d22-112">Exemplo 2: Atualizar o tamanho do cluster por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="56d22-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="56d22-113">Atualizar o tamanho do cluster por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="56d22-113">Update cluster size by input object</span></span>

## <span data-ttu-id="56d22-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56d22-114">PARAMETERS</span></span>

### <span data-ttu-id="56d22-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56d22-115">-AsJob</span></span>
<span data-ttu-id="56d22-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="56d22-116">Run the command as a job</span></span>

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

### <span data-ttu-id="56d22-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="56d22-117">-ClusterSize</span></span>
<span data-ttu-id="56d22-118">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="56d22-118">The cluster size</span></span>

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

### <span data-ttu-id="56d22-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d22-119">-DefaultProfile</span></span>
<span data-ttu-id="56d22-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56d22-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d22-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d22-121">-InputObject</span></span>
<span data-ttu-id="56d22-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="56d22-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56d22-123">-Name</span><span class="sxs-lookup"><span data-stu-id="56d22-123">-Name</span></span>
<span data-ttu-id="56d22-124">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="56d22-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="56d22-125">-NoWait</span></span>
<span data-ttu-id="56d22-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="56d22-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="56d22-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="56d22-127">-PrivateCloudName</span></span>
<span data-ttu-id="56d22-128">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="56d22-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d22-129">-ResourceGroupName</span></span>
<span data-ttu-id="56d22-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56d22-130">The name of the resource group.</span></span>
<span data-ttu-id="56d22-131">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="56d22-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56d22-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56d22-132">-SubscriptionId</span></span>
<span data-ttu-id="56d22-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="56d22-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56d22-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56d22-134">-Confirm</span></span>
<span data-ttu-id="56d22-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d22-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d22-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d22-136">-WhatIf</span></span>
<span data-ttu-id="56d22-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56d22-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d22-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56d22-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d22-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d22-139">CommonParameters</span></span>
<span data-ttu-id="56d22-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d22-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d22-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56d22-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d22-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56d22-142">INPUTS</span></span>

### <span data-ttu-id="56d22-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="56d22-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="56d22-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56d22-144">OUTPUTS</span></span>

### <span data-ttu-id="56d22-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="56d22-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="56d22-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="56d22-146">NOTES</span></span>

<span data-ttu-id="56d22-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="56d22-147">ALIASES</span></span>

<span data-ttu-id="56d22-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="56d22-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56d22-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="56d22-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56d22-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56d22-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56d22-151">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="56d22-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56d22-152">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="56d22-153">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="56d22-154">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="56d22-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="56d22-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56d22-156">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="56d22-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="56d22-157">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="56d22-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="56d22-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56d22-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56d22-159">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="56d22-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="56d22-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="56d22-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="56d22-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56d22-161">RELATED LINKS</span></span>

