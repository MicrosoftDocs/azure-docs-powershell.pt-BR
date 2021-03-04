---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 5a29444c5f6d05ddbf614e86cd13af6818d24d79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885943"
---
# <span data-ttu-id="6dbe4-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="6dbe4-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="6dbe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="6dbe4-103">Exclui instâncias de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="6dbe4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6dbe4-104">SYNTAX</span></span>

### <span data-ttu-id="6dbe4-105">DeleteExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6dbe4-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6dbe4-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6dbe4-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6dbe4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6dbe4-107">DESCRIPTION</span></span>
<span data-ttu-id="6dbe4-108">Exclui instâncias de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="6dbe4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6dbe4-109">EXAMPLES</span></span>

### <span data-ttu-id="6dbe4-110">Exemplo 1: Remover uma instância de função de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="6dbe4-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="6dbe4-111">Este comando remove a instância de função chamada ContosoFrontEnd_IN_0 do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6dbe4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6dbe4-112">PARAMETERS</span></span>

### <span data-ttu-id="6dbe4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dbe4-113">-AsJob</span></span>
<span data-ttu-id="6dbe4-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6dbe4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6dbe4-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6dbe4-115">-CloudServiceName</span></span>
<span data-ttu-id="6dbe4-116">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-116">Name of the cloud service.</span></span>

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

### <span data-ttu-id="6dbe4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dbe4-117">-DefaultProfile</span></span>
<span data-ttu-id="6dbe4-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dbe4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dbe4-119">-InputObject</span></span>
<span data-ttu-id="6dbe4-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6dbe4-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6dbe4-121">-NoWait</span></span>
<span data-ttu-id="6dbe4-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6dbe4-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6dbe4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dbe4-123">-PassThru</span></span>
<span data-ttu-id="6dbe4-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6dbe4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6dbe4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dbe4-125">-ResourceGroupName</span></span>
<span data-ttu-id="6dbe4-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="6dbe4-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="6dbe4-127">-RoleInstance</span></span>
<span data-ttu-id="6dbe4-128">Lista de nomes de instâncias de função de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="6dbe4-129">O valor de '\*' significa todas as instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="6dbe4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dbe4-130">-SubscriptionId</span></span>
<span data-ttu-id="6dbe4-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6dbe4-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6dbe4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dbe4-133">-Confirm</span></span>
<span data-ttu-id="6dbe4-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dbe4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dbe4-135">-WhatIf</span></span>
<span data-ttu-id="6dbe4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dbe4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dbe4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dbe4-138">CommonParameters</span></span>
<span data-ttu-id="6dbe4-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dbe4-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dbe4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dbe4-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dbe4-141">INPUTS</span></span>

### <span data-ttu-id="6dbe4-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6dbe4-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="6dbe4-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6dbe4-143">OUTPUTS</span></span>

### <span data-ttu-id="6dbe4-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6dbe4-144">System.Boolean</span></span>

## <span data-ttu-id="6dbe4-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="6dbe4-145">NOTES</span></span>

<span data-ttu-id="6dbe4-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6dbe4-146">ALIASES</span></span>

<span data-ttu-id="6dbe4-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6dbe4-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6dbe4-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6dbe4-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6dbe4-150">INPUTOBJECT <ICloudServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="6dbe4-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6dbe4-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6dbe4-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="6dbe4-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6dbe4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6dbe4-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6dbe4-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="6dbe4-154">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="6dbe4-155">`[RoleName <String>]`: Nome da função.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="6dbe4-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6dbe4-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6dbe4-158">`[UpdateDomain <Int32?>]`: Especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="6dbe4-159">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6dbe4-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="6dbe4-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dbe4-160">RELATED LINKS</span></span>

