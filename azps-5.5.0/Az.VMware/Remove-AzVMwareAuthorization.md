---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
ms.openlocfilehash: 39a6f251cd0cfb190ea8541f5b04c35d710de2c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116029"
---
# <span data-ttu-id="a3be0-101">Remove-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="a3be0-101">Remove-AzVMwareAuthorization</span></span>

## <span data-ttu-id="a3be0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3be0-102">SYNOPSIS</span></span>
<span data-ttu-id="a3be0-103">Excluir uma Autorização de Circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="a3be0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3be0-104">SYNTAX</span></span>

### <span data-ttu-id="a3be0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3be0-105">Delete (Default)</span></span>
```
Remove-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a3be0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3be0-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3be0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3be0-107">DESCRIPTION</span></span>
<span data-ttu-id="a3be0-108">Excluir uma Autorização de Circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="a3be0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3be0-109">EXAMPLES</span></span>

### <span data-ttu-id="a3be0-110">Exemplo 1: Excluir autorização para nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="a3be0-111">Excluir autorização para nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="a3be0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3be0-112">PARAMETERS</span></span>

### <span data-ttu-id="a3be0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3be0-113">-AsJob</span></span>
<span data-ttu-id="a3be0-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a3be0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a3be0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3be0-115">-DefaultProfile</span></span>
<span data-ttu-id="a3be0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3be0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3be0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3be0-117">-InputObject</span></span>
<span data-ttu-id="a3be0-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a3be0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3be0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3be0-119">-Name</span></span>
<span data-ttu-id="a3be0-120">Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="a3be0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a3be0-121">-NoWait</span></span>
<span data-ttu-id="a3be0-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="a3be0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a3be0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3be0-123">-PassThru</span></span>
<span data-ttu-id="a3be0-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a3be0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a3be0-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="a3be0-125">-PrivateCloudName</span></span>
<span data-ttu-id="a3be0-126">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="a3be0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3be0-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3be0-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3be0-128">The name of the resource group.</span></span>
<span data-ttu-id="a3be0-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3be0-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a3be0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3be0-130">-SubscriptionId</span></span>
<span data-ttu-id="a3be0-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a3be0-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a3be0-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a3be0-132">-Confirm</span></span>
<span data-ttu-id="a3be0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3be0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3be0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3be0-134">-WhatIf</span></span>
<span data-ttu-id="a3be0-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a3be0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3be0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3be0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3be0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3be0-137">CommonParameters</span></span>
<span data-ttu-id="a3be0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3be0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3be0-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3be0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3be0-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3be0-140">INPUTS</span></span>

### <span data-ttu-id="a3be0-141">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="a3be0-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="a3be0-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3be0-142">OUTPUTS</span></span>

### <span data-ttu-id="a3be0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3be0-143">System.Boolean</span></span>

## <span data-ttu-id="a3be0-144">Notas</span><span class="sxs-lookup"><span data-stu-id="a3be0-144">NOTES</span></span>

<span data-ttu-id="a3be0-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="a3be0-145">ALIASES</span></span>

<span data-ttu-id="a3be0-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a3be0-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3be0-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a3be0-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3be0-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3be0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3be0-149">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a3be0-149">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3be0-150">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="a3be0-151">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="a3be0-152">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="a3be0-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a3be0-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3be0-154">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="a3be0-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="a3be0-155">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a3be0-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="a3be0-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3be0-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a3be0-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3be0-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a3be0-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a3be0-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a3be0-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3be0-159">RELATED LINKS</span></span>

