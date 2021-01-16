---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257835"
---
# <span data-ttu-id="44567-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="44567-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="44567-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44567-102">SYNOPSIS</span></span>
<span data-ttu-id="44567-103">Excluir uma associação.</span><span class="sxs-lookup"><span data-stu-id="44567-103">Delete an association.</span></span>

## <span data-ttu-id="44567-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44567-104">SYNTAX</span></span>

### <span data-ttu-id="44567-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="44567-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44567-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44567-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44567-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44567-107">DESCRIPTION</span></span>
<span data-ttu-id="44567-108">Excluir uma associação.</span><span class="sxs-lookup"><span data-stu-id="44567-108">Delete an association.</span></span>

## <span data-ttu-id="44567-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44567-109">EXAMPLES</span></span>

### <span data-ttu-id="44567-110">Exemplo 1: remover uma associação de provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="44567-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="44567-111">Remova uma associação de provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="44567-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="44567-112">Exemplo 2: remover uma associação de provedor personalizado com tubulação</span><span class="sxs-lookup"><span data-stu-id="44567-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="44567-113">Remova uma associação de provedor personalizado, usando o recurso de encanamento e o PassThru para indicar êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="44567-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="44567-114">OS</span><span class="sxs-lookup"><span data-stu-id="44567-114">PARAMETERS</span></span>

### <span data-ttu-id="44567-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44567-115">-AsJob</span></span>
<span data-ttu-id="44567-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="44567-116">Run the command as a job</span></span>

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

### <span data-ttu-id="44567-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44567-117">-DefaultProfile</span></span>
<span data-ttu-id="44567-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44567-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44567-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44567-119">-InputObject</span></span>
<span data-ttu-id="44567-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="44567-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="44567-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="44567-121">-Name</span></span>
<span data-ttu-id="44567-122">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="44567-122">The name of the association.</span></span>

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

### <span data-ttu-id="44567-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="44567-123">-NoWait</span></span>
<span data-ttu-id="44567-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="44567-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44567-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44567-125">-PassThru</span></span>
<span data-ttu-id="44567-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="44567-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44567-127">-Escopo</span><span class="sxs-lookup"><span data-stu-id="44567-127">-Scope</span></span>
<span data-ttu-id="44567-128">O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="44567-128">The scope of the association.</span></span>

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

### <span data-ttu-id="44567-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44567-129">-Confirm</span></span>
<span data-ttu-id="44567-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44567-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44567-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44567-131">-WhatIf</span></span>
<span data-ttu-id="44567-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44567-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44567-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44567-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44567-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44567-134">CommonParameters</span></span>
<span data-ttu-id="44567-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44567-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44567-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44567-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44567-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44567-137">INPUTS</span></span>

### <span data-ttu-id="44567-138">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="44567-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="44567-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44567-139">OUTPUTS</span></span>

### <span data-ttu-id="44567-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44567-140">System.Boolean</span></span>

## <span data-ttu-id="44567-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44567-141">NOTES</span></span>

<span data-ttu-id="44567-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="44567-142">ALIASES</span></span>

<span data-ttu-id="44567-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="44567-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44567-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="44567-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44567-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44567-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44567-146">INPUTobject <ICustomProvidersIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="44567-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44567-147">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="44567-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="44567-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="44567-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44567-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44567-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="44567-150">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="44567-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="44567-151">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="44567-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="44567-152">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="44567-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="44567-153">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="44567-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="44567-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44567-154">RELATED LINKS</span></span>

