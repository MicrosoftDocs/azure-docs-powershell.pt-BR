---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: 87d04a30b5e04132f937d21b3585557efe71f4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891489"
---
# <span data-ttu-id="daabb-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="daabb-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="daabb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daabb-102">SYNOPSIS</span></span>
<span data-ttu-id="daabb-103">Exclui o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="daabb-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="daabb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="daabb-104">SYNTAX</span></span>

### <span data-ttu-id="daabb-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="daabb-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="daabb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="daabb-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="daabb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="daabb-107">DESCRIPTION</span></span>
<span data-ttu-id="daabb-108">Exclui o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="daabb-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="daabb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daabb-109">EXAMPLES</span></span>

### <span data-ttu-id="daabb-110">Exemplo 1: Remover um provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="daabb-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="daabb-111">Remover um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="daabb-111">Remove a custom provider</span></span>

### <span data-ttu-id="daabb-112">Exemplo 2: Remover um provedor personalizado com PassThru</span><span class="sxs-lookup"><span data-stu-id="daabb-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="daabb-113">Remova um provedor personalizado, usando o recurso PassThru para indicar sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="daabb-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="daabb-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="daabb-114">PARAMETERS</span></span>

### <span data-ttu-id="daabb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daabb-115">-AsJob</span></span>
<span data-ttu-id="daabb-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="daabb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="daabb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daabb-117">-DefaultProfile</span></span>
<span data-ttu-id="daabb-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daabb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daabb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daabb-119">-InputObject</span></span>
<span data-ttu-id="daabb-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="daabb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="daabb-121">-Name</span></span>
<span data-ttu-id="daabb-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="daabb-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="daabb-123">-NoWait</span></span>
<span data-ttu-id="daabb-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="daabb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="daabb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="daabb-125">-PassThru</span></span>
<span data-ttu-id="daabb-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="daabb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="daabb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daabb-127">-ResourceGroupName</span></span>
<span data-ttu-id="daabb-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daabb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="daabb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="daabb-129">-SubscriptionId</span></span>
<span data-ttu-id="daabb-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="daabb-130">The Azure subscription ID.</span></span>
<span data-ttu-id="daabb-131">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="daabb-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="daabb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daabb-132">-Confirm</span></span>
<span data-ttu-id="daabb-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daabb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daabb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daabb-134">-WhatIf</span></span>
<span data-ttu-id="daabb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daabb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daabb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daabb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daabb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daabb-137">CommonParameters</span></span>
<span data-ttu-id="daabb-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daabb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daabb-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daabb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daabb-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="daabb-140">INPUTS</span></span>

### <span data-ttu-id="daabb-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="daabb-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="daabb-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="daabb-142">OUTPUTS</span></span>

### <span data-ttu-id="daabb-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="daabb-143">System.Boolean</span></span>

## <span data-ttu-id="daabb-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="daabb-144">NOTES</span></span>

<span data-ttu-id="daabb-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="daabb-145">ALIASES</span></span>

<span data-ttu-id="daabb-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="daabb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="daabb-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="daabb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="daabb-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="daabb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="daabb-149">INPUTOBJECT <ICustomProvidersIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="daabb-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="daabb-150">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="daabb-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="daabb-151">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="daabb-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="daabb-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daabb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="daabb-153">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="daabb-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="daabb-154">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="daabb-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="daabb-155">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="daabb-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="daabb-156">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="daabb-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="daabb-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daabb-157">RELATED LINKS</span></span>

