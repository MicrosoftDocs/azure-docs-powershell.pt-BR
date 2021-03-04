---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: fbc61ec485be94eacb0267a9698a861f962c61a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891851"
---
# <span data-ttu-id="a111f-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="a111f-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="a111f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a111f-102">SYNOPSIS</span></span>
<span data-ttu-id="a111f-103">Atualize uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a111f-103">Update a desktop.</span></span>

## <span data-ttu-id="a111f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a111f-104">SYNTAX</span></span>

### <span data-ttu-id="a111f-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a111f-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a111f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a111f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a111f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a111f-107">DESCRIPTION</span></span>
<span data-ttu-id="a111f-108">Atualize uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a111f-108">Update a desktop.</span></span>

## <span data-ttu-id="a111f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a111f-109">EXAMPLES</span></span>

### <span data-ttu-id="a111f-110">Exemplo 1: atualizar uma área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="a111f-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="a111f-111">Este comando atualiza uma Área de Trabalho Virtual do Windows em um grupo de aplicações.</span><span class="sxs-lookup"><span data-stu-id="a111f-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="a111f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a111f-112">PARAMETERS</span></span>

### <span data-ttu-id="a111f-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="a111f-113">-ApplicationGroupName</span></span>
<span data-ttu-id="a111f-114">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a111f-114">The name of the application group</span></span>

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

### <span data-ttu-id="a111f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a111f-115">-DefaultProfile</span></span>
<span data-ttu-id="a111f-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a111f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a111f-117">-Description</span><span class="sxs-lookup"><span data-stu-id="a111f-117">-Description</span></span>
<span data-ttu-id="a111f-118">Descrição da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="a111f-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="a111f-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a111f-119">-FriendlyName</span></span>
<span data-ttu-id="a111f-120">Nome amigável da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="a111f-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="a111f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a111f-121">-InputObject</span></span>
<span data-ttu-id="a111f-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a111f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a111f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a111f-123">-Name</span></span>
<span data-ttu-id="a111f-124">O nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="a111f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a111f-125">-ResourceGroupName</span></span>
<span data-ttu-id="a111f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a111f-126">The name of the resource group.</span></span>
<span data-ttu-id="a111f-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a111f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a111f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a111f-128">-SubscriptionId</span></span>
<span data-ttu-id="a111f-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a111f-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a111f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a111f-130">-Tag</span></span>
<span data-ttu-id="a111f-131">tags a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="a111f-131">tags to be updated</span></span>

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

### <span data-ttu-id="a111f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a111f-132">-Confirm</span></span>
<span data-ttu-id="a111f-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a111f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a111f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a111f-134">-WhatIf</span></span>
<span data-ttu-id="a111f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a111f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a111f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a111f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a111f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a111f-137">CommonParameters</span></span>
<span data-ttu-id="a111f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a111f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a111f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a111f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a111f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a111f-140">INPUTS</span></span>

### <span data-ttu-id="a111f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a111f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a111f-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a111f-142">OUTPUTS</span></span>

### <span data-ttu-id="a111f-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="a111f-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="a111f-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a111f-144">NOTES</span></span>

<span data-ttu-id="a111f-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a111f-145">ALIASES</span></span>

<span data-ttu-id="a111f-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a111f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a111f-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a111f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a111f-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a111f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a111f-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a111f-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a111f-150">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a111f-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a111f-151">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a111f-152">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a111f-153">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a111f-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a111f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a111f-155">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a111f-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a111f-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a111f-157">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a111f-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a111f-158">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a111f-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a111f-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a111f-160">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a111f-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a111f-161">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a111f-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a111f-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a111f-162">RELATED LINKS</span></span>

