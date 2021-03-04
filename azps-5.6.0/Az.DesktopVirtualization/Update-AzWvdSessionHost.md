---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: 9e8599edaa1a1c19d5b0629d290402c792cf2563
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889332"
---
# <span data-ttu-id="2e60f-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="2e60f-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="2e60f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e60f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e60f-103">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="2e60f-103">Update a session host.</span></span>

## <span data-ttu-id="2e60f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2e60f-104">SYNTAX</span></span>

### <span data-ttu-id="2e60f-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e60f-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2e60f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2e60f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e60f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2e60f-107">DESCRIPTION</span></span>
<span data-ttu-id="2e60f-108">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="2e60f-108">Update a session host.</span></span>

## <span data-ttu-id="2e60f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e60f-109">EXAMPLES</span></span>

### <span data-ttu-id="2e60f-110">Exemplo 1: Atualizar um SessionHost da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="2e60f-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="2e60f-111">Este comando atualiza um Windows Virtual Desktop SessionHost em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="2e60f-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="2e60f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2e60f-112">PARAMETERS</span></span>

### <span data-ttu-id="2e60f-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="2e60f-113">-AllowNewSession</span></span>
<span data-ttu-id="2e60f-114">Permitir uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="2e60f-114">Allow a new session.</span></span>

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

### <span data-ttu-id="2e60f-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="2e60f-115">-AssignedUser</span></span>
<span data-ttu-id="2e60f-116">Usuário atribuído ao SessionHost.</span><span class="sxs-lookup"><span data-stu-id="2e60f-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="2e60f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e60f-117">-DefaultProfile</span></span>
<span data-ttu-id="2e60f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e60f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e60f-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2e60f-119">-HostPoolName</span></span>
<span data-ttu-id="2e60f-120">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="2e60f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e60f-121">-InputObject</span></span>
<span data-ttu-id="2e60f-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2e60f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e60f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2e60f-123">-Name</span></span>
<span data-ttu-id="2e60f-124">O nome do host de sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-124">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="2e60f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e60f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e60f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e60f-126">The name of the resource group.</span></span>
<span data-ttu-id="2e60f-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2e60f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2e60f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e60f-128">-SubscriptionId</span></span>
<span data-ttu-id="2e60f-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2e60f-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2e60f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e60f-130">-Confirm</span></span>
<span data-ttu-id="2e60f-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e60f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e60f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e60f-132">-WhatIf</span></span>
<span data-ttu-id="2e60f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e60f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e60f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e60f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e60f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e60f-135">CommonParameters</span></span>
<span data-ttu-id="2e60f-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e60f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e60f-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e60f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e60f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e60f-138">INPUTS</span></span>

### <span data-ttu-id="2e60f-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2e60f-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2e60f-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2e60f-140">OUTPUTS</span></span>

### <span data-ttu-id="2e60f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="2e60f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="2e60f-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="2e60f-142">NOTES</span></span>

<span data-ttu-id="2e60f-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2e60f-143">ALIASES</span></span>

<span data-ttu-id="2e60f-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2e60f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e60f-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2e60f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e60f-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e60f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e60f-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="2e60f-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e60f-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e60f-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2e60f-149">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2e60f-150">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2e60f-151">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2e60f-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2e60f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e60f-153">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2e60f-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e60f-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2e60f-155">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2e60f-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="2e60f-156">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2e60f-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2e60f-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2e60f-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="2e60f-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2e60f-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2e60f-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2e60f-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e60f-160">RELATED LINKS</span></span>

