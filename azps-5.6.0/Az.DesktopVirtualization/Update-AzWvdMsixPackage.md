---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: f552c8e21703d64efa2ac65f47461daa963fc1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889333"
---
# <span data-ttu-id="92214-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="92214-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="92214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92214-102">SYNOPSIS</span></span>
<span data-ttu-id="92214-103">Atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="92214-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="92214-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92214-104">SYNTAX</span></span>

### <span data-ttu-id="92214-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92214-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92214-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="92214-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92214-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92214-107">DESCRIPTION</span></span>
<span data-ttu-id="92214-108">Atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="92214-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="92214-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92214-109">EXAMPLES</span></span>

### <span data-ttu-id="92214-110">Exemplo 1: atualizar um pacote MSIX</span><span class="sxs-lookup"><span data-stu-id="92214-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="92214-111">Este comando atualiza um pacote MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="92214-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="92214-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92214-112">PARAMETERS</span></span>

### <span data-ttu-id="92214-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92214-113">-DefaultProfile</span></span>
<span data-ttu-id="92214-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92214-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92214-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92214-115">-DisplayName</span></span>
<span data-ttu-id="92214-116">Nome de exibição do pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="92214-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="92214-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="92214-117">-FullName</span></span>
<span data-ttu-id="92214-118">O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="92214-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92214-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="92214-119">-HostPoolName</span></span>
<span data-ttu-id="92214-120">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="92214-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92214-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92214-121">-InputObject</span></span>
<span data-ttu-id="92214-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="92214-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92214-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="92214-123">-IsActive</span></span>
<span data-ttu-id="92214-124">Definir uma versão do pacote para ser ativa em hostpool.</span><span class="sxs-lookup"><span data-stu-id="92214-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="92214-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="92214-125">-IsRegularRegistration</span></span>
<span data-ttu-id="92214-126">Definir o modo de registro.</span><span class="sxs-lookup"><span data-stu-id="92214-126">Set Registration mode.</span></span>
<span data-ttu-id="92214-127">Regular ou atrasada.</span><span class="sxs-lookup"><span data-stu-id="92214-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="92214-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92214-128">-ResourceGroupName</span></span>
<span data-ttu-id="92214-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92214-129">The name of the resource group.</span></span>
<span data-ttu-id="92214-130">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92214-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92214-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92214-131">-SubscriptionId</span></span>
<span data-ttu-id="92214-132">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="92214-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92214-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92214-133">-Confirm</span></span>
<span data-ttu-id="92214-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92214-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92214-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92214-135">-WhatIf</span></span>
<span data-ttu-id="92214-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92214-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92214-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92214-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92214-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92214-138">CommonParameters</span></span>
<span data-ttu-id="92214-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92214-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92214-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92214-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92214-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92214-141">INPUTS</span></span>

### <span data-ttu-id="92214-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="92214-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="92214-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92214-143">OUTPUTS</span></span>

### <span data-ttu-id="92214-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="92214-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="92214-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="92214-145">NOTES</span></span>

<span data-ttu-id="92214-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="92214-146">ALIASES</span></span>

<span data-ttu-id="92214-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="92214-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92214-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="92214-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92214-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92214-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92214-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="92214-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92214-151">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="92214-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="92214-152">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="92214-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="92214-153">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="92214-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="92214-154">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="92214-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="92214-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="92214-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92214-156">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="92214-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="92214-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92214-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92214-158">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92214-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="92214-159">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="92214-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="92214-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="92214-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="92214-161">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="92214-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="92214-162">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="92214-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="92214-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92214-163">RELATED LINKS</span></span>

