---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113227"
---
# <span data-ttu-id="be567-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="be567-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="be567-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be567-102">SYNOPSIS</span></span>
<span data-ttu-id="be567-103">Remover uma userSession.</span><span class="sxs-lookup"><span data-stu-id="be567-103">Remove a userSession.</span></span>

## <span data-ttu-id="be567-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be567-104">SYNTAX</span></span>

### <span data-ttu-id="be567-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be567-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be567-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be567-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be567-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="be567-107">DESCRIPTION</span></span>
<span data-ttu-id="be567-108">Remover uma userSession.</span><span class="sxs-lookup"><span data-stu-id="be567-108">Remove a userSession.</span></span>

## <span data-ttu-id="be567-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be567-109">EXAMPLES</span></span>

### <span data-ttu-id="be567-110">Exemplo 1: Excluir uma UserSession da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="be567-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="be567-111">Esse comando exclui uma UserSessão da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="be567-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="be567-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be567-112">PARAMETERS</span></span>

### <span data-ttu-id="be567-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be567-113">-DefaultProfile</span></span>
<span data-ttu-id="be567-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be567-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be567-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="be567-115">-Force</span></span>
<span data-ttu-id="be567-116">Forçar o sinalizador a fazer logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="be567-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="be567-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="be567-117">-HostPoolName</span></span>
<span data-ttu-id="be567-118">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="be567-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="be567-119">-ID</span><span class="sxs-lookup"><span data-stu-id="be567-119">-Id</span></span>
<span data-ttu-id="be567-120">O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="be567-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="be567-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be567-121">-InputObject</span></span>
<span data-ttu-id="be567-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="be567-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be567-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be567-123">-PassThru</span></span>
<span data-ttu-id="be567-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="be567-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="be567-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be567-125">-ResourceGroupName</span></span>
<span data-ttu-id="be567-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="be567-126">The name of the resource group.</span></span>
<span data-ttu-id="be567-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be567-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="be567-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="be567-128">-SessionHostName</span></span>
<span data-ttu-id="be567-129">O nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="be567-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="be567-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be567-130">-SubscriptionId</span></span>
<span data-ttu-id="be567-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="be567-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="be567-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="be567-132">-Confirm</span></span>
<span data-ttu-id="be567-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be567-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be567-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be567-134">-WhatIf</span></span>
<span data-ttu-id="be567-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="be567-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be567-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be567-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be567-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be567-137">CommonParameters</span></span>
<span data-ttu-id="be567-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be567-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be567-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be567-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be567-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="be567-140">INPUTS</span></span>

### <span data-ttu-id="be567-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="be567-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="be567-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="be567-142">OUTPUTS</span></span>

### <span data-ttu-id="be567-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be567-143">System.Boolean</span></span>

## <span data-ttu-id="be567-144">Notas</span><span class="sxs-lookup"><span data-stu-id="be567-144">NOTES</span></span>

<span data-ttu-id="be567-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="be567-145">ALIASES</span></span>

<span data-ttu-id="be567-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="be567-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be567-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="be567-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be567-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be567-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be567-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="be567-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be567-150">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="be567-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="be567-151">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="be567-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="be567-152">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="be567-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="be567-153">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="be567-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="be567-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="be567-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be567-155">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="be567-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="be567-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="be567-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="be567-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be567-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="be567-158">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="be567-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="be567-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="be567-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="be567-160">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="be567-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="be567-161">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="be567-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="be567-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be567-162">RELATED LINKS</span></span>

