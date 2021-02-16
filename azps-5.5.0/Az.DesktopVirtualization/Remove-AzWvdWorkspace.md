---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: bd266bf6fe8a4239a1e2f10a5b462afd0fcc3577
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117691"
---
# <span data-ttu-id="31f0e-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="31f0e-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="31f0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="31f0e-103">Remover um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="31f0e-103">Remove a workspace.</span></span>

## <span data-ttu-id="31f0e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31f0e-104">SYNTAX</span></span>

### <span data-ttu-id="31f0e-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="31f0e-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="31f0e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="31f0e-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31f0e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="31f0e-107">DESCRIPTION</span></span>
<span data-ttu-id="31f0e-108">Remover um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="31f0e-108">Remove a workspace.</span></span>

## <span data-ttu-id="31f0e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31f0e-109">EXAMPLES</span></span>

### <span data-ttu-id="31f0e-110">Exemplo 1: Excluir um Espaço de Trabalho Virtual da Área de Trabalho do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="31f0e-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="31f0e-111">Esse comando exclui um Espaço de Trabalho Virtual da Área de Trabalho do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="31f0e-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="31f0e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31f0e-112">PARAMETERS</span></span>

### <span data-ttu-id="31f0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f0e-113">-DefaultProfile</span></span>
<span data-ttu-id="31f0e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31f0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f0e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31f0e-115">-InputObject</span></span>
<span data-ttu-id="31f0e-116">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="31f0e-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="31f0e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31f0e-117">-Name</span></span>
<span data-ttu-id="31f0e-118">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="31f0e-118">The name of the workspace</span></span>

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

### <span data-ttu-id="31f0e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31f0e-119">-PassThru</span></span>
<span data-ttu-id="31f0e-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="31f0e-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="31f0e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f0e-121">-ResourceGroupName</span></span>
<span data-ttu-id="31f0e-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31f0e-122">The name of the resource group.</span></span>
<span data-ttu-id="31f0e-123">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="31f0e-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="31f0e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31f0e-124">-SubscriptionId</span></span>
<span data-ttu-id="31f0e-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="31f0e-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="31f0e-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="31f0e-126">-Confirm</span></span>
<span data-ttu-id="31f0e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f0e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f0e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f0e-128">-WhatIf</span></span>
<span data-ttu-id="31f0e-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="31f0e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f0e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31f0e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f0e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f0e-131">CommonParameters</span></span>
<span data-ttu-id="31f0e-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f0e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f0e-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31f0e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f0e-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="31f0e-134">INPUTS</span></span>

### <span data-ttu-id="31f0e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="31f0e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="31f0e-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="31f0e-136">OUTPUTS</span></span>

### <span data-ttu-id="31f0e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31f0e-137">System.Boolean</span></span>

## <span data-ttu-id="31f0e-138">Notas</span><span class="sxs-lookup"><span data-stu-id="31f0e-138">NOTES</span></span>

<span data-ttu-id="31f0e-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="31f0e-139">ALIASES</span></span>

<span data-ttu-id="31f0e-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="31f0e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31f0e-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="31f0e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31f0e-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31f0e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31f0e-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="31f0e-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31f0e-144">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="31f0e-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="31f0e-145">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="31f0e-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="31f0e-146">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="31f0e-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="31f0e-147">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="31f0e-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="31f0e-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="31f0e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31f0e-149">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="31f0e-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="31f0e-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31f0e-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="31f0e-151">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="31f0e-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="31f0e-152">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="31f0e-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="31f0e-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="31f0e-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="31f0e-154">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="31f0e-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="31f0e-155">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="31f0e-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="31f0e-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31f0e-156">RELATED LINKS</span></span>

