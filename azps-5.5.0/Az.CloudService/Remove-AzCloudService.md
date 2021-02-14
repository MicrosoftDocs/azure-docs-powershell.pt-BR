---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
ms.openlocfilehash: 07d7747a16af8d61b8ddbf05030445e599bb7e33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116892"
---
# <span data-ttu-id="14d73-101">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="14d73-101">Remove-AzCloudService</span></span>

## <span data-ttu-id="14d73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14d73-102">SYNOPSIS</span></span>
<span data-ttu-id="14d73-103">Exclui um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="14d73-103">Deletes a cloud service.</span></span>

## <span data-ttu-id="14d73-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14d73-104">SYNTAX</span></span>

### <span data-ttu-id="14d73-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14d73-105">Delete (Default)</span></span>
```
Remove-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14d73-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14d73-106">DeleteViaIdentity</span></span>
```
Remove-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14d73-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="14d73-107">DESCRIPTION</span></span>
<span data-ttu-id="14d73-108">Exclui um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="14d73-108">Deletes a cloud service.</span></span>

## <span data-ttu-id="14d73-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14d73-109">EXAMPLES</span></span>

### <span data-ttu-id="14d73-110">Exemplo 1: Remover um serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="14d73-110">Example 1: Remove a cloud service</span></span>
```powershell
PS C:\> Remove-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="14d73-111">Esse comando remove o serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="14d73-111">This command removes the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="14d73-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14d73-112">PARAMETERS</span></span>

### <span data-ttu-id="14d73-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14d73-113">-AsJob</span></span>
<span data-ttu-id="14d73-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="14d73-114">Run the command as a job</span></span>

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

### <span data-ttu-id="14d73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d73-115">-DefaultProfile</span></span>
<span data-ttu-id="14d73-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14d73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d73-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14d73-117">-InputObject</span></span>
<span data-ttu-id="14d73-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="14d73-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14d73-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="14d73-119">-Name</span></span>
<span data-ttu-id="14d73-120">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="14d73-120">Name of the cloud service.</span></span>

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

### <span data-ttu-id="14d73-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="14d73-121">-NoWait</span></span>
<span data-ttu-id="14d73-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="14d73-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14d73-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14d73-123">-PassThru</span></span>
<span data-ttu-id="14d73-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="14d73-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="14d73-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d73-125">-ResourceGroupName</span></span>
<span data-ttu-id="14d73-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14d73-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="14d73-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14d73-127">-SubscriptionId</span></span>
<span data-ttu-id="14d73-128">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="14d73-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="14d73-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="14d73-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="14d73-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="14d73-130">-Confirm</span></span>
<span data-ttu-id="14d73-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d73-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d73-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d73-132">-WhatIf</span></span>
<span data-ttu-id="14d73-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="14d73-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14d73-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14d73-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d73-135">CommonParameters</span></span>
<span data-ttu-id="14d73-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d73-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14d73-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d73-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="14d73-138">INPUTS</span></span>

### <span data-ttu-id="14d73-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="14d73-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="14d73-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="14d73-140">OUTPUTS</span></span>

### <span data-ttu-id="14d73-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14d73-141">System.Boolean</span></span>

## <span data-ttu-id="14d73-142">Notas</span><span class="sxs-lookup"><span data-stu-id="14d73-142">NOTES</span></span>

<span data-ttu-id="14d73-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="14d73-143">ALIASES</span></span>

<span data-ttu-id="14d73-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="14d73-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14d73-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="14d73-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14d73-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14d73-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14d73-147">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="14d73-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14d73-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="14d73-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="14d73-149">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="14d73-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14d73-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="14d73-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="14d73-151">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="14d73-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="14d73-152">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="14d73-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="14d73-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="14d73-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="14d73-154">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="14d73-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="14d73-155">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="14d73-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="14d73-156">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="14d73-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="14d73-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14d73-157">RELATED LINKS</span></span>

