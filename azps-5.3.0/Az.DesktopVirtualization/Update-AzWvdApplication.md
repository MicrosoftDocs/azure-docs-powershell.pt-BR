---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428404"
---
# <span data-ttu-id="53644-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="53644-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="53644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53644-102">SYNOPSIS</span></span>
<span data-ttu-id="53644-103">Atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-103">Update an application.</span></span>

## <span data-ttu-id="53644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53644-104">SYNTAX</span></span>

### <span data-ttu-id="53644-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="53644-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53644-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53644-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53644-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53644-107">DESCRIPTION</span></span>
<span data-ttu-id="53644-108">Atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-108">Update an application.</span></span>

## <span data-ttu-id="53644-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53644-109">EXAMPLES</span></span>

### <span data-ttu-id="53644-110">Exemplo 1: atualizar um aplicativo de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="53644-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="53644-111">Esse comando atualiza um aplicativo de área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="53644-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="53644-112">OS</span><span class="sxs-lookup"><span data-stu-id="53644-112">PARAMETERS</span></span>

### <span data-ttu-id="53644-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="53644-113">-ApplicationType</span></span>
<span data-ttu-id="53644-114">Tipo de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53644-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="53644-115">-CommandLineArgument</span></span>
<span data-ttu-id="53644-116">Argumentos de linha de comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="53644-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="53644-117">-CommandLineSetting</span></span>
<span data-ttu-id="53644-118">Especifica se esse aplicativo publicado pode ser iniciado com argumentos de linha de comando fornecidos pelo cliente, argumentos de linha de comando especificados no tempo de publicação ou nenhum argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="53644-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53644-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53644-119">-DefaultProfile</span></span>
<span data-ttu-id="53644-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53644-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53644-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="53644-121">-Description</span></span>
<span data-ttu-id="53644-122">Descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-122">Description of Application.</span></span>

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

### <span data-ttu-id="53644-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="53644-123">-FilePath</span></span>
<span data-ttu-id="53644-124">Especifica um caminho para o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="53644-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="53644-125">-FriendlyName</span></span>
<span data-ttu-id="53644-126">Nome amigável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53644-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="53644-127">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="53644-127">-GroupName</span></span>
<span data-ttu-id="53644-128">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="53644-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53644-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="53644-129">-IconIndex</span></span>
<span data-ttu-id="53644-130">Índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="53644-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53644-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="53644-131">-IconPath</span></span>
<span data-ttu-id="53644-132">Caminho para o ícone.</span><span class="sxs-lookup"><span data-stu-id="53644-132">Path to icon.</span></span>

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

### <span data-ttu-id="53644-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53644-133">-InputObject</span></span>
<span data-ttu-id="53644-134">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="53644-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="53644-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="53644-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="53644-136">Especifica a ID do aplicativo do pacote para aplicativos MSIX</span><span class="sxs-lookup"><span data-stu-id="53644-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="53644-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="53644-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="53644-138">Especifica o nome da família de pacotes para aplicativos do MSIX</span><span class="sxs-lookup"><span data-stu-id="53644-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="53644-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="53644-139">-Name</span></span>
<span data-ttu-id="53644-140">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="53644-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53644-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53644-141">-ResourceGroupName</span></span>
<span data-ttu-id="53644-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53644-142">The name of the resource group.</span></span>
<span data-ttu-id="53644-143">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="53644-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="53644-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="53644-144">-ShowInPortal</span></span>
<span data-ttu-id="53644-145">Especifica se o programa RemoteApp deve ser mostrado no servidor de acesso à Web da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="53644-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="53644-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53644-146">-SubscriptionId</span></span>
<span data-ttu-id="53644-147">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="53644-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="53644-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="53644-148">-Tag</span></span>
<span data-ttu-id="53644-149">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="53644-149">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53644-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53644-150">-Confirm</span></span>
<span data-ttu-id="53644-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53644-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53644-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53644-152">-WhatIf</span></span>
<span data-ttu-id="53644-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53644-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53644-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53644-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53644-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53644-155">CommonParameters</span></span>
<span data-ttu-id="53644-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53644-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53644-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53644-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53644-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53644-158">INPUTS</span></span>

### <span data-ttu-id="53644-159">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="53644-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="53644-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53644-160">OUTPUTS</span></span>

### <span data-ttu-id="53644-161">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="53644-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="53644-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53644-162">NOTES</span></span>

<span data-ttu-id="53644-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="53644-163">ALIASES</span></span>

<span data-ttu-id="53644-164">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="53644-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53644-165">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="53644-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53644-166">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53644-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53644-167">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="53644-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53644-168">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="53644-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="53644-169">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="53644-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="53644-170">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="53644-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="53644-171">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="53644-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="53644-172">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="53644-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53644-173">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="53644-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="53644-174">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53644-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="53644-175">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="53644-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="53644-176">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="53644-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="53644-177">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="53644-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="53644-178">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="53644-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="53644-179">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="53644-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="53644-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53644-180">RELATED LINKS</span></span>

