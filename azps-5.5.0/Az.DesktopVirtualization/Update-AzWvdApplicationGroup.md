---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113854"
---
# <span data-ttu-id="4dfd7-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4dfd7-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4dfd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4dfd7-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfd7-103">Atualizar um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="4dfd7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4dfd7-104">SYNTAX</span></span>

### <span data-ttu-id="4dfd7-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4dfd7-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4dfd7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4dfd7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4dfd7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dfd7-107">DESCRIPTION</span></span>
<span data-ttu-id="4dfd7-108">Atualizar um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="4dfd7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4dfd7-109">EXAMPLES</span></span>

### <span data-ttu-id="4dfd7-110">Exemplo 1: Criar um Grupo de Aplicativos da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="4dfd7-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="4dfd7-111">Esse comando cria um Grupo de Aplicativos da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="4dfd7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4dfd7-112">PARAMETERS</span></span>

### <span data-ttu-id="4dfd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfd7-113">-DefaultProfile</span></span>
<span data-ttu-id="4dfd7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfd7-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4dfd7-115">-Description</span></span>
<span data-ttu-id="4dfd7-116">Descrição do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4dfd7-117">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="4dfd7-117">-FriendlyName</span></span>
<span data-ttu-id="4dfd7-118">Nome amigável do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4dfd7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dfd7-119">-InputObject</span></span>
<span data-ttu-id="4dfd7-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4dfd7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dfd7-121">-Name</span></span>
<span data-ttu-id="4dfd7-122">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="4dfd7-122">The name of the application group</span></span>

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

### <span data-ttu-id="4dfd7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dfd7-123">-ResourceGroupName</span></span>
<span data-ttu-id="4dfd7-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-124">The name of the resource group.</span></span>
<span data-ttu-id="4dfd7-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4dfd7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dfd7-126">-SubscriptionId</span></span>
<span data-ttu-id="4dfd7-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4dfd7-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dfd7-128">-Tag</span></span>
<span data-ttu-id="4dfd7-129">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="4dfd7-129">tags to be updated</span></span>

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

### <span data-ttu-id="4dfd7-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4dfd7-130">-Confirm</span></span>
<span data-ttu-id="4dfd7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfd7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfd7-132">-WhatIf</span></span>
<span data-ttu-id="4dfd7-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dfd7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfd7-135">CommonParameters</span></span>
<span data-ttu-id="4dfd7-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfd7-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dfd7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfd7-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="4dfd7-138">INPUTS</span></span>

### <span data-ttu-id="4dfd7-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4dfd7-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4dfd7-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="4dfd7-140">OUTPUTS</span></span>

### <span data-ttu-id="4dfd7-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4dfd7-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="4dfd7-142">Notas</span><span class="sxs-lookup"><span data-stu-id="4dfd7-142">NOTES</span></span>

<span data-ttu-id="4dfd7-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="4dfd7-143">ALIASES</span></span>

<span data-ttu-id="4dfd7-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4dfd7-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4dfd7-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4dfd7-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4dfd7-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4dfd7-148">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="4dfd7-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4dfd7-149">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="4dfd7-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4dfd7-150">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="4dfd7-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4dfd7-151">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="4dfd7-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4dfd7-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4dfd7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4dfd7-153">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="4dfd7-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4dfd7-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4dfd7-155">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="4dfd7-156">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="4dfd7-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4dfd7-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4dfd7-158">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="4dfd7-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4dfd7-159">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="4dfd7-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4dfd7-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-160">RELATED LINKS</span></span>

