---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: 68631f106b795f42fa8ead1a6379ff9dbaa0f4ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889358"
---
# <span data-ttu-id="c97cd-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="c97cd-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="c97cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c97cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c97cd-103">A operação Excluir Serviço de Domínio exclui um Serviço de Domínio existente.</span><span class="sxs-lookup"><span data-stu-id="c97cd-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="c97cd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c97cd-104">SYNTAX</span></span>

### <span data-ttu-id="c97cd-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c97cd-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c97cd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c97cd-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c97cd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c97cd-107">DESCRIPTION</span></span>
<span data-ttu-id="c97cd-108">A operação Excluir Serviço de Domínio exclui um Serviço de Domínio existente.</span><span class="sxs-lookup"><span data-stu-id="c97cd-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="c97cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c97cd-109">EXAMPLES</span></span>

### <span data-ttu-id="c97cd-110">Exemplo 1: Excluir o AzADDomain por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="c97cd-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="c97cd-111">Excluir o AzADDomain por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="c97cd-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="c97cd-112">Exemplo 2: Excluir o AzADDomain por InputObject</span><span class="sxs-lookup"><span data-stu-id="c97cd-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="c97cd-113">Excluir o AzADDomain por InputObject</span><span class="sxs-lookup"><span data-stu-id="c97cd-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="c97cd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c97cd-114">PARAMETERS</span></span>

### <span data-ttu-id="c97cd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c97cd-115">-AsJob</span></span>
<span data-ttu-id="c97cd-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c97cd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c97cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97cd-117">-DefaultProfile</span></span>
<span data-ttu-id="c97cd-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c97cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c97cd-119">-InputObject</span></span>
<span data-ttu-id="c97cd-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c97cd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c97cd-121">-Name</span></span>
<span data-ttu-id="c97cd-122">O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="c97cd-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c97cd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c97cd-123">-NoWait</span></span>
<span data-ttu-id="c97cd-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c97cd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c97cd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c97cd-125">-PassThru</span></span>
<span data-ttu-id="c97cd-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c97cd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c97cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="c97cd-128">O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="c97cd-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="c97cd-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c97cd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c97cd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c97cd-130">-SubscriptionId</span></span>
<span data-ttu-id="c97cd-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c97cd-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c97cd-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c97cd-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c97cd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c97cd-133">-Confirm</span></span>
<span data-ttu-id="c97cd-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c97cd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97cd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97cd-135">-WhatIf</span></span>
<span data-ttu-id="c97cd-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c97cd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97cd-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c97cd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97cd-138">CommonParameters</span></span>
<span data-ttu-id="c97cd-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97cd-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c97cd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97cd-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c97cd-141">INPUTS</span></span>

### <span data-ttu-id="c97cd-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="c97cd-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="c97cd-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c97cd-143">OUTPUTS</span></span>

### <span data-ttu-id="c97cd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c97cd-144">System.Boolean</span></span>

## <span data-ttu-id="c97cd-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="c97cd-145">NOTES</span></span>

<span data-ttu-id="c97cd-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c97cd-146">ALIASES</span></span>

<span data-ttu-id="c97cd-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="c97cd-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c97cd-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c97cd-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c97cd-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c97cd-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c97cd-150">INPUTOBJECT <IAdDomainServicesIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="c97cd-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c97cd-151">`[DomainServiceName <String>]`: O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="c97cd-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="c97cd-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c97cd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c97cd-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="c97cd-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="c97cd-154">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c97cd-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="c97cd-155">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c97cd-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c97cd-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c97cd-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c97cd-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c97cd-157">RELATED LINKS</span></span>

