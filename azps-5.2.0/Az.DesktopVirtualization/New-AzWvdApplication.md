---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 724e1877b924829560112f926b75bd1c523c8f18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259614"
---
# <span data-ttu-id="a05d3-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a05d3-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="a05d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a05d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a05d3-103">Criar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-103">Create or update an application.</span></span>

## <span data-ttu-id="a05d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a05d3-104">SYNTAX</span></span>

### <span data-ttu-id="a05d3-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a05d3-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a05d3-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="a05d3-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a05d3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a05d3-107">DESCRIPTION</span></span>
<span data-ttu-id="a05d3-108">Criar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-108">Create or update an application.</span></span>

## <span data-ttu-id="a05d3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a05d3-109">EXAMPLES</span></span>

### <span data-ttu-id="a05d3-110">Exemplo 1: criar um aplicativo de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="a05d3-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="a05d3-111">Esse comando cria um aplicativo de área de trabalho virtual do Windows em um grupo applicaton.</span><span class="sxs-lookup"><span data-stu-id="a05d3-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a05d3-112">OS</span><span class="sxs-lookup"><span data-stu-id="a05d3-112">PARAMETERS</span></span>

### <span data-ttu-id="a05d3-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="a05d3-113">-AppAlias</span></span>
<span data-ttu-id="a05d3-114">Alias do aplicativo do item do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="a05d3-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="a05d3-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="a05d3-115">-ApplicationType</span></span>
<span data-ttu-id="a05d3-116">Tipo de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="a05d3-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="a05d3-117">-CommandLineArgument</span></span>
<span data-ttu-id="a05d3-118">Argumentos de linha de comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="a05d3-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="a05d3-119">-CommandLineSetting</span></span>
<span data-ttu-id="a05d3-120">Especifica se esse aplicativo publicado pode ser iniciado com argumentos de linha de comando fornecidos pelo cliente, argumentos de linha de comando especificados no tempo de publicação ou nenhum argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a05d3-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="a05d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05d3-121">-DefaultProfile</span></span>
<span data-ttu-id="a05d3-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a05d3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05d3-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a05d3-123">-Description</span></span>
<span data-ttu-id="a05d3-124">Descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-124">Description of Application.</span></span>

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

### <span data-ttu-id="a05d3-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a05d3-125">-FilePath</span></span>
<span data-ttu-id="a05d3-126">Especifica um caminho para o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="a05d3-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a05d3-127">-FriendlyName</span></span>
<span data-ttu-id="a05d3-128">Nome amigável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a05d3-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="a05d3-129">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="a05d3-129">-GroupName</span></span>
<span data-ttu-id="a05d3-130">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a05d3-130">The name of the application group</span></span>

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

### <span data-ttu-id="a05d3-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="a05d3-131">-IconIndex</span></span>
<span data-ttu-id="a05d3-132">Índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="a05d3-132">Index of the icon.</span></span>

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

### <span data-ttu-id="a05d3-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="a05d3-133">-IconPath</span></span>
<span data-ttu-id="a05d3-134">Caminho para o ícone.</span><span class="sxs-lookup"><span data-stu-id="a05d3-134">Path to icon.</span></span>

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

### <span data-ttu-id="a05d3-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="a05d3-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="a05d3-136">Especifica a ID do aplicativo do pacote para aplicativos MSIX</span><span class="sxs-lookup"><span data-stu-id="a05d3-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="a05d3-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="a05d3-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="a05d3-138">Especifica o nome da família de pacotes para aplicativos do MSIX</span><span class="sxs-lookup"><span data-stu-id="a05d3-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="a05d3-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a05d3-139">-Name</span></span>
<span data-ttu-id="a05d3-140">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a05d3-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="a05d3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05d3-141">-ResourceGroupName</span></span>
<span data-ttu-id="a05d3-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a05d3-142">The name of the resource group.</span></span>
<span data-ttu-id="a05d3-143">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a05d3-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a05d3-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="a05d3-144">-ShowInPortal</span></span>
<span data-ttu-id="a05d3-145">Especifica se o programa RemoteApp deve ser mostrado no servidor de acesso à Web da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="a05d3-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="a05d3-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a05d3-146">-SubscriptionId</span></span>
<span data-ttu-id="a05d3-147">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a05d3-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a05d3-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a05d3-148">-Confirm</span></span>
<span data-ttu-id="a05d3-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a05d3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05d3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05d3-150">-WhatIf</span></span>
<span data-ttu-id="a05d3-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a05d3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05d3-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a05d3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05d3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05d3-153">CommonParameters</span></span>
<span data-ttu-id="a05d3-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05d3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05d3-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a05d3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05d3-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a05d3-156">INPUTS</span></span>

## <span data-ttu-id="a05d3-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a05d3-157">OUTPUTS</span></span>

### <span data-ttu-id="a05d3-158">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="a05d3-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="a05d3-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a05d3-159">NOTES</span></span>

<span data-ttu-id="a05d3-160">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a05d3-160">ALIASES</span></span>

## <span data-ttu-id="a05d3-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a05d3-161">RELATED LINKS</span></span>

