---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 76ad6df6dbbd9b019e4c89fdbca55107264f0406
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118511"
---
# <span data-ttu-id="721fc-101">Remove-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="721fc-101">Remove-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="721fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="721fc-102">SYNOPSIS</span></span>
<span data-ttu-id="721fc-103">Excluir uma nuvem particular</span><span class="sxs-lookup"><span data-stu-id="721fc-103">Delete a private cloud</span></span>

## <span data-ttu-id="721fc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="721fc-104">SYNTAX</span></span>

### <span data-ttu-id="721fc-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="721fc-105">Delete (Default)</span></span>
```
Remove-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="721fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="721fc-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="721fc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="721fc-107">DESCRIPTION</span></span>
<span data-ttu-id="721fc-108">Excluir uma nuvem particular</span><span class="sxs-lookup"><span data-stu-id="721fc-108">Delete a private cloud</span></span>

## <span data-ttu-id="721fc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="721fc-109">EXAMPLES</span></span>

### <span data-ttu-id="721fc-110">Exemplo 1: Excluir nuvem privada</span><span class="sxs-lookup"><span data-stu-id="721fc-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="721fc-111">Excluir nuvem particular</span><span class="sxs-lookup"><span data-stu-id="721fc-111">Delete private cloud</span></span>

## <span data-ttu-id="721fc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="721fc-112">PARAMETERS</span></span>

### <span data-ttu-id="721fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="721fc-113">-AsJob</span></span>
<span data-ttu-id="721fc-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="721fc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="721fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721fc-115">-DefaultProfile</span></span>
<span data-ttu-id="721fc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="721fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="721fc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="721fc-117">-InputObject</span></span>
<span data-ttu-id="721fc-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="721fc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="721fc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="721fc-119">-Name</span></span>
<span data-ttu-id="721fc-120">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="721fc-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="721fc-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="721fc-121">-NoWait</span></span>
<span data-ttu-id="721fc-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="721fc-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="721fc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="721fc-123">-PassThru</span></span>
<span data-ttu-id="721fc-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="721fc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="721fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="721fc-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="721fc-126">The name of the resource group.</span></span>
<span data-ttu-id="721fc-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="721fc-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="721fc-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="721fc-128">-SubscriptionId</span></span>
<span data-ttu-id="721fc-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="721fc-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="721fc-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="721fc-130">-Confirm</span></span>
<span data-ttu-id="721fc-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="721fc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721fc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721fc-132">-WhatIf</span></span>
<span data-ttu-id="721fc-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="721fc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="721fc-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="721fc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721fc-135">CommonParameters</span></span>
<span data-ttu-id="721fc-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721fc-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="721fc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721fc-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="721fc-138">INPUTS</span></span>

### <span data-ttu-id="721fc-139">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="721fc-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="721fc-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="721fc-140">OUTPUTS</span></span>

### <span data-ttu-id="721fc-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="721fc-141">System.Boolean</span></span>

## <span data-ttu-id="721fc-142">Notas</span><span class="sxs-lookup"><span data-stu-id="721fc-142">NOTES</span></span>

<span data-ttu-id="721fc-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="721fc-143">ALIASES</span></span>

<span data-ttu-id="721fc-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="721fc-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="721fc-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="721fc-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="721fc-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="721fc-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="721fc-147">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="721fc-147">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="721fc-148">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="721fc-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="721fc-149">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="721fc-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="721fc-150">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="721fc-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="721fc-151">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="721fc-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="721fc-152">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="721fc-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="721fc-153">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="721fc-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="721fc-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="721fc-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="721fc-155">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="721fc-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="721fc-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="721fc-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="721fc-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="721fc-157">RELATED LINKS</span></span>

