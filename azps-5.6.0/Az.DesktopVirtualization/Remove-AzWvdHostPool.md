---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 42902280d93797613197f7da3263418e0fc8672e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887140"
---
# <span data-ttu-id="75ded-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="75ded-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="75ded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ded-102">SYNOPSIS</span></span>
<span data-ttu-id="75ded-103">Remover um pool de host.</span><span class="sxs-lookup"><span data-stu-id="75ded-103">Remove a host pool.</span></span>

## <span data-ttu-id="75ded-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="75ded-104">SYNTAX</span></span>

### <span data-ttu-id="75ded-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75ded-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75ded-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75ded-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75ded-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="75ded-107">DESCRIPTION</span></span>
<span data-ttu-id="75ded-108">Remover um pool de host.</span><span class="sxs-lookup"><span data-stu-id="75ded-108">Remove a host pool.</span></span>

## <span data-ttu-id="75ded-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75ded-109">EXAMPLES</span></span>

### <span data-ttu-id="75ded-110">Exemplo 1: Excluir um HostPool da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="75ded-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="75ded-111">Este comando exclui um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="75ded-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="75ded-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="75ded-112">PARAMETERS</span></span>

### <span data-ttu-id="75ded-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ded-113">-DefaultProfile</span></span>
<span data-ttu-id="75ded-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75ded-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ded-115">-Force</span><span class="sxs-lookup"><span data-stu-id="75ded-115">-Force</span></span>
<span data-ttu-id="75ded-116">Forçar o sinalizador a excluir sessionHost.</span><span class="sxs-lookup"><span data-stu-id="75ded-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="75ded-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75ded-117">-InputObject</span></span>
<span data-ttu-id="75ded-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="75ded-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="75ded-119">-Name</span><span class="sxs-lookup"><span data-stu-id="75ded-119">-Name</span></span>
<span data-ttu-id="75ded-120">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ded-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75ded-121">-PassThru</span></span>
<span data-ttu-id="75ded-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="75ded-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="75ded-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ded-123">-ResourceGroupName</span></span>
<span data-ttu-id="75ded-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75ded-124">The name of the resource group.</span></span>
<span data-ttu-id="75ded-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="75ded-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="75ded-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75ded-126">-SubscriptionId</span></span>
<span data-ttu-id="75ded-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="75ded-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="75ded-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75ded-128">-Confirm</span></span>
<span data-ttu-id="75ded-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75ded-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ded-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ded-130">-WhatIf</span></span>
<span data-ttu-id="75ded-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75ded-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ded-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75ded-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ded-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ded-133">CommonParameters</span></span>
<span data-ttu-id="75ded-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ded-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ded-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75ded-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ded-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75ded-136">INPUTS</span></span>

### <span data-ttu-id="75ded-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="75ded-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="75ded-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="75ded-138">OUTPUTS</span></span>

### <span data-ttu-id="75ded-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75ded-139">System.Boolean</span></span>

## <span data-ttu-id="75ded-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="75ded-140">NOTES</span></span>

<span data-ttu-id="75ded-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="75ded-141">ALIASES</span></span>

<span data-ttu-id="75ded-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="75ded-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75ded-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="75ded-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75ded-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75ded-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75ded-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="75ded-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75ded-146">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="75ded-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="75ded-147">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="75ded-148">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="75ded-149">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="75ded-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="75ded-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75ded-151">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="75ded-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75ded-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="75ded-153">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="75ded-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="75ded-154">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="75ded-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="75ded-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="75ded-156">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="75ded-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="75ded-157">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="75ded-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="75ded-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75ded-158">RELATED LINKS</span></span>

