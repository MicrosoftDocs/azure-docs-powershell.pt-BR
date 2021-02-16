---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113223"
---
# <span data-ttu-id="d0e0c-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d0e0c-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="d0e0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e0c-103">Atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="d0e0c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0e0c-104">SYNTAX</span></span>

### <span data-ttu-id="d0e0c-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d0e0c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0e0c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d0e0c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0e0c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0e0c-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e0c-108">Atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="d0e0c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0e0c-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e0c-110">Exemplo 1: Atualizar um pacote MSIX</span><span class="sxs-lookup"><span data-stu-id="d0e0c-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="d0e0c-111">Este comando atualiza um Pacote MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="d0e0c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0e0c-112">PARAMETERS</span></span>

### <span data-ttu-id="d0e0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e0c-113">-DefaultProfile</span></span>
<span data-ttu-id="d0e0c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0e0c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d0e0c-115">-DisplayName</span></span>
<span data-ttu-id="d0e0c-116">Nome de exibição do pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="d0e0c-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="d0e0c-117">-FullName</span></span>
<span data-ttu-id="d0e0c-118">O nome completo do pacote de versão específico do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="d0e0c-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d0e0c-119">-HostPoolName</span></span>
<span data-ttu-id="d0e0c-120">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d0e0c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0e0c-121">-InputObject</span></span>
<span data-ttu-id="d0e0c-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d0e0c-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="d0e0c-123">-IsActive</span></span>
<span data-ttu-id="d0e0c-124">Definir uma versão do pacote para ser ativa em hostpool.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="d0e0c-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="d0e0c-125">-IsRegularRegistration</span></span>
<span data-ttu-id="d0e0c-126">Definir o modo de Registro.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-126">Set Registration mode.</span></span>
<span data-ttu-id="d0e0c-127">Regular ou atrasado.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="d0e0c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e0c-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0e0c-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-129">The name of the resource group.</span></span>
<span data-ttu-id="d0e0c-130">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d0e0c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0e0c-131">-SubscriptionId</span></span>
<span data-ttu-id="d0e0c-132">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d0e0c-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d0e0c-133">-Confirm</span></span>
<span data-ttu-id="d0e0c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e0c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e0c-135">-WhatIf</span></span>
<span data-ttu-id="d0e0c-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e0c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e0c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e0c-138">CommonParameters</span></span>
<span data-ttu-id="d0e0c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e0c-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0e0c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e0c-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="d0e0c-141">INPUTS</span></span>

### <span data-ttu-id="d0e0c-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d0e0c-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d0e0c-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="d0e0c-143">OUTPUTS</span></span>

### <span data-ttu-id="d0e0c-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d0e0c-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="d0e0c-145">Notas</span><span class="sxs-lookup"><span data-stu-id="d0e0c-145">NOTES</span></span>

<span data-ttu-id="d0e0c-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="d0e0c-146">ALIASES</span></span>

<span data-ttu-id="d0e0c-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d0e0c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0e0c-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0e0c-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0e0c-150">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="d0e0c-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0e0c-151">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d0e0c-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d0e0c-152">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d0e0c-153">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d0e0c-154">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d0e0c-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d0e0c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0e0c-156">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d0e0c-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d0e0c-158">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="d0e0c-159">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d0e0c-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d0e0c-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d0e0c-161">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="d0e0c-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d0e0c-162">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0e0c-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d0e0c-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0e0c-163">RELATED LINKS</span></span>

