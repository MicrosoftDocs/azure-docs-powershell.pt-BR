---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ddc8dee2e553701fc8f7660fe72b4070ff9eafa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113849"
---
# <span data-ttu-id="49b26-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="49b26-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="49b26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49b26-102">SYNOPSIS</span></span>
<span data-ttu-id="49b26-103">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="49b26-103">Update a session host.</span></span>

## <span data-ttu-id="49b26-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49b26-104">SYNTAX</span></span>

### <span data-ttu-id="49b26-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="49b26-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49b26-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="49b26-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49b26-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="49b26-107">DESCRIPTION</span></span>
<span data-ttu-id="49b26-108">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="49b26-108">Update a session host.</span></span>

## <span data-ttu-id="49b26-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49b26-109">EXAMPLES</span></span>

### <span data-ttu-id="49b26-110">Exemplo 1: Atualizar um Windows Virtual Desktop SessionHost por nome</span><span class="sxs-lookup"><span data-stu-id="49b26-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="49b26-111">Este comando atualiza um Windows Virtual Desktop SessionHost em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="49b26-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="49b26-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49b26-112">PARAMETERS</span></span>

### <span data-ttu-id="49b26-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="49b26-113">-AllowNewSession</span></span>
<span data-ttu-id="49b26-114">Permitir uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="49b26-114">Allow a new session.</span></span>

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

### <span data-ttu-id="49b26-115">-AtribuídoUsuário</span><span class="sxs-lookup"><span data-stu-id="49b26-115">-AssignedUser</span></span>
<span data-ttu-id="49b26-116">Usuário atribuído ao SessionHost.</span><span class="sxs-lookup"><span data-stu-id="49b26-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="49b26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b26-117">-DefaultProfile</span></span>
<span data-ttu-id="49b26-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49b26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b26-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="49b26-119">-HostPoolName</span></span>
<span data-ttu-id="49b26-120">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="49b26-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49b26-121">-InputObject</span></span>
<span data-ttu-id="49b26-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="49b26-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49b26-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="49b26-123">-Name</span></span>
<span data-ttu-id="49b26-124">O nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-124">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="49b26-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b26-125">-ResourceGroupName</span></span>
<span data-ttu-id="49b26-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49b26-126">The name of the resource group.</span></span>
<span data-ttu-id="49b26-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="49b26-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="49b26-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49b26-128">-SubscriptionId</span></span>
<span data-ttu-id="49b26-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="49b26-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="49b26-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="49b26-130">-Confirm</span></span>
<span data-ttu-id="49b26-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b26-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b26-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b26-132">-WhatIf</span></span>
<span data-ttu-id="49b26-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="49b26-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b26-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49b26-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b26-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b26-135">CommonParameters</span></span>
<span data-ttu-id="49b26-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b26-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b26-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49b26-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b26-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="49b26-138">INPUTS</span></span>

### <span data-ttu-id="49b26-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="49b26-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="49b26-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="49b26-140">OUTPUTS</span></span>

### <span data-ttu-id="49b26-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="49b26-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="49b26-142">Notas</span><span class="sxs-lookup"><span data-stu-id="49b26-142">NOTES</span></span>

<span data-ttu-id="49b26-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="49b26-143">ALIASES</span></span>

<span data-ttu-id="49b26-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="49b26-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49b26-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="49b26-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49b26-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49b26-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49b26-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="49b26-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49b26-148">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="49b26-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="49b26-149">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="49b26-150">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="49b26-151">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="49b26-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="49b26-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49b26-153">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="49b26-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49b26-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="49b26-155">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="49b26-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="49b26-156">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="49b26-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="49b26-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="49b26-158">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="49b26-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="49b26-159">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="49b26-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="49b26-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49b26-160">RELATED LINKS</span></span>

