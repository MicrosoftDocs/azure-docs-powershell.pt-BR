---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8d1918599832f5740515dc6334192bf9b4cc54ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887277"
---
# <span data-ttu-id="113ce-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="113ce-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="113ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="113ce-102">SYNOPSIS</span></span>
<span data-ttu-id="113ce-103">Excluir uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-103">Delete a private cloud</span></span>

## <span data-ttu-id="113ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="113ce-104">SYNTAX</span></span>

### <span data-ttu-id="113ce-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="113ce-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="113ce-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="113ce-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="113ce-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="113ce-107">DESCRIPTION</span></span>
<span data-ttu-id="113ce-108">Excluir uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-108">Delete a private cloud</span></span>

## <span data-ttu-id="113ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="113ce-109">EXAMPLES</span></span>

### <span data-ttu-id="113ce-110">Exemplo 1: Excluir nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="113ce-111">Excluir nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-111">Delete private cloud</span></span>

## <span data-ttu-id="113ce-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="113ce-112">PARAMETERS</span></span>

### <span data-ttu-id="113ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="113ce-113">-AsJob</span></span>
<span data-ttu-id="113ce-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="113ce-114">Run the command as a job</span></span>

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

### <span data-ttu-id="113ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113ce-115">-DefaultProfile</span></span>
<span data-ttu-id="113ce-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="113ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="113ce-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="113ce-117">-InputObject</span></span>
<span data-ttu-id="113ce-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="113ce-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="113ce-119">-Name</span><span class="sxs-lookup"><span data-stu-id="113ce-119">-Name</span></span>
<span data-ttu-id="113ce-120">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113ce-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="113ce-121">-NoWait</span></span>
<span data-ttu-id="113ce-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="113ce-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="113ce-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="113ce-123">-PassThru</span></span>
<span data-ttu-id="113ce-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="113ce-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="113ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="113ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="113ce-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="113ce-126">The name of the resource group.</span></span>
<span data-ttu-id="113ce-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="113ce-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="113ce-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="113ce-128">-SubscriptionId</span></span>
<span data-ttu-id="113ce-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="113ce-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="113ce-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="113ce-130">-Confirm</span></span>
<span data-ttu-id="113ce-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="113ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="113ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="113ce-132">-WhatIf</span></span>
<span data-ttu-id="113ce-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="113ce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="113ce-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="113ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="113ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113ce-135">CommonParameters</span></span>
<span data-ttu-id="113ce-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="113ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113ce-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="113ce-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113ce-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="113ce-138">INPUTS</span></span>

### <span data-ttu-id="113ce-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="113ce-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="113ce-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="113ce-140">OUTPUTS</span></span>

### <span data-ttu-id="113ce-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="113ce-141">System.Boolean</span></span>

## <span data-ttu-id="113ce-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="113ce-142">NOTES</span></span>

<span data-ttu-id="113ce-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="113ce-143">ALIASES</span></span>

<span data-ttu-id="113ce-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="113ce-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="113ce-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="113ce-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="113ce-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="113ce-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="113ce-147">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="113ce-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="113ce-148">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="113ce-149">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="113ce-150">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="113ce-151">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="113ce-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="113ce-152">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="113ce-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="113ce-153">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="113ce-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="113ce-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="113ce-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="113ce-155">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="113ce-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="113ce-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="113ce-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="113ce-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="113ce-157">RELATED LINKS</span></span>

