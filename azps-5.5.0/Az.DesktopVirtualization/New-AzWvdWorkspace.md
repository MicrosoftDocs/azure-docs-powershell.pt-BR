---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117698"
---
# <span data-ttu-id="bb773-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="bb773-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="bb773-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb773-102">SYNOPSIS</span></span>
<span data-ttu-id="bb773-103">Criar ou atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb773-103">Create or update a workspace.</span></span>

## <span data-ttu-id="bb773-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb773-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb773-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb773-105">DESCRIPTION</span></span>
<span data-ttu-id="bb773-106">Criar ou atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb773-106">Create or update a workspace.</span></span>

## <span data-ttu-id="bb773-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb773-107">EXAMPLES</span></span>

### <span data-ttu-id="bb773-108">Exemplo 1: Criar um Espaço de Trabalho virtual da área de trabalho do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="bb773-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="bb773-109">Esse comando cria um Espaço de Trabalho virtual da área de trabalho do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="bb773-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="bb773-110">Exemplo 2: Criar um Espaço de Trabalho virtual da área de trabalho do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="bb773-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="bb773-111">Esse comando cria um Espaço de Trabalho virtual da área de trabalho do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="bb773-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="bb773-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb773-112">PARAMETERS</span></span>

### <span data-ttu-id="bb773-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="bb773-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="bb773-114">Lista de Ids de recursos do applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bb773-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb773-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb773-115">-DefaultProfile</span></span>
<span data-ttu-id="bb773-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb773-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb773-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bb773-117">-Description</span></span>
<span data-ttu-id="bb773-118">Descrição do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb773-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="bb773-119">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="bb773-119">-FriendlyName</span></span>
<span data-ttu-id="bb773-120">Nome amigável do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb773-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="bb773-121">-Local</span><span class="sxs-lookup"><span data-stu-id="bb773-121">-Location</span></span>
<span data-ttu-id="bb773-122">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="bb773-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="bb773-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb773-123">-Name</span></span>
<span data-ttu-id="bb773-124">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bb773-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb773-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb773-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb773-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb773-126">The name of the resource group.</span></span>
<span data-ttu-id="bb773-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bb773-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bb773-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb773-128">-SubscriptionId</span></span>
<span data-ttu-id="bb773-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="bb773-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bb773-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb773-130">-Tag</span></span>
<span data-ttu-id="bb773-131">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="bb773-131">Resource tags.</span></span>

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

### <span data-ttu-id="bb773-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bb773-132">-Confirm</span></span>
<span data-ttu-id="bb773-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb773-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb773-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb773-134">-WhatIf</span></span>
<span data-ttu-id="bb773-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bb773-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb773-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb773-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb773-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb773-137">CommonParameters</span></span>
<span data-ttu-id="bb773-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb773-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb773-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb773-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb773-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb773-140">INPUTS</span></span>

## <span data-ttu-id="bb773-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb773-141">OUTPUTS</span></span>

### <span data-ttu-id="bb773-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="bb773-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="bb773-143">Notas</span><span class="sxs-lookup"><span data-stu-id="bb773-143">NOTES</span></span>

<span data-ttu-id="bb773-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="bb773-144">ALIASES</span></span>

## <span data-ttu-id="bb773-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb773-145">RELATED LINKS</span></span>

