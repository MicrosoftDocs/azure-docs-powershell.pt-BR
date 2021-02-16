---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113226"
---
# <span data-ttu-id="a3512-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="a3512-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="a3512-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3512-102">SYNOPSIS</span></span>
<span data-ttu-id="a3512-103">Enviar uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="a3512-103">Send a message to a user.</span></span>

## <span data-ttu-id="a3512-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3512-104">SYNTAX</span></span>

### <span data-ttu-id="a3512-105">SendExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3512-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3512-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a3512-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3512-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3512-107">DESCRIPTION</span></span>
<span data-ttu-id="a3512-108">Enviar uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="a3512-108">Send a message to a user.</span></span>

## <span data-ttu-id="a3512-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3512-109">EXAMPLES</span></span>

### <span data-ttu-id="a3512-110">Exemplo 1: Enviar uma mensagem para UserSession</span><span class="sxs-lookup"><span data-stu-id="a3512-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="a3512-111">Esse comando envia uma mensagem para uma UserSession.</span><span class="sxs-lookup"><span data-stu-id="a3512-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="a3512-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3512-112">PARAMETERS</span></span>

### <span data-ttu-id="a3512-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3512-113">-DefaultProfile</span></span>
<span data-ttu-id="a3512-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3512-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3512-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a3512-115">-HostPoolName</span></span>
<span data-ttu-id="a3512-116">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a3512-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3512-117">-InputObject</span></span>
<span data-ttu-id="a3512-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a3512-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3512-119">-Message Ressal</span><span class="sxs-lookup"><span data-stu-id="a3512-119">-MessageBody</span></span>
<span data-ttu-id="a3512-120">Corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3512-120">Body of message.</span></span>

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

### <span data-ttu-id="a3512-121">-Título da Mensagem</span><span class="sxs-lookup"><span data-stu-id="a3512-121">-MessageTitle</span></span>
<span data-ttu-id="a3512-122">Título da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3512-122">Title of message.</span></span>

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

### <span data-ttu-id="a3512-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3512-123">-PassThru</span></span>
<span data-ttu-id="a3512-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a3512-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a3512-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3512-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3512-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3512-126">The name of the resource group.</span></span>
<span data-ttu-id="a3512-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3512-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a3512-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="a3512-128">-SessionHostName</span></span>
<span data-ttu-id="a3512-129">O nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="a3512-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3512-130">-SubscriptionId</span></span>
<span data-ttu-id="a3512-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a3512-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a3512-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="a3512-132">-UserSessionId</span></span>
<span data-ttu-id="a3512-133">O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="a3512-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a3512-134">-Confirm</span></span>
<span data-ttu-id="a3512-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3512-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3512-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3512-136">-WhatIf</span></span>
<span data-ttu-id="a3512-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a3512-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3512-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3512-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3512-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3512-139">CommonParameters</span></span>
<span data-ttu-id="a3512-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3512-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3512-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3512-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3512-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3512-142">INPUTS</span></span>

### <span data-ttu-id="a3512-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a3512-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a3512-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3512-144">OUTPUTS</span></span>

### <span data-ttu-id="a3512-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3512-145">System.Boolean</span></span>

## <span data-ttu-id="a3512-146">Notas</span><span class="sxs-lookup"><span data-stu-id="a3512-146">NOTES</span></span>

<span data-ttu-id="a3512-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="a3512-147">ALIASES</span></span>

<span data-ttu-id="a3512-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a3512-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3512-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a3512-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3512-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3512-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3512-151">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a3512-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3512-152">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a3512-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a3512-153">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a3512-154">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a3512-155">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a3512-156">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a3512-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3512-157">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a3512-158">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3512-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a3512-159">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3512-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="a3512-160">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a3512-161">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a3512-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a3512-162">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a3512-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a3512-163">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a3512-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a3512-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3512-164">RELATED LINKS</span></span>

