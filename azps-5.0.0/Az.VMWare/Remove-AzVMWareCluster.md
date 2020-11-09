---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282104"
---
# <span data-ttu-id="52cfb-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="52cfb-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="52cfb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="52cfb-103">Excluir um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="52cfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52cfb-104">SYNTAX</span></span>

### <span data-ttu-id="52cfb-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="52cfb-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="52cfb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52cfb-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52cfb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52cfb-107">DESCRIPTION</span></span>
<span data-ttu-id="52cfb-108">Excluir um cluster em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="52cfb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52cfb-109">EXAMPLES</span></span>

### <span data-ttu-id="52cfb-110">Exemplo 1: excluir cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="52cfb-111">Excluir cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="52cfb-112">OS</span><span class="sxs-lookup"><span data-stu-id="52cfb-112">PARAMETERS</span></span>

### <span data-ttu-id="52cfb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52cfb-113">-AsJob</span></span>
<span data-ttu-id="52cfb-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="52cfb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="52cfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52cfb-115">-DefaultProfile</span></span>
<span data-ttu-id="52cfb-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52cfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52cfb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52cfb-117">-InputObject</span></span>
<span data-ttu-id="52cfb-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52cfb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="52cfb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="52cfb-119">-Name</span></span>
<span data-ttu-id="52cfb-120">Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-120">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="52cfb-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="52cfb-121">-NoWait</span></span>
<span data-ttu-id="52cfb-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="52cfb-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52cfb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52cfb-123">-PassThru</span></span>
<span data-ttu-id="52cfb-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="52cfb-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="52cfb-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="52cfb-125">-PrivateCloudName</span></span>
<span data-ttu-id="52cfb-126">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="52cfb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52cfb-127">-ResourceGroupName</span></span>
<span data-ttu-id="52cfb-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52cfb-128">The name of the resource group.</span></span>
<span data-ttu-id="52cfb-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="52cfb-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="52cfb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52cfb-130">-SubscriptionId</span></span>
<span data-ttu-id="52cfb-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="52cfb-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="52cfb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52cfb-132">-Confirm</span></span>
<span data-ttu-id="52cfb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52cfb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52cfb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cfb-134">-WhatIf</span></span>
<span data-ttu-id="52cfb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52cfb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52cfb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52cfb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52cfb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cfb-137">CommonParameters</span></span>
<span data-ttu-id="52cfb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52cfb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cfb-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52cfb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cfb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52cfb-140">INPUTS</span></span>

### <span data-ttu-id="52cfb-141">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="52cfb-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="52cfb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52cfb-142">OUTPUTS</span></span>

### <span data-ttu-id="52cfb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52cfb-143">System.Boolean</span></span>

## <span data-ttu-id="52cfb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52cfb-144">NOTES</span></span>

<span data-ttu-id="52cfb-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52cfb-145">ALIASES</span></span>

<span data-ttu-id="52cfb-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="52cfb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52cfb-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="52cfb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52cfb-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52cfb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52cfb-149">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="52cfb-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52cfb-150">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="52cfb-151">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="52cfb-152">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="52cfb-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="52cfb-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52cfb-154">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="52cfb-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="52cfb-155">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="52cfb-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="52cfb-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52cfb-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="52cfb-157">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="52cfb-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="52cfb-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="52cfb-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="52cfb-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52cfb-159">RELATED LINKS</span></span>

