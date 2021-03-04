---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
ms.openlocfilehash: 5004aa694dd0ebb90239e2fb77259df9e84c59f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890650"
---
# <span data-ttu-id="b1119-101">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="b1119-101">Remove-AzCloudService</span></span>

## <span data-ttu-id="b1119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1119-102">SYNOPSIS</span></span>
<span data-ttu-id="b1119-103">Exclui um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b1119-103">Deletes a cloud service.</span></span>

## <span data-ttu-id="b1119-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b1119-104">SYNTAX</span></span>

### <span data-ttu-id="b1119-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1119-105">Delete (Default)</span></span>
```
Remove-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1119-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1119-106">DeleteViaIdentity</span></span>
```
Remove-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1119-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b1119-107">DESCRIPTION</span></span>
<span data-ttu-id="b1119-108">Exclui um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b1119-108">Deletes a cloud service.</span></span>

## <span data-ttu-id="b1119-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1119-109">EXAMPLES</span></span>

### <span data-ttu-id="b1119-110">Exemplo 1: Remover um serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="b1119-110">Example 1: Remove a cloud service</span></span>
```powershell
PS C:\> Remove-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="b1119-111">Este comando remove o serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b1119-111">This command removes the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b1119-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b1119-112">PARAMETERS</span></span>

### <span data-ttu-id="b1119-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1119-113">-AsJob</span></span>
<span data-ttu-id="b1119-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b1119-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b1119-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1119-115">-DefaultProfile</span></span>
<span data-ttu-id="b1119-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1119-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1119-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1119-117">-InputObject</span></span>
<span data-ttu-id="b1119-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b1119-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1119-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b1119-119">-Name</span></span>
<span data-ttu-id="b1119-120">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b1119-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1119-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1119-121">-NoWait</span></span>
<span data-ttu-id="b1119-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b1119-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b1119-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1119-123">-PassThru</span></span>
<span data-ttu-id="b1119-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b1119-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b1119-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1119-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1119-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1119-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="b1119-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1119-127">-SubscriptionId</span></span>
<span data-ttu-id="b1119-128">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b1119-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1119-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b1119-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b1119-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1119-130">-Confirm</span></span>
<span data-ttu-id="b1119-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1119-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1119-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1119-132">-WhatIf</span></span>
<span data-ttu-id="b1119-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1119-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1119-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1119-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1119-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1119-135">CommonParameters</span></span>
<span data-ttu-id="b1119-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1119-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1119-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1119-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1119-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1119-138">INPUTS</span></span>

### <span data-ttu-id="b1119-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b1119-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b1119-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b1119-140">OUTPUTS</span></span>

### <span data-ttu-id="b1119-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1119-141">System.Boolean</span></span>

## <span data-ttu-id="b1119-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="b1119-142">NOTES</span></span>

<span data-ttu-id="b1119-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b1119-143">ALIASES</span></span>

<span data-ttu-id="b1119-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b1119-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1119-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b1119-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1119-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1119-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1119-147">INPUTOBJECT <ICloudServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b1119-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1119-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b1119-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b1119-149">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b1119-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1119-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b1119-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b1119-151">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="b1119-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b1119-152">`[RoleName <String>]`: Nome da função.</span><span class="sxs-lookup"><span data-stu-id="b1119-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b1119-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b1119-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b1119-154">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b1119-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b1119-155">`[UpdateDomain <Int32?>]`: Especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="b1119-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b1119-156">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b1119-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b1119-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1119-157">RELATED LINKS</span></span>

