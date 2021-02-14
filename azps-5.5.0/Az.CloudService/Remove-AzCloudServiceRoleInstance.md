---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 8d44cc541cf44e03e2946ce428eb96c2f902bf84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115496"
---
# <span data-ttu-id="aba98-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="aba98-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="aba98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aba98-102">SYNOPSIS</span></span>
<span data-ttu-id="aba98-103">Exclui instâncias de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aba98-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="aba98-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aba98-104">SYNTAX</span></span>

### <span data-ttu-id="aba98-105">DeleteExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aba98-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aba98-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aba98-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aba98-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aba98-107">DESCRIPTION</span></span>
<span data-ttu-id="aba98-108">Exclui instâncias de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aba98-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="aba98-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aba98-109">EXAMPLES</span></span>

### <span data-ttu-id="aba98-110">Exemplo 1: Remover uma instância de função de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="aba98-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="aba98-111">Esse comando remove a instância de função chamada ContosoFrontEnd_IN_0 do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="aba98-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="aba98-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aba98-112">PARAMETERS</span></span>

### <span data-ttu-id="aba98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aba98-113">-AsJob</span></span>
<span data-ttu-id="aba98-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="aba98-114">Run the command as a job</span></span>

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

### <span data-ttu-id="aba98-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="aba98-115">-CloudServiceName</span></span>
<span data-ttu-id="aba98-116">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aba98-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba98-117">-DefaultProfile</span></span>
<span data-ttu-id="aba98-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aba98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aba98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aba98-119">-InputObject</span></span>
<span data-ttu-id="aba98-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="aba98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aba98-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aba98-121">-NoWait</span></span>
<span data-ttu-id="aba98-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="aba98-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aba98-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aba98-123">-PassThru</span></span>
<span data-ttu-id="aba98-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="aba98-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aba98-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba98-125">-ResourceGroupName</span></span>
<span data-ttu-id="aba98-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aba98-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba98-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="aba98-127">-RoleInstance</span></span>
<span data-ttu-id="aba98-128">Lista de nomes de instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aba98-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="aba98-129">O valor de '\*' significa todas as instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aba98-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba98-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aba98-130">-SubscriptionId</span></span>
<span data-ttu-id="aba98-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aba98-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aba98-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aba98-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba98-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aba98-133">-Confirm</span></span>
<span data-ttu-id="aba98-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aba98-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba98-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba98-135">-WhatIf</span></span>
<span data-ttu-id="aba98-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aba98-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba98-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aba98-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba98-138">CommonParameters</span></span>
<span data-ttu-id="aba98-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba98-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aba98-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba98-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="aba98-141">INPUTS</span></span>

### <span data-ttu-id="aba98-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="aba98-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="aba98-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="aba98-143">OUTPUTS</span></span>

### <span data-ttu-id="aba98-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aba98-144">System.Boolean</span></span>

## <span data-ttu-id="aba98-145">Notas</span><span class="sxs-lookup"><span data-stu-id="aba98-145">NOTES</span></span>

<span data-ttu-id="aba98-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="aba98-146">ALIASES</span></span>

<span data-ttu-id="aba98-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="aba98-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aba98-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="aba98-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aba98-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aba98-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aba98-150">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="aba98-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aba98-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aba98-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="aba98-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aba98-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aba98-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aba98-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="aba98-154">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="aba98-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="aba98-155">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="aba98-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="aba98-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aba98-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aba98-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aba98-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aba98-158">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="aba98-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="aba98-159">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="aba98-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="aba98-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aba98-160">RELATED LINKS</span></span>

