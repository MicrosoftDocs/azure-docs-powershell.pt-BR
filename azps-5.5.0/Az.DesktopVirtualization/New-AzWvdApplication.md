---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115827"
---
# <span data-ttu-id="a61df-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a61df-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="a61df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a61df-102">SYNOPSIS</span></span>
<span data-ttu-id="a61df-103">Criar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-103">Create or update an application.</span></span>

## <span data-ttu-id="a61df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a61df-104">SYNTAX</span></span>

### <span data-ttu-id="a61df-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="a61df-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a61df-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="a61df-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a61df-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a61df-107">DESCRIPTION</span></span>
<span data-ttu-id="a61df-108">Criar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-108">Create or update an application.</span></span>

## <span data-ttu-id="a61df-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a61df-109">EXAMPLES</span></span>

### <span data-ttu-id="a61df-110">Exemplo 1: Criar um aplicativo virtual da área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="a61df-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="a61df-111">Esse comando cria um Aplicativo virtual da área de trabalho do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a61df-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a61df-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a61df-112">PARAMETERS</span></span>

### <span data-ttu-id="a61df-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="a61df-113">-AppAlias</span></span>
<span data-ttu-id="a61df-114">Alias do Aplicativo no item do menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="a61df-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="a61df-115">-ApplicationType</span></span>
<span data-ttu-id="a61df-116">Tipo de Recurso do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="a61df-117">-CommandLineArgument</span></span>
<span data-ttu-id="a61df-118">Argumentos de Linha de Comando para Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-118">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="a61df-119">-CommandLineSetting</span></span>
<span data-ttu-id="a61df-120">Especifica se este aplicativo publicado pode ser lançado com argumentos de linha de comando fornecidos pelo cliente, argumentos de linha de comando especificados no momento da publicação ou nenhum argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a61df-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61df-121">-DefaultProfile</span></span>
<span data-ttu-id="a61df-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a61df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a61df-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a61df-123">-Description</span></span>
<span data-ttu-id="a61df-124">Descrição do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-124">Description of Application.</span></span>

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

### <span data-ttu-id="a61df-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a61df-125">-FilePath</span></span>
<span data-ttu-id="a61df-126">Especifica um caminho para o arquivo executável para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-126">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-127">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="a61df-127">-FriendlyName</span></span>
<span data-ttu-id="a61df-128">Nome amigável do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a61df-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="a61df-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a61df-129">-GroupName</span></span>
<span data-ttu-id="a61df-130">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a61df-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="a61df-131">-IconIndex</span></span>
<span data-ttu-id="a61df-132">Índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="a61df-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="a61df-133">-IconPath</span></span>
<span data-ttu-id="a61df-134">Caminho para o ícone.</span><span class="sxs-lookup"><span data-stu-id="a61df-134">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="a61df-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="a61df-136">Especifica a ID do aplicativo de pacote para aplicativos MSIX</span><span class="sxs-lookup"><span data-stu-id="a61df-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="a61df-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="a61df-138">Especifica o nome da família de pacotes para aplicativos MSIX</span><span class="sxs-lookup"><span data-stu-id="a61df-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a61df-139">-Name</span></span>
<span data-ttu-id="a61df-140">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a61df-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a61df-141">-ResourceGroupName</span></span>
<span data-ttu-id="a61df-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a61df-142">The name of the resource group.</span></span>
<span data-ttu-id="a61df-143">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a61df-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="a61df-144">-ShowInPortal</span></span>
<span data-ttu-id="a61df-145">Especifica se você deve mostrar o programa RemoteApp no servidor RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="a61df-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="a61df-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a61df-146">-SubscriptionId</span></span>
<span data-ttu-id="a61df-147">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a61df-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61df-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a61df-148">-Confirm</span></span>
<span data-ttu-id="a61df-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a61df-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a61df-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a61df-150">-WhatIf</span></span>
<span data-ttu-id="a61df-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a61df-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a61df-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a61df-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a61df-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61df-153">CommonParameters</span></span>
<span data-ttu-id="a61df-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a61df-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61df-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a61df-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61df-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="a61df-156">INPUTS</span></span>

## <span data-ttu-id="a61df-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="a61df-157">OUTPUTS</span></span>

### <span data-ttu-id="a61df-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="a61df-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="a61df-159">Notas</span><span class="sxs-lookup"><span data-stu-id="a61df-159">NOTES</span></span>

<span data-ttu-id="a61df-160">Aliases</span><span class="sxs-lookup"><span data-stu-id="a61df-160">ALIASES</span></span>

## <span data-ttu-id="a61df-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a61df-161">RELATED LINKS</span></span>

