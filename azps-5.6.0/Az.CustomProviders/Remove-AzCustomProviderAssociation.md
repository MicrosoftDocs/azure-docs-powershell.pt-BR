---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 6d3a6863044722be49efb78a71e3e0fbe82db5e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891487"
---
# <span data-ttu-id="3c418-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="3c418-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="3c418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c418-102">SYNOPSIS</span></span>
<span data-ttu-id="3c418-103">Excluir uma associação.</span><span class="sxs-lookup"><span data-stu-id="3c418-103">Delete an association.</span></span>

## <span data-ttu-id="3c418-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c418-104">SYNTAX</span></span>

### <span data-ttu-id="3c418-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c418-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c418-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c418-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c418-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c418-107">DESCRIPTION</span></span>
<span data-ttu-id="3c418-108">Excluir uma associação.</span><span class="sxs-lookup"><span data-stu-id="3c418-108">Delete an association.</span></span>

## <span data-ttu-id="3c418-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c418-109">EXAMPLES</span></span>

### <span data-ttu-id="3c418-110">Exemplo 1: Remover uma associação de provedor personalizada.</span><span class="sxs-lookup"><span data-stu-id="3c418-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="3c418-111">Remova uma associação de provedor personalizada.</span><span class="sxs-lookup"><span data-stu-id="3c418-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="3c418-112">Exemplo 2: Remover uma associação de provedor personalizada com o Piping</span><span class="sxs-lookup"><span data-stu-id="3c418-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="3c418-113">Remova uma associação de provedor personalizada, usando a canalização e o recurso PassThru para indicar sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="3c418-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="3c418-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c418-114">PARAMETERS</span></span>

### <span data-ttu-id="3c418-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c418-115">-AsJob</span></span>
<span data-ttu-id="3c418-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3c418-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3c418-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c418-117">-DefaultProfile</span></span>
<span data-ttu-id="3c418-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c418-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c418-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c418-119">-InputObject</span></span>
<span data-ttu-id="3c418-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3c418-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c418-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c418-121">-Name</span></span>
<span data-ttu-id="3c418-122">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="3c418-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c418-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c418-123">-NoWait</span></span>
<span data-ttu-id="3c418-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3c418-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c418-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c418-125">-PassThru</span></span>
<span data-ttu-id="3c418-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3c418-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c418-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="3c418-127">-Scope</span></span>
<span data-ttu-id="3c418-128">O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="3c418-128">The scope of the association.</span></span>

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

### <span data-ttu-id="3c418-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c418-129">-Confirm</span></span>
<span data-ttu-id="3c418-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c418-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c418-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c418-131">-WhatIf</span></span>
<span data-ttu-id="3c418-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c418-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c418-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c418-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c418-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c418-134">CommonParameters</span></span>
<span data-ttu-id="3c418-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c418-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c418-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c418-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c418-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c418-137">INPUTS</span></span>

### <span data-ttu-id="3c418-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="3c418-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="3c418-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c418-139">OUTPUTS</span></span>

### <span data-ttu-id="3c418-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c418-140">System.Boolean</span></span>

## <span data-ttu-id="3c418-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c418-141">NOTES</span></span>

<span data-ttu-id="3c418-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3c418-142">ALIASES</span></span>

<span data-ttu-id="3c418-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="3c418-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c418-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3c418-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c418-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c418-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c418-146">INPUTOBJECT <ICustomProvidersIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="3c418-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c418-147">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="3c418-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="3c418-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3c418-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c418-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c418-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3c418-150">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c418-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="3c418-151">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="3c418-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="3c418-152">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c418-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="3c418-153">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="3c418-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="3c418-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c418-154">RELATED LINKS</span></span>

