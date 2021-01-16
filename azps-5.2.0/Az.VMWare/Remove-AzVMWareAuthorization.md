---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258182"
---
# <span data-ttu-id="9d860-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="9d860-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="9d860-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d860-102">SYNOPSIS</span></span>
<span data-ttu-id="9d860-103">Excluir uma autorização de circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="9d860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d860-104">SYNTAX</span></span>

### <span data-ttu-id="9d860-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d860-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9d860-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d860-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d860-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d860-107">DESCRIPTION</span></span>
<span data-ttu-id="9d860-108">Excluir uma autorização de circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="9d860-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d860-109">EXAMPLES</span></span>

### <span data-ttu-id="9d860-110">Exemplo 1: excluir a autorização da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="9d860-111">Excluir a autorização para nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="9d860-112">OS</span><span class="sxs-lookup"><span data-stu-id="9d860-112">PARAMETERS</span></span>

### <span data-ttu-id="9d860-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d860-113">-AsJob</span></span>
<span data-ttu-id="9d860-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9d860-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9d860-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d860-115">-DefaultProfile</span></span>
<span data-ttu-id="9d860-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d860-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d860-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d860-117">-InputObject</span></span>
<span data-ttu-id="9d860-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9d860-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9d860-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d860-119">-Name</span></span>
<span data-ttu-id="9d860-120">Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d860-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9d860-121">-NoWait</span></span>
<span data-ttu-id="9d860-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9d860-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d860-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d860-123">-PassThru</span></span>
<span data-ttu-id="9d860-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9d860-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9d860-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9d860-125">-PrivateCloudName</span></span>
<span data-ttu-id="9d860-126">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="9d860-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d860-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d860-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d860-128">The name of the resource group.</span></span>
<span data-ttu-id="9d860-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9d860-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9d860-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d860-130">-SubscriptionId</span></span>
<span data-ttu-id="9d860-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="9d860-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9d860-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d860-132">-Confirm</span></span>
<span data-ttu-id="9d860-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d860-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d860-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d860-134">-WhatIf</span></span>
<span data-ttu-id="9d860-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d860-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d860-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d860-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d860-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d860-137">CommonParameters</span></span>
<span data-ttu-id="9d860-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d860-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d860-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d860-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d860-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d860-140">INPUTS</span></span>

### <span data-ttu-id="9d860-141">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9d860-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9d860-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d860-142">OUTPUTS</span></span>

### <span data-ttu-id="9d860-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d860-143">System.Boolean</span></span>

## <span data-ttu-id="9d860-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d860-144">NOTES</span></span>

<span data-ttu-id="9d860-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9d860-145">ALIASES</span></span>

<span data-ttu-id="9d860-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="9d860-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d860-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9d860-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d860-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9d860-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d860-149">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9d860-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d860-150">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9d860-151">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9d860-152">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9d860-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9d860-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d860-154">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="9d860-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9d860-155">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="9d860-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9d860-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d860-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9d860-157">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9d860-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="9d860-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="9d860-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9d860-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d860-159">RELATED LINKS</span></span>

