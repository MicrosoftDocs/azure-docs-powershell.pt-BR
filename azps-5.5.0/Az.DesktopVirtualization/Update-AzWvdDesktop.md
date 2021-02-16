---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 31a9ecc324938ae3518887d58ac2a762b374328c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127014"
---
# <span data-ttu-id="09850-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="09850-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="09850-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09850-102">SYNOPSIS</span></span>
<span data-ttu-id="09850-103">Atualizar uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="09850-103">Update a desktop.</span></span>

## <span data-ttu-id="09850-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09850-104">SYNTAX</span></span>

### <span data-ttu-id="09850-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09850-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09850-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09850-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="09850-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="09850-107">DESCRIPTION</span></span>
<span data-ttu-id="09850-108">Atualizar uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="09850-108">Update a desktop.</span></span>

## <span data-ttu-id="09850-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09850-109">EXAMPLES</span></span>

### <span data-ttu-id="09850-110">Exemplo 1: Atualizar uma área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="09850-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="09850-111">Este comando atualiza uma Área de Trabalho Virtual do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="09850-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="09850-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09850-112">PARAMETERS</span></span>

### <span data-ttu-id="09850-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="09850-113">-ApplicationGroupName</span></span>
<span data-ttu-id="09850-114">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="09850-114">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09850-115">-DefaultProfile</span></span>
<span data-ttu-id="09850-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09850-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09850-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="09850-117">-Description</span></span>
<span data-ttu-id="09850-118">Descrição da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="09850-118">Description of Desktop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-119">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="09850-119">-FriendlyName</span></span>
<span data-ttu-id="09850-120">Nome amigável da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="09850-120">Friendly name of Desktop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09850-121">-InputObject</span></span>
<span data-ttu-id="09850-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="09850-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09850-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="09850-123">-Name</span></span>
<span data-ttu-id="09850-124">O nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="09850-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09850-125">-ResourceGroupName</span></span>
<span data-ttu-id="09850-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09850-126">The name of the resource group.</span></span>
<span data-ttu-id="09850-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="09850-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09850-128">-SubscriptionId</span></span>
<span data-ttu-id="09850-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="09850-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="09850-130">-Tag</span></span>
<span data-ttu-id="09850-131">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="09850-131">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="09850-132">-Confirm</span></span>
<span data-ttu-id="09850-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09850-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09850-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09850-134">-WhatIf</span></span>
<span data-ttu-id="09850-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="09850-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09850-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09850-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09850-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09850-137">CommonParameters</span></span>
<span data-ttu-id="09850-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09850-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09850-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09850-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09850-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="09850-140">INPUTS</span></span>

### <span data-ttu-id="09850-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="09850-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="09850-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="09850-142">OUTPUTS</span></span>

### <span data-ttu-id="09850-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="09850-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="09850-144">Notas</span><span class="sxs-lookup"><span data-stu-id="09850-144">NOTES</span></span>

<span data-ttu-id="09850-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="09850-145">ALIASES</span></span>

<span data-ttu-id="09850-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="09850-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09850-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="09850-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09850-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09850-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09850-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="09850-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09850-150">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="09850-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="09850-151">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="09850-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="09850-152">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="09850-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="09850-153">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="09850-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="09850-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="09850-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09850-155">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="09850-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="09850-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09850-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09850-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="09850-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="09850-158">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="09850-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="09850-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="09850-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09850-160">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="09850-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="09850-161">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="09850-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="09850-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09850-162">RELATED LINKS</span></span>

