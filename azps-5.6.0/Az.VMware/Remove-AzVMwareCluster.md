---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
ms.openlocfilehash: 878691dcc0cdc2a94dd5cc8509d9d74231aaee35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889827"
---
# <span data-ttu-id="90912-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="90912-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="90912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90912-102">SYNOPSIS</span></span>
<span data-ttu-id="90912-103">Excluir um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="90912-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90912-104">SYNTAX</span></span>

### <span data-ttu-id="90912-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90912-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="90912-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90912-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90912-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90912-107">DESCRIPTION</span></span>
<span data-ttu-id="90912-108">Excluir um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="90912-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90912-109">EXAMPLES</span></span>

### <span data-ttu-id="90912-110">Exemplo 1: Excluir cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="90912-111">Excluir cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="90912-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90912-112">PARAMETERS</span></span>

### <span data-ttu-id="90912-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90912-113">-AsJob</span></span>
<span data-ttu-id="90912-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="90912-114">Run the command as a job</span></span>

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

### <span data-ttu-id="90912-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90912-115">-DefaultProfile</span></span>
<span data-ttu-id="90912-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90912-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90912-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90912-117">-InputObject</span></span>
<span data-ttu-id="90912-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="90912-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90912-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90912-119">-Name</span></span>
<span data-ttu-id="90912-120">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90912-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="90912-121">-NoWait</span></span>
<span data-ttu-id="90912-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="90912-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90912-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90912-123">-PassThru</span></span>
<span data-ttu-id="90912-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="90912-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="90912-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="90912-125">-PrivateCloudName</span></span>
<span data-ttu-id="90912-126">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-126">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90912-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90912-127">-ResourceGroupName</span></span>
<span data-ttu-id="90912-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90912-128">The name of the resource group.</span></span>
<span data-ttu-id="90912-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="90912-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90912-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90912-130">-SubscriptionId</span></span>
<span data-ttu-id="90912-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="90912-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90912-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90912-132">-Confirm</span></span>
<span data-ttu-id="90912-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90912-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90912-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90912-134">-WhatIf</span></span>
<span data-ttu-id="90912-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90912-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90912-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90912-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90912-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90912-137">CommonParameters</span></span>
<span data-ttu-id="90912-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90912-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90912-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90912-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90912-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90912-140">INPUTS</span></span>

### <span data-ttu-id="90912-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="90912-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="90912-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90912-142">OUTPUTS</span></span>

### <span data-ttu-id="90912-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90912-143">System.Boolean</span></span>

## <span data-ttu-id="90912-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="90912-144">NOTES</span></span>

<span data-ttu-id="90912-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="90912-145">ALIASES</span></span>

<span data-ttu-id="90912-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="90912-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90912-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="90912-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90912-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90912-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90912-149">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="90912-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90912-150">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="90912-151">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="90912-152">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="90912-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="90912-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90912-154">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="90912-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="90912-155">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="90912-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="90912-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90912-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="90912-157">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="90912-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="90912-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="90912-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="90912-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90912-159">RELATED LINKS</span></span>

