---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 1976c5750b5372cedce8ccf237fe8a444fa1feee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887137"
---
# <span data-ttu-id="4d3fc-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="4d3fc-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="4d3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3fc-103">Envie uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-103">Send a message to a user.</span></span>

## <span data-ttu-id="4d3fc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4d3fc-104">SYNTAX</span></span>

### <span data-ttu-id="4d3fc-105">SendExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d3fc-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d3fc-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4d3fc-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d3fc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4d3fc-107">DESCRIPTION</span></span>
<span data-ttu-id="4d3fc-108">Envie uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-108">Send a message to a user.</span></span>

## <span data-ttu-id="4d3fc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d3fc-109">EXAMPLES</span></span>

### <span data-ttu-id="4d3fc-110">Exemplo 1: Enviar uma mensagem para UserSession</span><span class="sxs-lookup"><span data-stu-id="4d3fc-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="4d3fc-111">Este comando envia uma mensagem para um UserSession.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="4d3fc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4d3fc-112">PARAMETERS</span></span>

### <span data-ttu-id="4d3fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3fc-113">-DefaultProfile</span></span>
<span data-ttu-id="4d3fc-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d3fc-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4d3fc-115">-HostPoolName</span></span>
<span data-ttu-id="4d3fc-116">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3fc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d3fc-117">-InputObject</span></span>
<span data-ttu-id="4d3fc-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3fc-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="4d3fc-119">-MessageBody</span></span>
<span data-ttu-id="4d3fc-120">Corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-120">Body of message.</span></span>

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

### <span data-ttu-id="4d3fc-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="4d3fc-121">-MessageTitle</span></span>
<span data-ttu-id="4d3fc-122">Título da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-122">Title of message.</span></span>

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

### <span data-ttu-id="4d3fc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d3fc-123">-PassThru</span></span>
<span data-ttu-id="4d3fc-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4d3fc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4d3fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d3fc-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-126">The name of the resource group.</span></span>
<span data-ttu-id="4d3fc-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3fc-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="4d3fc-128">-SessionHostName</span></span>
<span data-ttu-id="4d3fc-129">O nome do host de sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3fc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d3fc-130">-SubscriptionId</span></span>
<span data-ttu-id="4d3fc-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3fc-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="4d3fc-132">-UserSessionId</span></span>
<span data-ttu-id="4d3fc-133">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3fc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d3fc-134">-Confirm</span></span>
<span data-ttu-id="4d3fc-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d3fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3fc-136">-WhatIf</span></span>
<span data-ttu-id="4d3fc-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3fc-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d3fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3fc-139">CommonParameters</span></span>
<span data-ttu-id="4d3fc-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3fc-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d3fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3fc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d3fc-142">INPUTS</span></span>

### <span data-ttu-id="4d3fc-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4d3fc-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4d3fc-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4d3fc-144">OUTPUTS</span></span>

### <span data-ttu-id="4d3fc-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d3fc-145">System.Boolean</span></span>

## <span data-ttu-id="4d3fc-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="4d3fc-146">NOTES</span></span>

<span data-ttu-id="4d3fc-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4d3fc-147">ALIASES</span></span>

<span data-ttu-id="4d3fc-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="4d3fc-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d3fc-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d3fc-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d3fc-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="4d3fc-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d3fc-152">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="4d3fc-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4d3fc-153">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4d3fc-154">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4d3fc-155">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4d3fc-156">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4d3fc-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d3fc-157">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4d3fc-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d3fc-159">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d3fc-160">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4d3fc-161">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4d3fc-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4d3fc-162">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="4d3fc-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4d3fc-163">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="4d3fc-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4d3fc-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d3fc-164">RELATED LINKS</span></span>

