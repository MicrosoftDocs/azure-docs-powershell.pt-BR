---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955600"
---
# <span data-ttu-id="0e8f8-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="0e8f8-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="0e8f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8f8-103">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-103">Update a session host.</span></span>

## <span data-ttu-id="0e8f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e8f8-104">SYNTAX</span></span>

### <span data-ttu-id="0e8f8-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="0e8f8-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0e8f8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0e8f8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e8f8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e8f8-107">DESCRIPTION</span></span>
<span data-ttu-id="0e8f8-108">Atualizar um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-108">Update a session host.</span></span>

## <span data-ttu-id="0e8f8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e8f8-109">EXAMPLES</span></span>

### <span data-ttu-id="0e8f8-110">Exemplo 1: atualizar um SessionHost de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="0e8f8-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="0e8f8-111">Esse comando atualiza um SessionHost de área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="0e8f8-112">OS</span><span class="sxs-lookup"><span data-stu-id="0e8f8-112">PARAMETERS</span></span>

### <span data-ttu-id="0e8f8-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="0e8f8-113">-AllowNewSession</span></span>
<span data-ttu-id="0e8f8-114">Permitir uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-114">Allow a new session.</span></span>

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

### <span data-ttu-id="0e8f8-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="0e8f8-115">-AssignedUser</span></span>
<span data-ttu-id="0e8f8-116">Usuário atribuído a SessionHost.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="0e8f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8f8-117">-DefaultProfile</span></span>
<span data-ttu-id="0e8f8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e8f8-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="0e8f8-119">-HostPoolName</span></span>
<span data-ttu-id="0e8f8-120">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="0e8f8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e8f8-121">-InputObject</span></span>
<span data-ttu-id="0e8f8-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e8f8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e8f8-123">-Name</span></span>
<span data-ttu-id="0e8f8-124">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-124">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="0e8f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e8f8-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-126">The name of the resource group.</span></span>
<span data-ttu-id="0e8f8-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0e8f8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e8f8-128">-SubscriptionId</span></span>
<span data-ttu-id="0e8f8-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0e8f8-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e8f8-130">-Confirm</span></span>
<span data-ttu-id="0e8f8-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8f8-132">-WhatIf</span></span>
<span data-ttu-id="0e8f8-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8f8-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8f8-135">CommonParameters</span></span>
<span data-ttu-id="0e8f8-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8f8-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e8f8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8f8-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e8f8-138">INPUTS</span></span>

### <span data-ttu-id="0e8f8-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0e8f8-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0e8f8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e8f8-140">OUTPUTS</span></span>

### <span data-ttu-id="0e8f8-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="0e8f8-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="0e8f8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e8f8-142">NOTES</span></span>

<span data-ttu-id="0e8f8-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0e8f8-143">ALIASES</span></span>

<span data-ttu-id="0e8f8-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="0e8f8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e8f8-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e8f8-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e8f8-147">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="0e8f8-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e8f8-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="0e8f8-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0e8f8-149">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0e8f8-150">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0e8f8-151">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0e8f8-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0e8f8-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e8f8-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0e8f8-154">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="0e8f8-155">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0e8f8-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0e8f8-157">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="0e8f8-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0e8f8-158">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0e8f8-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0e8f8-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e8f8-159">RELATED LINKS</span></span>

