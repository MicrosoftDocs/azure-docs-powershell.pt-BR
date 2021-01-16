---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428406"
---
# <span data-ttu-id="f3a72-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="f3a72-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="f3a72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3a72-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a72-103">Remover um usersession.</span><span class="sxs-lookup"><span data-stu-id="f3a72-103">Remove a userSession.</span></span>

## <span data-ttu-id="f3a72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3a72-104">SYNTAX</span></span>

### <span data-ttu-id="f3a72-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3a72-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3a72-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3a72-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3a72-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3a72-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a72-108">Remover um usersession.</span><span class="sxs-lookup"><span data-stu-id="f3a72-108">Remove a userSession.</span></span>

## <span data-ttu-id="f3a72-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3a72-109">EXAMPLES</span></span>

### <span data-ttu-id="f3a72-110">Exemplo 1: excluir um usersession de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="f3a72-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="f3a72-111">Esse comando exclui uma sessão do userdesktop virtual do Windows em um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="f3a72-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="f3a72-112">OS</span><span class="sxs-lookup"><span data-stu-id="f3a72-112">PARAMETERS</span></span>

### <span data-ttu-id="f3a72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a72-113">-DefaultProfile</span></span>
<span data-ttu-id="f3a72-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3a72-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f3a72-115">-Force</span></span>
<span data-ttu-id="f3a72-116">Force o sinalizador a fazer logon no usersession.</span><span class="sxs-lookup"><span data-stu-id="f3a72-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="f3a72-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f3a72-117">-HostPoolName</span></span>
<span data-ttu-id="f3a72-118">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a72-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f3a72-119">-Id</span></span>
<span data-ttu-id="f3a72-120">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a72-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3a72-121">-InputObject</span></span>
<span data-ttu-id="f3a72-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f3a72-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a72-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3a72-123">-PassThru</span></span>
<span data-ttu-id="f3a72-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f3a72-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3a72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a72-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3a72-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3a72-126">The name of the resource group.</span></span>
<span data-ttu-id="f3a72-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3a72-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a72-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="f3a72-128">-SessionHostName</span></span>
<span data-ttu-id="f3a72-129">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a72-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3a72-130">-SubscriptionId</span></span>
<span data-ttu-id="f3a72-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f3a72-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a72-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3a72-132">-Confirm</span></span>
<span data-ttu-id="f3a72-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3a72-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a72-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a72-134">-WhatIf</span></span>
<span data-ttu-id="f3a72-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3a72-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a72-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3a72-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a72-137">CommonParameters</span></span>
<span data-ttu-id="f3a72-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3a72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a72-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3a72-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a72-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3a72-140">INPUTS</span></span>

### <span data-ttu-id="f3a72-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f3a72-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f3a72-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3a72-142">OUTPUTS</span></span>

### <span data-ttu-id="f3a72-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3a72-143">System.Boolean</span></span>

## <span data-ttu-id="f3a72-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3a72-144">NOTES</span></span>

<span data-ttu-id="f3a72-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f3a72-145">ALIASES</span></span>

<span data-ttu-id="f3a72-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f3a72-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3a72-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f3a72-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3a72-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3a72-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3a72-149">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f3a72-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3a72-150">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f3a72-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f3a72-151">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f3a72-152">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f3a72-153">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f3a72-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f3a72-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3a72-155">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f3a72-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3a72-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f3a72-157">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3a72-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="f3a72-158">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f3a72-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f3a72-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f3a72-160">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="f3a72-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f3a72-161">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="f3a72-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f3a72-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3a72-162">RELATED LINKS</span></span>

