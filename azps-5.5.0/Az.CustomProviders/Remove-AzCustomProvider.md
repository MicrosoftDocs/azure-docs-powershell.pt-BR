---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112004"
---
# <span data-ttu-id="c41f6-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="c41f6-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="c41f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c41f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c41f6-103">Exclui o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c41f6-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="c41f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c41f6-104">SYNTAX</span></span>

### <span data-ttu-id="c41f6-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c41f6-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c41f6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c41f6-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c41f6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c41f6-107">DESCRIPTION</span></span>
<span data-ttu-id="c41f6-108">Exclui o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c41f6-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="c41f6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c41f6-109">EXAMPLES</span></span>

### <span data-ttu-id="c41f6-110">Exemplo 1: Remover um provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="c41f6-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="c41f6-111">Remover um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="c41f6-111">Remove a custom provider</span></span>

### <span data-ttu-id="c41f6-112">Exemplo 2: Remover um provedor personalizado com PassThru</span><span class="sxs-lookup"><span data-stu-id="c41f6-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="c41f6-113">Remova um provedor personalizado usando o recurso PassThru para indicar sucesso ou fracasso.</span><span class="sxs-lookup"><span data-stu-id="c41f6-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="c41f6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c41f6-114">PARAMETERS</span></span>

### <span data-ttu-id="c41f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c41f6-115">-AsJob</span></span>
<span data-ttu-id="c41f6-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c41f6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c41f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41f6-117">-DefaultProfile</span></span>
<span data-ttu-id="c41f6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c41f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c41f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c41f6-119">-InputObject</span></span>
<span data-ttu-id="c41f6-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c41f6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c41f6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c41f6-121">-Name</span></span>
<span data-ttu-id="c41f6-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="c41f6-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="c41f6-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c41f6-123">-NoWait</span></span>
<span data-ttu-id="c41f6-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="c41f6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c41f6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c41f6-125">-PassThru</span></span>
<span data-ttu-id="c41f6-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c41f6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c41f6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41f6-127">-ResourceGroupName</span></span>
<span data-ttu-id="c41f6-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c41f6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c41f6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c41f6-129">-SubscriptionId</span></span>
<span data-ttu-id="c41f6-130">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c41f6-130">The Azure subscription ID.</span></span>
<span data-ttu-id="c41f6-131">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c41f6-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c41f6-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c41f6-132">-Confirm</span></span>
<span data-ttu-id="c41f6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c41f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41f6-134">-WhatIf</span></span>
<span data-ttu-id="c41f6-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c41f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c41f6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c41f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41f6-137">CommonParameters</span></span>
<span data-ttu-id="c41f6-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41f6-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c41f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41f6-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="c41f6-140">INPUTS</span></span>

### <span data-ttu-id="c41f6-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="c41f6-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="c41f6-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="c41f6-142">OUTPUTS</span></span>

### <span data-ttu-id="c41f6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c41f6-143">System.Boolean</span></span>

## <span data-ttu-id="c41f6-144">Notas</span><span class="sxs-lookup"><span data-stu-id="c41f6-144">NOTES</span></span>

<span data-ttu-id="c41f6-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="c41f6-145">ALIASES</span></span>

<span data-ttu-id="c41f6-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="c41f6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c41f6-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c41f6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c41f6-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c41f6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c41f6-149">INPUTOBJECT: <ICustomProvidersIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="c41f6-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c41f6-150">`[AssociationName <String>]`: o nome da associação.</span><span class="sxs-lookup"><span data-stu-id="c41f6-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="c41f6-151">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c41f6-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c41f6-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c41f6-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c41f6-153">`[ResourceProviderName <String>]`: o nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="c41f6-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="c41f6-154">`[Scope <String>]`: o escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="c41f6-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="c41f6-155">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c41f6-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c41f6-156">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c41f6-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c41f6-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c41f6-157">RELATED LINKS</span></span>

