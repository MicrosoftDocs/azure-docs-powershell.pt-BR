---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 016719f32af1af9acdc4543d565f9acc086b05fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432860"
---
# <span data-ttu-id="d1119-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="d1119-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="d1119-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1119-102">SYNOPSIS</span></span>
<span data-ttu-id="d1119-103">Desconectar um usersession.</span><span class="sxs-lookup"><span data-stu-id="d1119-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="d1119-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1119-104">SYNTAX</span></span>

### <span data-ttu-id="d1119-105">Desconectar (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1119-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1119-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1119-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1119-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1119-107">DESCRIPTION</span></span>
<span data-ttu-id="d1119-108">Desconectar um usersession.</span><span class="sxs-lookup"><span data-stu-id="d1119-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="d1119-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1119-109">EXAMPLES</span></span>

### <span data-ttu-id="d1119-110">Exemplo 1: desconectar um usersession da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="d1119-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="d1119-111">Este comando desconecta uma sessão do userdesktop virtual do Windows em um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="d1119-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="d1119-112">OS</span><span class="sxs-lookup"><span data-stu-id="d1119-112">PARAMETERS</span></span>

### <span data-ttu-id="d1119-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1119-113">-DefaultProfile</span></span>
<span data-ttu-id="d1119-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1119-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1119-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d1119-115">-HostPoolName</span></span>
<span data-ttu-id="d1119-116">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1119-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d1119-117">-Id</span></span>
<span data-ttu-id="d1119-118">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1119-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1119-119">-InputObject</span></span>
<span data-ttu-id="d1119-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d1119-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1119-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1119-121">-PassThru</span></span>
<span data-ttu-id="d1119-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d1119-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d1119-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1119-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1119-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1119-124">The name of the resource group.</span></span>
<span data-ttu-id="d1119-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d1119-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1119-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="d1119-126">-SessionHostName</span></span>
<span data-ttu-id="d1119-127">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1119-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1119-128">-SubscriptionId</span></span>
<span data-ttu-id="d1119-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d1119-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1119-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1119-130">-Confirm</span></span>
<span data-ttu-id="d1119-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1119-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1119-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1119-132">-WhatIf</span></span>
<span data-ttu-id="d1119-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1119-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1119-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1119-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1119-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1119-135">CommonParameters</span></span>
<span data-ttu-id="d1119-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1119-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1119-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1119-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1119-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1119-138">INPUTS</span></span>

### <span data-ttu-id="d1119-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d1119-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d1119-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1119-140">OUTPUTS</span></span>

### <span data-ttu-id="d1119-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1119-141">System.Boolean</span></span>

## <span data-ttu-id="d1119-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1119-142">NOTES</span></span>

<span data-ttu-id="d1119-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d1119-143">ALIASES</span></span>

<span data-ttu-id="d1119-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d1119-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1119-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d1119-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1119-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1119-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1119-147">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d1119-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1119-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d1119-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d1119-149">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d1119-150">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d1119-151">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d1119-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d1119-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1119-153">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d1119-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1119-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d1119-155">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d1119-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="d1119-156">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d1119-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d1119-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d1119-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="d1119-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d1119-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d1119-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d1119-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1119-160">RELATED LINKS</span></span>

