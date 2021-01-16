---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264427"
---
# <span data-ttu-id="3de02-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="3de02-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="3de02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3de02-102">SYNOPSIS</span></span>
<span data-ttu-id="3de02-103">Exclui o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de02-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="3de02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3de02-104">SYNTAX</span></span>

### <span data-ttu-id="3de02-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="3de02-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3de02-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3de02-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3de02-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3de02-107">DESCRIPTION</span></span>
<span data-ttu-id="3de02-108">Exclui o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de02-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="3de02-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3de02-109">EXAMPLES</span></span>

### <span data-ttu-id="3de02-110">Exemplo 1: remover um provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de02-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="3de02-111">Remover um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="3de02-111">Remove a custom provider</span></span>

### <span data-ttu-id="3de02-112">Exemplo 2: remover um provedor personalizado com PassThru</span><span class="sxs-lookup"><span data-stu-id="3de02-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="3de02-113">Remova um provedor personalizado, usando o recurso PassThru para indicar êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="3de02-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="3de02-114">OS</span><span class="sxs-lookup"><span data-stu-id="3de02-114">PARAMETERS</span></span>

### <span data-ttu-id="3de02-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3de02-115">-AsJob</span></span>
<span data-ttu-id="3de02-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3de02-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3de02-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de02-117">-DefaultProfile</span></span>
<span data-ttu-id="3de02-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3de02-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3de02-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3de02-119">-InputObject</span></span>
<span data-ttu-id="3de02-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3de02-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3de02-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3de02-121">-Name</span></span>
<span data-ttu-id="3de02-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de02-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="3de02-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3de02-123">-NoWait</span></span>
<span data-ttu-id="3de02-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3de02-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3de02-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3de02-125">-PassThru</span></span>
<span data-ttu-id="3de02-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3de02-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3de02-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de02-127">-ResourceGroupName</span></span>
<span data-ttu-id="3de02-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de02-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3de02-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3de02-129">-SubscriptionId</span></span>
<span data-ttu-id="3de02-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de02-130">The Azure subscription ID.</span></span>
<span data-ttu-id="3de02-131">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3de02-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="3de02-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3de02-132">-Confirm</span></span>
<span data-ttu-id="3de02-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de02-134">-WhatIf</span></span>
<span data-ttu-id="3de02-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3de02-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de02-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3de02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de02-137">CommonParameters</span></span>
<span data-ttu-id="3de02-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de02-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3de02-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de02-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3de02-140">INPUTS</span></span>

### <span data-ttu-id="3de02-141">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="3de02-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="3de02-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3de02-142">OUTPUTS</span></span>

### <span data-ttu-id="3de02-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3de02-143">System.Boolean</span></span>

## <span data-ttu-id="3de02-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3de02-144">NOTES</span></span>

<span data-ttu-id="3de02-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3de02-145">ALIASES</span></span>

<span data-ttu-id="3de02-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3de02-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3de02-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3de02-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3de02-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3de02-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3de02-149">INPUTobject <ICustomProvidersIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3de02-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3de02-150">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="3de02-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="3de02-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3de02-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3de02-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de02-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3de02-153">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de02-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="3de02-154">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="3de02-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="3de02-155">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de02-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="3de02-156">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3de02-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="3de02-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3de02-157">RELATED LINKS</span></span>

