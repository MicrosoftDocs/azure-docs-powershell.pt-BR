---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127019"
---
# <span data-ttu-id="16120-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="16120-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="16120-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16120-102">SYNOPSIS</span></span>
<span data-ttu-id="16120-103">Atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-103">Update an application.</span></span>

## <span data-ttu-id="16120-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16120-104">SYNTAX</span></span>

### <span data-ttu-id="16120-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16120-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16120-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16120-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16120-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="16120-107">DESCRIPTION</span></span>
<span data-ttu-id="16120-108">Atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-108">Update an application.</span></span>

## <span data-ttu-id="16120-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16120-109">EXAMPLES</span></span>

### <span data-ttu-id="16120-110">Exemplo 1: Atualizar um aplicativo virtual da área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="16120-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="16120-111">Este comando atualiza um Aplicativo virtual da área de trabalho do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="16120-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="16120-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16120-112">PARAMETERS</span></span>

### <span data-ttu-id="16120-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="16120-113">-ApplicationType</span></span>
<span data-ttu-id="16120-114">Tipo de Recurso do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="16120-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="16120-115">-CommandLineArgument</span></span>
<span data-ttu-id="16120-116">Argumentos de Linha de Comando para Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="16120-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="16120-117">-CommandLineSetting</span></span>
<span data-ttu-id="16120-118">Especifica se este aplicativo publicado pode ser lançado com argumentos de linha de comando fornecidos pelo cliente, argumentos de linha de comando especificados no momento da publicação ou nenhum argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="16120-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="16120-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16120-119">-DefaultProfile</span></span>
<span data-ttu-id="16120-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16120-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16120-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="16120-121">-Description</span></span>
<span data-ttu-id="16120-122">Descrição do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-122">Description of Application.</span></span>

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

### <span data-ttu-id="16120-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="16120-123">-FilePath</span></span>
<span data-ttu-id="16120-124">Especifica um caminho para o arquivo executável para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="16120-125">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="16120-125">-FriendlyName</span></span>
<span data-ttu-id="16120-126">Nome amigável do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16120-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="16120-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="16120-127">-GroupName</span></span>
<span data-ttu-id="16120-128">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="16120-128">The name of the application group</span></span>

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

### <span data-ttu-id="16120-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="16120-129">-IconIndex</span></span>
<span data-ttu-id="16120-130">Índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="16120-130">Index of the icon.</span></span>

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

### <span data-ttu-id="16120-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="16120-131">-IconPath</span></span>
<span data-ttu-id="16120-132">Caminho para o ícone.</span><span class="sxs-lookup"><span data-stu-id="16120-132">Path to icon.</span></span>

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

### <span data-ttu-id="16120-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16120-133">-InputObject</span></span>
<span data-ttu-id="16120-134">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="16120-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16120-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="16120-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="16120-136">Especifica a ID do aplicativo de pacote para aplicativos MSIX</span><span class="sxs-lookup"><span data-stu-id="16120-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="16120-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="16120-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="16120-138">Especifica o nome da família de pacotes para aplicativos MSIX</span><span class="sxs-lookup"><span data-stu-id="16120-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="16120-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="16120-139">-Name</span></span>
<span data-ttu-id="16120-140">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="16120-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="16120-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16120-141">-ResourceGroupName</span></span>
<span data-ttu-id="16120-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16120-142">The name of the resource group.</span></span>
<span data-ttu-id="16120-143">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="16120-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="16120-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="16120-144">-ShowInPortal</span></span>
<span data-ttu-id="16120-145">Especifica se você deve mostrar o programa RemoteApp no servidor RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="16120-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="16120-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16120-146">-SubscriptionId</span></span>
<span data-ttu-id="16120-147">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="16120-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="16120-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="16120-148">-Tag</span></span>
<span data-ttu-id="16120-149">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="16120-149">tags to be updated</span></span>

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

### <span data-ttu-id="16120-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16120-150">-Confirm</span></span>
<span data-ttu-id="16120-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16120-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16120-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16120-152">-WhatIf</span></span>
<span data-ttu-id="16120-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16120-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16120-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16120-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16120-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16120-155">CommonParameters</span></span>
<span data-ttu-id="16120-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16120-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16120-157">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16120-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16120-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="16120-158">INPUTS</span></span>

### <span data-ttu-id="16120-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="16120-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="16120-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="16120-160">OUTPUTS</span></span>

### <span data-ttu-id="16120-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="16120-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="16120-162">Notas</span><span class="sxs-lookup"><span data-stu-id="16120-162">NOTES</span></span>

<span data-ttu-id="16120-163">Aliases</span><span class="sxs-lookup"><span data-stu-id="16120-163">ALIASES</span></span>

<span data-ttu-id="16120-164">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="16120-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16120-165">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="16120-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16120-166">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16120-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16120-167">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="16120-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16120-168">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="16120-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="16120-169">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="16120-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="16120-170">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="16120-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="16120-171">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="16120-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="16120-172">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="16120-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16120-173">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="16120-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="16120-174">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16120-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="16120-175">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="16120-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="16120-176">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="16120-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="16120-177">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="16120-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="16120-178">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="16120-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="16120-179">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="16120-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="16120-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16120-180">RELATED LINKS</span></span>

