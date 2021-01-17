---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ddc8dee2e553701fc8f7660fe72b4070ff9eafa1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429412"
---
# <span data-ttu-id="e4156-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="e4156-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="e4156-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4156-102">SYNOPSIS</span></span>
<span data-ttu-id="e4156-103">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="e4156-103">Update a session host.</span></span>

## <span data-ttu-id="e4156-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4156-104">SYNTAX</span></span>

### <span data-ttu-id="e4156-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4156-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4156-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e4156-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4156-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4156-107">DESCRIPTION</span></span>
<span data-ttu-id="e4156-108">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="e4156-108">Update a session host.</span></span>

## <span data-ttu-id="e4156-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4156-109">EXAMPLES</span></span>

### <span data-ttu-id="e4156-110">Exemplo 1: atualizar um SessionHost de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="e4156-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="e4156-111">Esse comando atualiza um SessionHost de área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="e4156-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="e4156-112">OS</span><span class="sxs-lookup"><span data-stu-id="e4156-112">PARAMETERS</span></span>

### <span data-ttu-id="e4156-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="e4156-113">-AllowNewSession</span></span>
<span data-ttu-id="e4156-114">Permitir uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="e4156-114">Allow a new session.</span></span>

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

### <span data-ttu-id="e4156-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="e4156-115">-AssignedUser</span></span>
<span data-ttu-id="e4156-116">Usuário atribuído a SessionHost.</span><span class="sxs-lookup"><span data-stu-id="e4156-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="e4156-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4156-117">-DefaultProfile</span></span>
<span data-ttu-id="e4156-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4156-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4156-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e4156-119">-HostPoolName</span></span>
<span data-ttu-id="e4156-120">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e4156-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4156-121">-InputObject</span></span>
<span data-ttu-id="e4156-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e4156-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4156-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4156-123">-Name</span></span>
<span data-ttu-id="e4156-124">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4156-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4156-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4156-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4156-126">The name of the resource group.</span></span>
<span data-ttu-id="e4156-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e4156-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e4156-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4156-128">-SubscriptionId</span></span>
<span data-ttu-id="e4156-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e4156-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e4156-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4156-130">-Confirm</span></span>
<span data-ttu-id="e4156-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4156-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4156-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4156-132">-WhatIf</span></span>
<span data-ttu-id="e4156-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4156-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4156-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4156-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4156-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4156-135">CommonParameters</span></span>
<span data-ttu-id="e4156-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4156-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4156-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4156-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4156-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4156-138">INPUTS</span></span>

### <span data-ttu-id="e4156-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e4156-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e4156-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4156-140">OUTPUTS</span></span>

### <span data-ttu-id="e4156-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="e4156-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="e4156-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4156-142">NOTES</span></span>

<span data-ttu-id="e4156-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e4156-143">ALIASES</span></span>

<span data-ttu-id="e4156-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e4156-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4156-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e4156-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4156-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4156-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4156-147">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e4156-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4156-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="e4156-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e4156-149">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e4156-150">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e4156-151">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e4156-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e4156-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4156-153">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e4156-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4156-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e4156-155">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e4156-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="e4156-156">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e4156-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e4156-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e4156-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="e4156-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e4156-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e4156-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e4156-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4156-160">RELATED LINKS</span></span>

