---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887161"
---
# <span data-ttu-id="1e5ea-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="1e5ea-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="1e5ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5ea-103">Desconecte uma userSession.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="1e5ea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1e5ea-104">SYNTAX</span></span>

### <span data-ttu-id="1e5ea-105">Desconectar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1e5ea-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e5ea-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e5ea-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e5ea-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1e5ea-107">DESCRIPTION</span></span>
<span data-ttu-id="1e5ea-108">Desconecte uma userSession.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="1e5ea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e5ea-109">EXAMPLES</span></span>

### <span data-ttu-id="1e5ea-110">Exemplo 1: Desconectar uma UserSession da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="1e5ea-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="1e5ea-111">Este comando desconecta uma UserSession da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="1e5ea-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1e5ea-112">PARAMETERS</span></span>

### <span data-ttu-id="1e5ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5ea-113">-DefaultProfile</span></span>
<span data-ttu-id="1e5ea-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e5ea-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="1e5ea-115">-HostPoolName</span></span>
<span data-ttu-id="1e5ea-116">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="1e5ea-117">-Id</span><span class="sxs-lookup"><span data-stu-id="1e5ea-117">-Id</span></span>
<span data-ttu-id="1e5ea-118">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="1e5ea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e5ea-119">-InputObject</span></span>
<span data-ttu-id="1e5ea-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e5ea-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e5ea-121">-PassThru</span></span>
<span data-ttu-id="1e5ea-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="1e5ea-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1e5ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e5ea-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-124">The name of the resource group.</span></span>
<span data-ttu-id="1e5ea-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e5ea-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="1e5ea-126">-SessionHostName</span></span>
<span data-ttu-id="1e5ea-127">O nome do host de sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="1e5ea-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e5ea-128">-SubscriptionId</span></span>
<span data-ttu-id="1e5ea-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1e5ea-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e5ea-130">-Confirm</span></span>
<span data-ttu-id="1e5ea-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5ea-132">-WhatIf</span></span>
<span data-ttu-id="1e5ea-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5ea-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5ea-135">CommonParameters</span></span>
<span data-ttu-id="1e5ea-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5ea-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e5ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5ea-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e5ea-138">INPUTS</span></span>

### <span data-ttu-id="1e5ea-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1e5ea-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1e5ea-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1e5ea-140">OUTPUTS</span></span>

### <span data-ttu-id="1e5ea-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e5ea-141">System.Boolean</span></span>

## <span data-ttu-id="1e5ea-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="1e5ea-142">NOTES</span></span>

<span data-ttu-id="1e5ea-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1e5ea-143">ALIASES</span></span>

<span data-ttu-id="1e5ea-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="1e5ea-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e5ea-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e5ea-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e5ea-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="1e5ea-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e5ea-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="1e5ea-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1e5ea-149">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1e5ea-150">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1e5ea-151">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1e5ea-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1e5ea-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e5ea-153">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="1e5ea-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1e5ea-155">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="1e5ea-156">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1e5ea-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1e5ea-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1e5ea-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="1e5ea-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1e5ea-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1e5ea-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1e5ea-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e5ea-160">RELATED LINKS</span></span>

