---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114550"
---
# <span data-ttu-id="bad19-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="bad19-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="bad19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bad19-102">SYNOPSIS</span></span>
<span data-ttu-id="bad19-103">Remover um SessionHost.</span><span class="sxs-lookup"><span data-stu-id="bad19-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="bad19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bad19-104">SYNTAX</span></span>

### <span data-ttu-id="bad19-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="bad19-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bad19-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bad19-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bad19-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bad19-107">DESCRIPTION</span></span>
<span data-ttu-id="bad19-108">Remover um SessionHost.</span><span class="sxs-lookup"><span data-stu-id="bad19-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="bad19-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bad19-109">EXAMPLES</span></span>

### <span data-ttu-id="bad19-110">Exemplo 1: excluir um SessionHost da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="bad19-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="bad19-111">Esse comando exclui uma SessionHost da área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="bad19-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="bad19-112">OS</span><span class="sxs-lookup"><span data-stu-id="bad19-112">PARAMETERS</span></span>

### <span data-ttu-id="bad19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad19-113">-DefaultProfile</span></span>
<span data-ttu-id="bad19-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bad19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bad19-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bad19-115">-Force</span></span>
<span data-ttu-id="bad19-116">Force o sinalizador para forçar a exclusão do sessionHost mesmo quando o usersession existe.</span><span class="sxs-lookup"><span data-stu-id="bad19-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="bad19-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="bad19-117">-HostPoolName</span></span>
<span data-ttu-id="bad19-118">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="bad19-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bad19-119">-InputObject</span></span>
<span data-ttu-id="bad19-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bad19-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bad19-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bad19-121">-Name</span></span>
<span data-ttu-id="bad19-122">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad19-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bad19-123">-PassThru</span></span>
<span data-ttu-id="bad19-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bad19-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bad19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bad19-125">-ResourceGroupName</span></span>
<span data-ttu-id="bad19-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bad19-126">The name of the resource group.</span></span>
<span data-ttu-id="bad19-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bad19-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bad19-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bad19-128">-SubscriptionId</span></span>
<span data-ttu-id="bad19-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="bad19-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bad19-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bad19-130">-Confirm</span></span>
<span data-ttu-id="bad19-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bad19-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bad19-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bad19-132">-WhatIf</span></span>
<span data-ttu-id="bad19-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bad19-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bad19-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bad19-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bad19-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad19-135">CommonParameters</span></span>
<span data-ttu-id="bad19-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bad19-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad19-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bad19-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad19-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bad19-138">INPUTS</span></span>

### <span data-ttu-id="bad19-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="bad19-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bad19-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bad19-140">OUTPUTS</span></span>

### <span data-ttu-id="bad19-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bad19-141">System.Boolean</span></span>

## <span data-ttu-id="bad19-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bad19-142">NOTES</span></span>

<span data-ttu-id="bad19-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bad19-143">ALIASES</span></span>

<span data-ttu-id="bad19-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="bad19-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bad19-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="bad19-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bad19-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bad19-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bad19-147">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="bad19-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bad19-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="bad19-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bad19-149">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bad19-150">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bad19-151">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bad19-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="bad19-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bad19-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bad19-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bad19-154">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bad19-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="bad19-155">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bad19-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="bad19-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bad19-157">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="bad19-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bad19-158">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bad19-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bad19-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bad19-159">RELATED LINKS</span></span>

