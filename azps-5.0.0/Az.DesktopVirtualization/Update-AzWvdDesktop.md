---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117479"
---
# <span data-ttu-id="f3343-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="f3343-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="f3343-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3343-102">SYNOPSIS</span></span>
<span data-ttu-id="f3343-103">Atualize uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3343-103">Update a desktop.</span></span>

## <span data-ttu-id="f3343-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3343-104">SYNTAX</span></span>

### <span data-ttu-id="f3343-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3343-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3343-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f3343-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f3343-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3343-107">DESCRIPTION</span></span>
<span data-ttu-id="f3343-108">Atualize uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3343-108">Update a desktop.</span></span>

## <span data-ttu-id="f3343-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3343-109">EXAMPLES</span></span>

### <span data-ttu-id="f3343-110">Exemplo 1: atualizar uma área de trabalho da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="f3343-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="f3343-111">Esse comando atualiza uma área de trabalho da área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="f3343-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="f3343-112">OS</span><span class="sxs-lookup"><span data-stu-id="f3343-112">PARAMETERS</span></span>

### <span data-ttu-id="f3343-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="f3343-113">-ApplicationGroupName</span></span>
<span data-ttu-id="f3343-114">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f3343-114">The name of the application group</span></span>

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

### <span data-ttu-id="f3343-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3343-115">-DefaultProfile</span></span>
<span data-ttu-id="f3343-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3343-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3343-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f3343-117">-Description</span></span>
<span data-ttu-id="f3343-118">Descrição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3343-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="f3343-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3343-119">-FriendlyName</span></span>
<span data-ttu-id="f3343-120">Nome amigável da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3343-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="f3343-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3343-121">-InputObject</span></span>
<span data-ttu-id="f3343-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f3343-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3343-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3343-123">-Name</span></span>
<span data-ttu-id="f3343-124">O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="f3343-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="f3343-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3343-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3343-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3343-126">The name of the resource group.</span></span>
<span data-ttu-id="f3343-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3343-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f3343-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3343-128">-SubscriptionId</span></span>
<span data-ttu-id="f3343-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f3343-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f3343-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="f3343-130">-Tag</span></span>
<span data-ttu-id="f3343-131">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="f3343-131">tags to be updated</span></span>

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

### <span data-ttu-id="f3343-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3343-132">-Confirm</span></span>
<span data-ttu-id="f3343-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3343-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3343-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3343-134">-WhatIf</span></span>
<span data-ttu-id="f3343-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3343-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3343-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3343-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3343-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3343-137">CommonParameters</span></span>
<span data-ttu-id="f3343-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3343-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3343-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3343-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3343-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3343-140">INPUTS</span></span>

### <span data-ttu-id="f3343-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f3343-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f3343-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3343-142">OUTPUTS</span></span>

### <span data-ttu-id="f3343-143">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="f3343-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="f3343-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3343-144">NOTES</span></span>

<span data-ttu-id="f3343-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f3343-145">ALIASES</span></span>

<span data-ttu-id="f3343-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f3343-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3343-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f3343-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3343-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3343-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3343-149">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f3343-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3343-150">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f3343-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f3343-151">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="f3343-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f3343-152">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="f3343-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f3343-153">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="f3343-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f3343-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f3343-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3343-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3343-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f3343-156">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3343-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="f3343-157">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="f3343-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f3343-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f3343-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f3343-159">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="f3343-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f3343-160">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="f3343-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f3343-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3343-161">RELATED LINKS</span></span>

