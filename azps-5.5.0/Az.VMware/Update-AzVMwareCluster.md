---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112349"
---
# <span data-ttu-id="dfb98-101">Update-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="dfb98-101">Update-AzVMwareCluster</span></span>

## <span data-ttu-id="dfb98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfb98-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb98-103">Atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="dfb98-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfb98-104">SYNTAX</span></span>

### <span data-ttu-id="dfb98-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dfb98-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dfb98-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dfb98-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfb98-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfb98-107">DESCRIPTION</span></span>
<span data-ttu-id="dfb98-108">Atualizar um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="dfb98-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dfb98-109">EXAMPLES</span></span>

### <span data-ttu-id="dfb98-110">Exemplo 1: Atualizar o tamanho do cluster por nome</span><span class="sxs-lookup"><span data-stu-id="dfb98-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="dfb98-111">Atualizar o tamanho do cluster por nome</span><span class="sxs-lookup"><span data-stu-id="dfb98-111">Update cluster size by name</span></span>

### <span data-ttu-id="dfb98-112">Exemplo 2: Atualizar o tamanho do cluster por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="dfb98-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="dfb98-113">Atualizar o tamanho do cluster por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="dfb98-113">Update cluster size by input object</span></span>

## <span data-ttu-id="dfb98-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfb98-114">PARAMETERS</span></span>

### <span data-ttu-id="dfb98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfb98-115">-AsJob</span></span>
<span data-ttu-id="dfb98-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="dfb98-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dfb98-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="dfb98-117">-ClusterSize</span></span>
<span data-ttu-id="dfb98-118">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="dfb98-118">The cluster size</span></span>

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

### <span data-ttu-id="dfb98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb98-119">-DefaultProfile</span></span>
<span data-ttu-id="dfb98-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfb98-121">-InputObject</span></span>
<span data-ttu-id="dfb98-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="dfb98-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb98-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfb98-123">-Name</span></span>
<span data-ttu-id="dfb98-124">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="dfb98-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dfb98-125">-NoWait</span></span>
<span data-ttu-id="dfb98-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="dfb98-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfb98-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="dfb98-127">-PrivateCloudName</span></span>
<span data-ttu-id="dfb98-128">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="dfb98-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb98-129">-ResourceGroupName</span></span>
<span data-ttu-id="dfb98-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfb98-130">The name of the resource group.</span></span>
<span data-ttu-id="dfb98-131">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dfb98-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dfb98-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfb98-132">-SubscriptionId</span></span>
<span data-ttu-id="dfb98-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dfb98-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dfb98-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dfb98-134">-Confirm</span></span>
<span data-ttu-id="dfb98-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb98-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb98-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb98-136">-WhatIf</span></span>
<span data-ttu-id="dfb98-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dfb98-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb98-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfb98-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb98-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb98-139">CommonParameters</span></span>
<span data-ttu-id="dfb98-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb98-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb98-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfb98-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb98-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="dfb98-142">INPUTS</span></span>

### <span data-ttu-id="dfb98-143">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="dfb98-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="dfb98-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="dfb98-144">OUTPUTS</span></span>

### <span data-ttu-id="dfb98-145">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="dfb98-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="dfb98-146">Notas</span><span class="sxs-lookup"><span data-stu-id="dfb98-146">NOTES</span></span>

<span data-ttu-id="dfb98-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="dfb98-147">ALIASES</span></span>

<span data-ttu-id="dfb98-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="dfb98-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfb98-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dfb98-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfb98-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfb98-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfb98-151">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="dfb98-151">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfb98-152">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="dfb98-153">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="dfb98-154">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="dfb98-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="dfb98-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfb98-156">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="dfb98-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="dfb98-157">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="dfb98-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="dfb98-158">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfb98-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dfb98-159">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dfb98-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="dfb98-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dfb98-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="dfb98-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfb98-161">RELATED LINKS</span></span>

