---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 016719f32af1af9acdc4543d565f9acc086b05fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115832"
---
# <span data-ttu-id="96bff-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="96bff-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="96bff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96bff-102">SYNOPSIS</span></span>
<span data-ttu-id="96bff-103">Desconectar uma userSession.</span><span class="sxs-lookup"><span data-stu-id="96bff-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="96bff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96bff-104">SYNTAX</span></span>

### <span data-ttu-id="96bff-105">Desconectar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96bff-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96bff-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96bff-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96bff-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="96bff-107">DESCRIPTION</span></span>
<span data-ttu-id="96bff-108">Desconectar uma userSession.</span><span class="sxs-lookup"><span data-stu-id="96bff-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="96bff-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96bff-109">EXAMPLES</span></span>

### <span data-ttu-id="96bff-110">Exemplo 1: Desconectar uma UserSession da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="96bff-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="96bff-111">Esse comando desconecta uma UserSessão da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="96bff-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="96bff-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96bff-112">PARAMETERS</span></span>

### <span data-ttu-id="96bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96bff-113">-DefaultProfile</span></span>
<span data-ttu-id="96bff-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96bff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96bff-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="96bff-115">-HostPoolName</span></span>
<span data-ttu-id="96bff-116">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="96bff-117">-ID</span><span class="sxs-lookup"><span data-stu-id="96bff-117">-Id</span></span>
<span data-ttu-id="96bff-118">O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="96bff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96bff-119">-InputObject</span></span>
<span data-ttu-id="96bff-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="96bff-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96bff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96bff-121">-PassThru</span></span>
<span data-ttu-id="96bff-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="96bff-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="96bff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96bff-123">-ResourceGroupName</span></span>
<span data-ttu-id="96bff-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96bff-124">The name of the resource group.</span></span>
<span data-ttu-id="96bff-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96bff-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="96bff-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="96bff-126">-SessionHostName</span></span>
<span data-ttu-id="96bff-127">O nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="96bff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96bff-128">-SubscriptionId</span></span>
<span data-ttu-id="96bff-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="96bff-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="96bff-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96bff-130">-Confirm</span></span>
<span data-ttu-id="96bff-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96bff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96bff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96bff-132">-WhatIf</span></span>
<span data-ttu-id="96bff-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96bff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96bff-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96bff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96bff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bff-135">CommonParameters</span></span>
<span data-ttu-id="96bff-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96bff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bff-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96bff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bff-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="96bff-138">INPUTS</span></span>

### <span data-ttu-id="96bff-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="96bff-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="96bff-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="96bff-140">OUTPUTS</span></span>

### <span data-ttu-id="96bff-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96bff-141">System.Boolean</span></span>

## <span data-ttu-id="96bff-142">Notas</span><span class="sxs-lookup"><span data-stu-id="96bff-142">NOTES</span></span>

<span data-ttu-id="96bff-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="96bff-143">ALIASES</span></span>

<span data-ttu-id="96bff-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="96bff-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96bff-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="96bff-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96bff-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96bff-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96bff-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="96bff-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96bff-148">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="96bff-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="96bff-149">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="96bff-150">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="96bff-151">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="96bff-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="96bff-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96bff-153">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="96bff-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96bff-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="96bff-155">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96bff-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="96bff-156">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="96bff-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="96bff-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="96bff-158">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="96bff-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="96bff-159">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="96bff-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="96bff-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96bff-160">RELATED LINKS</span></span>

