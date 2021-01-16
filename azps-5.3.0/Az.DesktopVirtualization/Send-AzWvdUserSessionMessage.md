---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428405"
---
# <span data-ttu-id="5578f-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="5578f-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="5578f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5578f-102">SYNOPSIS</span></span>
<span data-ttu-id="5578f-103">Enviar uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="5578f-103">Send a message to a user.</span></span>

## <span data-ttu-id="5578f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5578f-104">SYNTAX</span></span>

### <span data-ttu-id="5578f-105">SendExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="5578f-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5578f-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5578f-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5578f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5578f-107">DESCRIPTION</span></span>
<span data-ttu-id="5578f-108">Enviar uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="5578f-108">Send a message to a user.</span></span>

## <span data-ttu-id="5578f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5578f-109">EXAMPLES</span></span>

### <span data-ttu-id="5578f-110">Exemplo 1: Enviar uma mensagem para o usersession</span><span class="sxs-lookup"><span data-stu-id="5578f-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="5578f-111">Esse comando envia uma mensagem para um usersession.</span><span class="sxs-lookup"><span data-stu-id="5578f-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="5578f-112">OS</span><span class="sxs-lookup"><span data-stu-id="5578f-112">PARAMETERS</span></span>

### <span data-ttu-id="5578f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5578f-113">-DefaultProfile</span></span>
<span data-ttu-id="5578f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5578f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5578f-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5578f-115">-HostPoolName</span></span>
<span data-ttu-id="5578f-116">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5578f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5578f-117">-InputObject</span></span>
<span data-ttu-id="5578f-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5578f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5578f-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="5578f-119">-MessageBody</span></span>
<span data-ttu-id="5578f-120">Corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5578f-120">Body of message.</span></span>

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

### <span data-ttu-id="5578f-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="5578f-121">-MessageTitle</span></span>
<span data-ttu-id="5578f-122">Título da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5578f-122">Title of message.</span></span>

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

### <span data-ttu-id="5578f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5578f-123">-PassThru</span></span>
<span data-ttu-id="5578f-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="5578f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5578f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5578f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5578f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5578f-126">The name of the resource group.</span></span>
<span data-ttu-id="5578f-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5578f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5578f-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="5578f-128">-SessionHostName</span></span>
<span data-ttu-id="5578f-129">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="5578f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5578f-130">-SubscriptionId</span></span>
<span data-ttu-id="5578f-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5578f-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5578f-132">-Usersessionid</span><span class="sxs-lookup"><span data-stu-id="5578f-132">-UserSessionId</span></span>
<span data-ttu-id="5578f-133">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="5578f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5578f-134">-Confirm</span></span>
<span data-ttu-id="5578f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5578f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5578f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5578f-136">-WhatIf</span></span>
<span data-ttu-id="5578f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5578f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5578f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5578f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5578f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5578f-139">CommonParameters</span></span>
<span data-ttu-id="5578f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5578f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5578f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5578f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5578f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5578f-142">INPUTS</span></span>

### <span data-ttu-id="5578f-143">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5578f-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5578f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5578f-144">OUTPUTS</span></span>

### <span data-ttu-id="5578f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5578f-145">System.Boolean</span></span>

## <span data-ttu-id="5578f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5578f-146">NOTES</span></span>

<span data-ttu-id="5578f-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5578f-147">ALIASES</span></span>

<span data-ttu-id="5578f-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5578f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5578f-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5578f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5578f-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5578f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5578f-151">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5578f-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5578f-152">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="5578f-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5578f-153">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5578f-154">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5578f-155">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5578f-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5578f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5578f-157">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5578f-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5578f-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5578f-159">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5578f-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="5578f-160">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5578f-161">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5578f-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5578f-162">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="5578f-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5578f-163">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5578f-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5578f-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5578f-164">RELATED LINKS</span></span>

