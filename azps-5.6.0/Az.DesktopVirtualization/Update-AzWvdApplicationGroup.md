---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: 55d2436d70061fb9fc70013a4d8a7ef7e99fa434
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890860"
---
# <span data-ttu-id="8d19a-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8d19a-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8d19a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d19a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d19a-103">Atualize um applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8d19a-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="8d19a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8d19a-104">SYNTAX</span></span>

### <span data-ttu-id="8d19a-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8d19a-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d19a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8d19a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8d19a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8d19a-107">DESCRIPTION</span></span>
<span data-ttu-id="8d19a-108">Atualize um applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8d19a-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="8d19a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d19a-109">EXAMPLES</span></span>

### <span data-ttu-id="8d19a-110">Exemplo 1: Criar um Grupo de Aplicativos de Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="8d19a-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="8d19a-111">Este comando cria um Windows Virtual Desktop ApplicationGroup em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8d19a-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="8d19a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8d19a-112">PARAMETERS</span></span>

### <span data-ttu-id="8d19a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d19a-113">-DefaultProfile</span></span>
<span data-ttu-id="8d19a-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d19a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d19a-115">-Description</span><span class="sxs-lookup"><span data-stu-id="8d19a-115">-Description</span></span>
<span data-ttu-id="8d19a-116">Descrição do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8d19a-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8d19a-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8d19a-117">-FriendlyName</span></span>
<span data-ttu-id="8d19a-118">Nome amigável de ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="8d19a-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8d19a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d19a-119">-InputObject</span></span>
<span data-ttu-id="8d19a-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8d19a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d19a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d19a-121">-Name</span></span>
<span data-ttu-id="8d19a-122">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8d19a-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d19a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d19a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d19a-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d19a-124">The name of the resource group.</span></span>
<span data-ttu-id="8d19a-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8d19a-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d19a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d19a-126">-SubscriptionId</span></span>
<span data-ttu-id="8d19a-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8d19a-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d19a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d19a-128">-Tag</span></span>
<span data-ttu-id="8d19a-129">tags a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="8d19a-129">tags to be updated</span></span>

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

### <span data-ttu-id="8d19a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d19a-130">-Confirm</span></span>
<span data-ttu-id="8d19a-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d19a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d19a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d19a-132">-WhatIf</span></span>
<span data-ttu-id="8d19a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d19a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d19a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d19a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d19a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d19a-135">CommonParameters</span></span>
<span data-ttu-id="8d19a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d19a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d19a-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d19a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d19a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d19a-138">INPUTS</span></span>

### <span data-ttu-id="8d19a-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8d19a-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8d19a-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8d19a-140">OUTPUTS</span></span>

### <span data-ttu-id="8d19a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8d19a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="8d19a-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="8d19a-142">NOTES</span></span>

<span data-ttu-id="8d19a-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8d19a-143">ALIASES</span></span>

<span data-ttu-id="8d19a-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="8d19a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d19a-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8d19a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d19a-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d19a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d19a-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="8d19a-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d19a-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8d19a-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8d19a-149">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="8d19a-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8d19a-150">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="8d19a-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8d19a-151">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="8d19a-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8d19a-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8d19a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d19a-153">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="8d19a-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8d19a-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d19a-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d19a-155">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8d19a-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d19a-156">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="8d19a-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8d19a-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8d19a-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d19a-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="8d19a-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8d19a-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8d19a-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8d19a-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d19a-160">RELATED LINKS</span></span>

