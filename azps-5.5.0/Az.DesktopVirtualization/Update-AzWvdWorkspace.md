---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 8a20777cfd6e28c3edc127117687b7aef801d94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127009"
---
# <span data-ttu-id="6c8d8-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c8d8-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="6c8d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8d8-103">Atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-103">Update a workspace.</span></span>

## <span data-ttu-id="6c8d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c8d8-104">SYNTAX</span></span>

### <span data-ttu-id="6c8d8-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6c8d8-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c8d8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6c8d8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c8d8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="6c8d8-108">Atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-108">Update a workspace.</span></span>

## <span data-ttu-id="6c8d8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c8d8-109">EXAMPLES</span></span>

### <span data-ttu-id="6c8d8-110">Exemplo 1: Atualizar um Espaço de Trabalho Virtual da Área de Trabalho do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="6c8d8-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="6c8d8-111">Este comando atualiza um Espaço de Trabalho virtual da área de trabalho do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="6c8d8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c8d8-112">PARAMETERS</span></span>

### <span data-ttu-id="6c8d8-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="6c8d8-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="6c8d8-114">Lista de links de grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8d8-115">-DefaultProfile</span></span>
<span data-ttu-id="6c8d8-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c8d8-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6c8d8-117">-Description</span></span>
<span data-ttu-id="6c8d8-118">Descrição do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="6c8d8-119">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="6c8d8-119">-FriendlyName</span></span>
<span data-ttu-id="6c8d8-120">Nome amigável do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="6c8d8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c8d8-121">-InputObject</span></span>
<span data-ttu-id="6c8d8-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c8d8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c8d8-123">-Name</span></span>
<span data-ttu-id="6c8d8-124">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="6c8d8-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c8d8-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-126">The name of the resource group.</span></span>
<span data-ttu-id="6c8d8-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6c8d8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c8d8-128">-SubscriptionId</span></span>
<span data-ttu-id="6c8d8-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6c8d8-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c8d8-130">-Tag</span></span>
<span data-ttu-id="6c8d8-131">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="6c8d8-131">tags to be updated</span></span>

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

### <span data-ttu-id="6c8d8-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6c8d8-132">-Confirm</span></span>
<span data-ttu-id="6c8d8-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8d8-134">-WhatIf</span></span>
<span data-ttu-id="6c8d8-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8d8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8d8-137">CommonParameters</span></span>
<span data-ttu-id="6c8d8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8d8-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c8d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8d8-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="6c8d8-140">INPUTS</span></span>

### <span data-ttu-id="6c8d8-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6c8d8-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6c8d8-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="6c8d8-142">OUTPUTS</span></span>

### <span data-ttu-id="6c8d8-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c8d8-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="6c8d8-144">Notas</span><span class="sxs-lookup"><span data-stu-id="6c8d8-144">NOTES</span></span>

<span data-ttu-id="6c8d8-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="6c8d8-145">ALIASES</span></span>

<span data-ttu-id="6c8d8-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="6c8d8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c8d8-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c8d8-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c8d8-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="6c8d8-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c8d8-150">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6c8d8-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6c8d8-151">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="6c8d8-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6c8d8-152">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="6c8d8-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6c8d8-153">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="6c8d8-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6c8d8-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="6c8d8-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c8d8-155">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="6c8d8-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6c8d8-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6c8d8-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="6c8d8-158">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="6c8d8-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6c8d8-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6c8d8-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6c8d8-160">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="6c8d8-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6c8d8-161">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="6c8d8-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6c8d8-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c8d8-162">RELATED LINKS</span></span>

