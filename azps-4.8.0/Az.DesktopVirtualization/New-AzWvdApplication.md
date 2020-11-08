---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114554"
---
# <span data-ttu-id="6807e-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="6807e-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="6807e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6807e-102">SYNOPSIS</span></span>
<span data-ttu-id="6807e-103">Criar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6807e-103">Create or update an application.</span></span>

## <span data-ttu-id="6807e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6807e-104">SYNTAX</span></span>

### <span data-ttu-id="6807e-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="6807e-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6807e-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="6807e-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6807e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6807e-107">DESCRIPTION</span></span>
<span data-ttu-id="6807e-108">Criar ou atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6807e-108">Create or update an application.</span></span>

## <span data-ttu-id="6807e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6807e-109">EXAMPLES</span></span>

### <span data-ttu-id="6807e-110">Exemplo 1: criar um aplicativo de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="6807e-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="6807e-111">Esse comando cria um aplicativo de área de trabalho virtual do Windows em um grupo applicaton.</span><span class="sxs-lookup"><span data-stu-id="6807e-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="6807e-112">OS</span><span class="sxs-lookup"><span data-stu-id="6807e-112">PARAMETERS</span></span>

### <span data-ttu-id="6807e-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="6807e-113">-AppAlias</span></span>
<span data-ttu-id="6807e-114">Alias do aplicativo do item do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="6807e-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="6807e-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="6807e-115">-CommandLineArgument</span></span>
<span data-ttu-id="6807e-116">Argumentos de linha de comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6807e-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="6807e-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="6807e-117">-CommandLineSetting</span></span>
<span data-ttu-id="6807e-118">Especifica se esse aplicativo publicado pode ser iniciado com argumentos de linha de comando fornecidos pelo cliente, argumentos de linha de comando especificados no tempo de publicação ou nenhum argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="6807e-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="6807e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6807e-119">-DefaultProfile</span></span>
<span data-ttu-id="6807e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6807e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6807e-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6807e-121">-Description</span></span>
<span data-ttu-id="6807e-122">Descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6807e-122">Description of Application.</span></span>

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

### <span data-ttu-id="6807e-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="6807e-123">-FilePath</span></span>
<span data-ttu-id="6807e-124">Especifica um caminho para o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6807e-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="6807e-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6807e-125">-FriendlyName</span></span>
<span data-ttu-id="6807e-126">Nome amigável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6807e-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="6807e-127">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="6807e-127">-GroupName</span></span>
<span data-ttu-id="6807e-128">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6807e-128">The name of the application group</span></span>

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

### <span data-ttu-id="6807e-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="6807e-129">-IconIndex</span></span>
<span data-ttu-id="6807e-130">Índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="6807e-130">Index of the icon.</span></span>

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

### <span data-ttu-id="6807e-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="6807e-131">-IconPath</span></span>
<span data-ttu-id="6807e-132">Caminho para o ícone.</span><span class="sxs-lookup"><span data-stu-id="6807e-132">Path to icon.</span></span>

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

### <span data-ttu-id="6807e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="6807e-133">-Name</span></span>
<span data-ttu-id="6807e-134">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="6807e-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="6807e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6807e-135">-ResourceGroupName</span></span>
<span data-ttu-id="6807e-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6807e-136">The name of the resource group.</span></span>
<span data-ttu-id="6807e-137">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6807e-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6807e-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="6807e-138">-ShowInPortal</span></span>
<span data-ttu-id="6807e-139">Especifica se o programa RemoteApp deve ser mostrado no servidor de acesso à Web da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="6807e-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="6807e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6807e-140">-SubscriptionId</span></span>
<span data-ttu-id="6807e-141">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6807e-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6807e-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6807e-142">-Confirm</span></span>
<span data-ttu-id="6807e-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6807e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6807e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6807e-144">-WhatIf</span></span>
<span data-ttu-id="6807e-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6807e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6807e-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6807e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6807e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6807e-147">CommonParameters</span></span>
<span data-ttu-id="6807e-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6807e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6807e-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6807e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6807e-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6807e-150">INPUTS</span></span>

## <span data-ttu-id="6807e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6807e-151">OUTPUTS</span></span>

### <span data-ttu-id="6807e-152">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="6807e-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="6807e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6807e-153">NOTES</span></span>

<span data-ttu-id="6807e-154">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6807e-154">ALIASES</span></span>

## <span data-ttu-id="6807e-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6807e-155">RELATED LINKS</span></span>

