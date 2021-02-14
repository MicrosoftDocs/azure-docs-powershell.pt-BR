---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110864"
---
# <span data-ttu-id="87f50-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="87f50-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="87f50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87f50-102">SYNOPSIS</span></span>
<span data-ttu-id="87f50-103">A operação Excluir Serviço de Domínio exclui um Serviço de Domínio existente.</span><span class="sxs-lookup"><span data-stu-id="87f50-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="87f50-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87f50-104">SYNTAX</span></span>

### <span data-ttu-id="87f50-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="87f50-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="87f50-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87f50-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87f50-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="87f50-107">DESCRIPTION</span></span>
<span data-ttu-id="87f50-108">A operação Excluir Serviço de Domínio exclui um Serviço de Domínio existente.</span><span class="sxs-lookup"><span data-stu-id="87f50-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="87f50-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87f50-109">EXAMPLES</span></span>

### <span data-ttu-id="87f50-110">Exemplo 1: Excluir o AzADDomain por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="87f50-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="87f50-111">Excluir o AzADDomain por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="87f50-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="87f50-112">Exemplo 2: Excluir o AzADDomain por InputObject</span><span class="sxs-lookup"><span data-stu-id="87f50-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="87f50-113">Excluir o AzADDomain por InputObject</span><span class="sxs-lookup"><span data-stu-id="87f50-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="87f50-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87f50-114">PARAMETERS</span></span>

### <span data-ttu-id="87f50-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87f50-115">-AsJob</span></span>
<span data-ttu-id="87f50-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="87f50-116">Run the command as a job</span></span>

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

### <span data-ttu-id="87f50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f50-117">-DefaultProfile</span></span>
<span data-ttu-id="87f50-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87f50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87f50-119">-InputObject</span></span>
<span data-ttu-id="87f50-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="87f50-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="87f50-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="87f50-121">-Name</span></span>
<span data-ttu-id="87f50-122">O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="87f50-122">The name of the domain service.</span></span>

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

### <span data-ttu-id="87f50-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87f50-123">-NoWait</span></span>
<span data-ttu-id="87f50-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="87f50-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87f50-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87f50-125">-PassThru</span></span>
<span data-ttu-id="87f50-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="87f50-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="87f50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f50-127">-ResourceGroupName</span></span>
<span data-ttu-id="87f50-128">O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="87f50-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="87f50-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="87f50-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="87f50-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87f50-130">-SubscriptionId</span></span>
<span data-ttu-id="87f50-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="87f50-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="87f50-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="87f50-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="87f50-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="87f50-133">-Confirm</span></span>
<span data-ttu-id="87f50-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87f50-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87f50-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87f50-135">-WhatIf</span></span>
<span data-ttu-id="87f50-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="87f50-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87f50-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87f50-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87f50-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f50-138">CommonParameters</span></span>
<span data-ttu-id="87f50-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f50-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f50-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87f50-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f50-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="87f50-141">INPUTS</span></span>

### <span data-ttu-id="87f50-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="87f50-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="87f50-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="87f50-143">OUTPUTS</span></span>

### <span data-ttu-id="87f50-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87f50-144">System.Boolean</span></span>

## <span data-ttu-id="87f50-145">Notas</span><span class="sxs-lookup"><span data-stu-id="87f50-145">NOTES</span></span>

<span data-ttu-id="87f50-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="87f50-146">ALIASES</span></span>

<span data-ttu-id="87f50-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="87f50-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87f50-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="87f50-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87f50-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87f50-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87f50-150">INPUTOBJECT: <IAdDomainServicesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="87f50-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87f50-151">`[DomainServiceName <String>]`: o nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="87f50-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="87f50-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="87f50-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87f50-153">`[ResourceGroupName <String>]`: o nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="87f50-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="87f50-154">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="87f50-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="87f50-155">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="87f50-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="87f50-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="87f50-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="87f50-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87f50-157">RELATED LINKS</span></span>

