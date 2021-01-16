---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272893"
---
# <span data-ttu-id="34f23-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="34f23-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="34f23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34f23-102">SYNOPSIS</span></span>
<span data-ttu-id="34f23-103">Atualize um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="34f23-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="34f23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34f23-104">SYNTAX</span></span>

### <span data-ttu-id="34f23-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="34f23-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34f23-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="34f23-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34f23-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34f23-107">DESCRIPTION</span></span>
<span data-ttu-id="34f23-108">Atualize um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="34f23-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="34f23-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34f23-109">EXAMPLES</span></span>

### <span data-ttu-id="34f23-110">Exemplo 1: atualizar um pacote do MSIX</span><span class="sxs-lookup"><span data-stu-id="34f23-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="34f23-111">Esse comando atualiza um pacote MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="34f23-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="34f23-112">OS</span><span class="sxs-lookup"><span data-stu-id="34f23-112">PARAMETERS</span></span>

### <span data-ttu-id="34f23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f23-113">-DefaultProfile</span></span>
<span data-ttu-id="34f23-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34f23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f23-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="34f23-115">-DisplayName</span></span>
<span data-ttu-id="34f23-116">Nome para exibição do pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="34f23-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="34f23-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="34f23-117">-FullName</span></span>
<span data-ttu-id="34f23-118">O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="34f23-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="34f23-119">-HostPoolName</span></span>
<span data-ttu-id="34f23-120">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="34f23-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f23-121">-InputObject</span></span>
<span data-ttu-id="34f23-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="34f23-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34f23-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="34f23-123">-IsActive</span></span>
<span data-ttu-id="34f23-124">Defina uma versão do pacote a ser ativada em hostpool.</span><span class="sxs-lookup"><span data-stu-id="34f23-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="34f23-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="34f23-125">-IsRegularRegistration</span></span>
<span data-ttu-id="34f23-126">Definir o modo de registro.</span><span class="sxs-lookup"><span data-stu-id="34f23-126">Set Registration mode.</span></span>
<span data-ttu-id="34f23-127">Normal ou atrasada.</span><span class="sxs-lookup"><span data-stu-id="34f23-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="34f23-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f23-128">-ResourceGroupName</span></span>
<span data-ttu-id="34f23-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34f23-129">The name of the resource group.</span></span>
<span data-ttu-id="34f23-130">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="34f23-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34f23-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34f23-131">-SubscriptionId</span></span>
<span data-ttu-id="34f23-132">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="34f23-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34f23-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34f23-133">-Confirm</span></span>
<span data-ttu-id="34f23-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f23-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f23-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f23-135">-WhatIf</span></span>
<span data-ttu-id="34f23-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34f23-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f23-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34f23-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f23-138">CommonParameters</span></span>
<span data-ttu-id="34f23-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f23-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34f23-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f23-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34f23-141">INPUTS</span></span>

### <span data-ttu-id="34f23-142">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="34f23-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="34f23-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34f23-143">OUTPUTS</span></span>

### <span data-ttu-id="34f23-144">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="34f23-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="34f23-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34f23-145">NOTES</span></span>

<span data-ttu-id="34f23-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="34f23-146">ALIASES</span></span>

<span data-ttu-id="34f23-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="34f23-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34f23-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="34f23-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34f23-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34f23-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34f23-150">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="34f23-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34f23-151">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="34f23-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="34f23-152">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="34f23-153">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="34f23-154">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="34f23-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="34f23-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34f23-156">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="34f23-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34f23-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34f23-158">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="34f23-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="34f23-159">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="34f23-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="34f23-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34f23-161">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="34f23-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="34f23-162">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="34f23-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="34f23-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34f23-163">RELATED LINKS</span></span>

