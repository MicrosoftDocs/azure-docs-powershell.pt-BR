---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: e0bc6fc07f03727295bc3a6babf204eaf405ae74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887138"
---
# <span data-ttu-id="d2ed8-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d2ed8-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="d2ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ed8-103">Remover um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="d2ed8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2ed8-104">SYNTAX</span></span>

### <span data-ttu-id="d2ed8-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2ed8-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2ed8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2ed8-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2ed8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="d2ed8-108">Remover um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="d2ed8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ed8-110">Exemplo 1: Excluir pacote MSIX pelo nome completo do pacote</span><span class="sxs-lookup"><span data-stu-id="d2ed8-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="d2ed8-111">Este comando exclui um pacote MSIX em um HostPool</span><span class="sxs-lookup"><span data-stu-id="d2ed8-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="d2ed8-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2ed8-112">PARAMETERS</span></span>

### <span data-ttu-id="d2ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="d2ed8-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ed8-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="d2ed8-115">-FullName</span></span>
<span data-ttu-id="d2ed8-116">O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed8-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d2ed8-117">-HostPoolName</span></span>
<span data-ttu-id="d2ed8-118">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d2ed8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2ed8-119">-InputObject</span></span>
<span data-ttu-id="d2ed8-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2ed8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2ed8-121">-PassThru</span></span>
<span data-ttu-id="d2ed8-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d2ed8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2ed8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ed8-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2ed8-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-124">The name of the resource group.</span></span>
<span data-ttu-id="d2ed8-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d2ed8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2ed8-126">-SubscriptionId</span></span>
<span data-ttu-id="d2ed8-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d2ed8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ed8-128">-Confirm</span></span>
<span data-ttu-id="d2ed8-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ed8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ed8-130">-WhatIf</span></span>
<span data-ttu-id="d2ed8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ed8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ed8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ed8-133">CommonParameters</span></span>
<span data-ttu-id="d2ed8-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ed8-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2ed8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ed8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2ed8-136">INPUTS</span></span>

### <span data-ttu-id="d2ed8-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d2ed8-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d2ed8-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2ed8-138">OUTPUTS</span></span>

### <span data-ttu-id="d2ed8-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2ed8-139">System.Boolean</span></span>

## <span data-ttu-id="d2ed8-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2ed8-140">NOTES</span></span>

<span data-ttu-id="d2ed8-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2ed8-141">ALIASES</span></span>

<span data-ttu-id="d2ed8-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d2ed8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2ed8-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2ed8-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2ed8-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="d2ed8-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2ed8-146">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d2ed8-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d2ed8-147">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d2ed8-148">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d2ed8-149">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d2ed8-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d2ed8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2ed8-151">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d2ed8-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2ed8-153">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2ed8-154">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d2ed8-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d2ed8-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2ed8-156">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="d2ed8-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d2ed8-157">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d2ed8-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d2ed8-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2ed8-158">RELATED LINKS</span></span>

