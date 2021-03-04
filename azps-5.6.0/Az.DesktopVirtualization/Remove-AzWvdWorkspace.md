---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 682f59c5c07643ecd93fd1ae051abc8e74c4e185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888946"
---
# <span data-ttu-id="d5ed0-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5ed0-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="d5ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ed0-103">Remova um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-103">Remove a workspace.</span></span>

## <span data-ttu-id="d5ed0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d5ed0-104">SYNTAX</span></span>

### <span data-ttu-id="d5ed0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d5ed0-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5ed0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d5ed0-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5ed0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d5ed0-107">DESCRIPTION</span></span>
<span data-ttu-id="d5ed0-108">Remova um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-108">Remove a workspace.</span></span>

## <span data-ttu-id="d5ed0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="d5ed0-110">Exemplo 1: Excluir um Espaço de Trabalho da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="d5ed0-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="d5ed0-111">Este comando exclui um Espaço de Trabalho da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="d5ed0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="d5ed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ed0-113">-DefaultProfile</span></span>
<span data-ttu-id="d5ed0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ed0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5ed0-115">-InputObject</span></span>
<span data-ttu-id="d5ed0-116">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5ed0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d5ed0-117">-Name</span></span>
<span data-ttu-id="d5ed0-118">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d5ed0-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ed0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5ed0-119">-PassThru</span></span>
<span data-ttu-id="d5ed0-120">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d5ed0-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d5ed0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ed0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5ed0-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-122">The name of the resource group.</span></span>
<span data-ttu-id="d5ed0-123">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d5ed0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5ed0-124">-SubscriptionId</span></span>
<span data-ttu-id="d5ed0-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d5ed0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5ed0-126">-Confirm</span></span>
<span data-ttu-id="d5ed0-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ed0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ed0-128">-WhatIf</span></span>
<span data-ttu-id="d5ed0-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5ed0-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ed0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ed0-131">CommonParameters</span></span>
<span data-ttu-id="d5ed0-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ed0-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5ed0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ed0-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-134">INPUTS</span></span>

### <span data-ttu-id="d5ed0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d5ed0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d5ed0-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-136">OUTPUTS</span></span>

### <span data-ttu-id="d5ed0-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5ed0-137">System.Boolean</span></span>

## <span data-ttu-id="d5ed0-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="d5ed0-138">NOTES</span></span>

<span data-ttu-id="d5ed0-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d5ed0-139">ALIASES</span></span>

<span data-ttu-id="d5ed0-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d5ed0-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5ed0-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5ed0-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5ed0-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="d5ed0-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5ed0-144">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d5ed0-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d5ed0-145">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="d5ed0-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d5ed0-146">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="d5ed0-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d5ed0-147">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d5ed0-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d5ed0-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d5ed0-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5ed0-149">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="d5ed0-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d5ed0-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d5ed0-151">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="d5ed0-152">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="d5ed0-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d5ed0-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d5ed0-154">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="d5ed0-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d5ed0-155">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d5ed0-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d5ed0-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-156">RELATED LINKS</span></span>

