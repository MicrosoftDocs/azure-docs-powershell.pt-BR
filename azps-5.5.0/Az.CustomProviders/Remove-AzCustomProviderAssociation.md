---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115879"
---
# <span data-ttu-id="45656-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="45656-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="45656-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45656-102">SYNOPSIS</span></span>
<span data-ttu-id="45656-103">Excluir uma associação.</span><span class="sxs-lookup"><span data-stu-id="45656-103">Delete an association.</span></span>

## <span data-ttu-id="45656-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45656-104">SYNTAX</span></span>

### <span data-ttu-id="45656-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="45656-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45656-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45656-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45656-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="45656-107">DESCRIPTION</span></span>
<span data-ttu-id="45656-108">Excluir uma associação.</span><span class="sxs-lookup"><span data-stu-id="45656-108">Delete an association.</span></span>

## <span data-ttu-id="45656-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45656-109">EXAMPLES</span></span>

### <span data-ttu-id="45656-110">Exemplo 1: Remover uma associação de provedores personalizados.</span><span class="sxs-lookup"><span data-stu-id="45656-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="45656-111">Remover uma associação de provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="45656-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="45656-112">Exemplo 2: Remover uma associação de provedor personalizado com a Piping</span><span class="sxs-lookup"><span data-stu-id="45656-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="45656-113">Remova uma associação de provedores personalizados, usando a piping e o recurso PassThru para indicar sucesso ou fracasso.</span><span class="sxs-lookup"><span data-stu-id="45656-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="45656-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45656-114">PARAMETERS</span></span>

### <span data-ttu-id="45656-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45656-115">-AsJob</span></span>
<span data-ttu-id="45656-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="45656-116">Run the command as a job</span></span>

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

### <span data-ttu-id="45656-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45656-117">-DefaultProfile</span></span>
<span data-ttu-id="45656-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45656-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45656-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45656-119">-InputObject</span></span>
<span data-ttu-id="45656-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="45656-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45656-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="45656-121">-Name</span></span>
<span data-ttu-id="45656-122">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="45656-122">The name of the association.</span></span>

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

### <span data-ttu-id="45656-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="45656-123">-NoWait</span></span>
<span data-ttu-id="45656-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="45656-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45656-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45656-125">-PassThru</span></span>
<span data-ttu-id="45656-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="45656-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45656-127">-Escopo</span><span class="sxs-lookup"><span data-stu-id="45656-127">-Scope</span></span>
<span data-ttu-id="45656-128">O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="45656-128">The scope of the association.</span></span>

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

### <span data-ttu-id="45656-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="45656-129">-Confirm</span></span>
<span data-ttu-id="45656-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45656-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45656-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45656-131">-WhatIf</span></span>
<span data-ttu-id="45656-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="45656-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45656-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45656-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45656-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45656-134">CommonParameters</span></span>
<span data-ttu-id="45656-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45656-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45656-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45656-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45656-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="45656-137">INPUTS</span></span>

### <span data-ttu-id="45656-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="45656-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="45656-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="45656-139">OUTPUTS</span></span>

### <span data-ttu-id="45656-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45656-140">System.Boolean</span></span>

## <span data-ttu-id="45656-141">Notas</span><span class="sxs-lookup"><span data-stu-id="45656-141">NOTES</span></span>

<span data-ttu-id="45656-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="45656-142">ALIASES</span></span>

<span data-ttu-id="45656-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="45656-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45656-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="45656-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45656-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45656-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45656-146">INPUTOBJECT: <ICustomProvidersIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="45656-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45656-147">`[AssociationName <String>]`: o nome da associação.</span><span class="sxs-lookup"><span data-stu-id="45656-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="45656-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="45656-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45656-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45656-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="45656-150">`[ResourceProviderName <String>]`: o nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="45656-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="45656-151">`[Scope <String>]`: o escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="45656-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="45656-152">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="45656-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="45656-153">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="45656-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="45656-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45656-154">RELATED LINKS</span></span>

