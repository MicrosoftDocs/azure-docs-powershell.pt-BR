---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 04e7c192659ec1f1aa71b0bf1b97e61030cd9b4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257546"
---
# <span data-ttu-id="36f4c-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="36f4c-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="36f4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="36f4c-103">Atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36f4c-103">Update a workspace.</span></span>

## <span data-ttu-id="36f4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36f4c-104">SYNTAX</span></span>

### <span data-ttu-id="36f4c-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="36f4c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36f4c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36f4c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36f4c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="36f4c-108">Atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36f4c-108">Update a workspace.</span></span>

## <span data-ttu-id="36f4c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36f4c-109">EXAMPLES</span></span>

### <span data-ttu-id="36f4c-110">Exemplo 1: atualizar um espaço de trabalho da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="36f4c-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="36f4c-111">Este comando atualiza um espaço de trabalho da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36f4c-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="36f4c-112">OS</span><span class="sxs-lookup"><span data-stu-id="36f4c-112">PARAMETERS</span></span>

### <span data-ttu-id="36f4c-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="36f4c-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="36f4c-114">Lista de links de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36f4c-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="36f4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f4c-115">-DefaultProfile</span></span>
<span data-ttu-id="36f4c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36f4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f4c-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="36f4c-117">-Description</span></span>
<span data-ttu-id="36f4c-118">Descrição do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36f4c-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="36f4c-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="36f4c-119">-FriendlyName</span></span>
<span data-ttu-id="36f4c-120">Nome amigável do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36f4c-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="36f4c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36f4c-121">-InputObject</span></span>
<span data-ttu-id="36f4c-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="36f4c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36f4c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="36f4c-123">-Name</span></span>
<span data-ttu-id="36f4c-124">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="36f4c-124">The name of the workspace</span></span>

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

### <span data-ttu-id="36f4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="36f4c-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36f4c-126">The name of the resource group.</span></span>
<span data-ttu-id="36f4c-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="36f4c-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36f4c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36f4c-128">-SubscriptionId</span></span>
<span data-ttu-id="36f4c-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="36f4c-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36f4c-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="36f4c-130">-Tag</span></span>
<span data-ttu-id="36f4c-131">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="36f4c-131">tags to be updated</span></span>

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

### <span data-ttu-id="36f4c-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36f4c-132">-Confirm</span></span>
<span data-ttu-id="36f4c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f4c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f4c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f4c-134">-WhatIf</span></span>
<span data-ttu-id="36f4c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36f4c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f4c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36f4c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f4c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f4c-137">CommonParameters</span></span>
<span data-ttu-id="36f4c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f4c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f4c-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36f4c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f4c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36f4c-140">INPUTS</span></span>

### <span data-ttu-id="36f4c-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="36f4c-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="36f4c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36f4c-142">OUTPUTS</span></span>

### <span data-ttu-id="36f4c-143">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="36f4c-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="36f4c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36f4c-144">NOTES</span></span>

<span data-ttu-id="36f4c-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36f4c-145">ALIASES</span></span>

<span data-ttu-id="36f4c-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="36f4c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36f4c-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="36f4c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36f4c-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36f4c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36f4c-149">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="36f4c-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36f4c-150">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="36f4c-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="36f4c-151">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="36f4c-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="36f4c-152">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="36f4c-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="36f4c-153">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="36f4c-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="36f4c-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="36f4c-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36f4c-155">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="36f4c-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="36f4c-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36f4c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36f4c-157">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="36f4c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="36f4c-158">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="36f4c-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="36f4c-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="36f4c-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="36f4c-160">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="36f4c-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="36f4c-161">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="36f4c-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="36f4c-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36f4c-162">RELATED LINKS</span></span>

