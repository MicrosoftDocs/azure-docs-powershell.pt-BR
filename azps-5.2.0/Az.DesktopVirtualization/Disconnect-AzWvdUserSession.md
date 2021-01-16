---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 016719f32af1af9acdc4543d565f9acc086b05fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258299"
---
# <span data-ttu-id="a87bd-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="a87bd-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="a87bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a87bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a87bd-103">Desconectar um usersession.</span><span class="sxs-lookup"><span data-stu-id="a87bd-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="a87bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a87bd-104">SYNTAX</span></span>

### <span data-ttu-id="a87bd-105">Desconectar (padrão)</span><span class="sxs-lookup"><span data-stu-id="a87bd-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a87bd-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a87bd-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a87bd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a87bd-107">DESCRIPTION</span></span>
<span data-ttu-id="a87bd-108">Desconectar um usersession.</span><span class="sxs-lookup"><span data-stu-id="a87bd-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="a87bd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a87bd-109">EXAMPLES</span></span>

### <span data-ttu-id="a87bd-110">Exemplo 1: desconectar um usersession da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="a87bd-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="a87bd-111">Este comando desconecta uma sessão do userdesktop virtual do Windows em um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="a87bd-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="a87bd-112">OS</span><span class="sxs-lookup"><span data-stu-id="a87bd-112">PARAMETERS</span></span>

### <span data-ttu-id="a87bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87bd-113">-DefaultProfile</span></span>
<span data-ttu-id="a87bd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a87bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a87bd-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a87bd-115">-HostPoolName</span></span>
<span data-ttu-id="a87bd-116">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a87bd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a87bd-117">-Id</span></span>
<span data-ttu-id="a87bd-118">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="a87bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a87bd-119">-InputObject</span></span>
<span data-ttu-id="a87bd-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a87bd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a87bd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a87bd-121">-PassThru</span></span>
<span data-ttu-id="a87bd-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a87bd-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a87bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a87bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="a87bd-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a87bd-124">The name of the resource group.</span></span>
<span data-ttu-id="a87bd-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a87bd-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a87bd-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="a87bd-126">-SessionHostName</span></span>
<span data-ttu-id="a87bd-127">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="a87bd-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a87bd-128">-SubscriptionId</span></span>
<span data-ttu-id="a87bd-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a87bd-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a87bd-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a87bd-130">-Confirm</span></span>
<span data-ttu-id="a87bd-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a87bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a87bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87bd-132">-WhatIf</span></span>
<span data-ttu-id="a87bd-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a87bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a87bd-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a87bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a87bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87bd-135">CommonParameters</span></span>
<span data-ttu-id="a87bd-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87bd-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a87bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87bd-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a87bd-138">INPUTS</span></span>

### <span data-ttu-id="a87bd-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a87bd-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a87bd-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a87bd-140">OUTPUTS</span></span>

### <span data-ttu-id="a87bd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a87bd-141">System.Boolean</span></span>

## <span data-ttu-id="a87bd-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a87bd-142">NOTES</span></span>

<span data-ttu-id="a87bd-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a87bd-143">ALIASES</span></span>

<span data-ttu-id="a87bd-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a87bd-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a87bd-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a87bd-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a87bd-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a87bd-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a87bd-147">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a87bd-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a87bd-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a87bd-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a87bd-149">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a87bd-150">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a87bd-151">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a87bd-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a87bd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a87bd-153">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a87bd-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a87bd-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a87bd-155">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a87bd-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="a87bd-156">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a87bd-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a87bd-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a87bd-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a87bd-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a87bd-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a87bd-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a87bd-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a87bd-160">RELATED LINKS</span></span>

