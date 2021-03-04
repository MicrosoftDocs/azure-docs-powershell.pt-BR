---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: 9335bb4c3177fa405d65038255f43dbba5fb88fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887146"
---
# <span data-ttu-id="38ec0-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="38ec0-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="38ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="38ec0-103">Criar ou atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="38ec0-103">Create or update a workspace.</span></span>

## <span data-ttu-id="38ec0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38ec0-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38ec0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="38ec0-106">Criar ou atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="38ec0-106">Create or update a workspace.</span></span>

## <span data-ttu-id="38ec0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38ec0-107">EXAMPLES</span></span>

### <span data-ttu-id="38ec0-108">Exemplo 1: Criar um Espaço de Trabalho da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="38ec0-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="38ec0-109">Este comando cria um Espaço de Trabalho da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="38ec0-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="38ec0-110">Exemplo 2: Criar um Espaço de Trabalho da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="38ec0-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="38ec0-111">Este comando cria um Espaço de Trabalho da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="38ec0-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="38ec0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38ec0-112">PARAMETERS</span></span>

### <span data-ttu-id="38ec0-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="38ec0-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="38ec0-114">Lista de Ids de recurso applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="38ec0-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="38ec0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ec0-115">-DefaultProfile</span></span>
<span data-ttu-id="38ec0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38ec0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ec0-117">-Description</span><span class="sxs-lookup"><span data-stu-id="38ec0-117">-Description</span></span>
<span data-ttu-id="38ec0-118">Descrição do Workspace.</span><span class="sxs-lookup"><span data-stu-id="38ec0-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="38ec0-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="38ec0-119">-FriendlyName</span></span>
<span data-ttu-id="38ec0-120">Nome amigável do Workspace.</span><span class="sxs-lookup"><span data-stu-id="38ec0-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="38ec0-121">-Location</span><span class="sxs-lookup"><span data-stu-id="38ec0-121">-Location</span></span>
<span data-ttu-id="38ec0-122">A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="38ec0-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="38ec0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="38ec0-123">-Name</span></span>
<span data-ttu-id="38ec0-124">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="38ec0-124">The name of the workspace</span></span>

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

### <span data-ttu-id="38ec0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ec0-125">-ResourceGroupName</span></span>
<span data-ttu-id="38ec0-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38ec0-126">The name of the resource group.</span></span>
<span data-ttu-id="38ec0-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="38ec0-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="38ec0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38ec0-128">-SubscriptionId</span></span>
<span data-ttu-id="38ec0-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="38ec0-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="38ec0-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="38ec0-130">-Tag</span></span>
<span data-ttu-id="38ec0-131">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="38ec0-131">Resource tags.</span></span>

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

### <span data-ttu-id="38ec0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38ec0-132">-Confirm</span></span>
<span data-ttu-id="38ec0-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ec0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ec0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ec0-134">-WhatIf</span></span>
<span data-ttu-id="38ec0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38ec0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ec0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38ec0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ec0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ec0-137">CommonParameters</span></span>
<span data-ttu-id="38ec0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ec0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ec0-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38ec0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ec0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38ec0-140">INPUTS</span></span>

## <span data-ttu-id="38ec0-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38ec0-141">OUTPUTS</span></span>

### <span data-ttu-id="38ec0-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="38ec0-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="38ec0-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="38ec0-143">NOTES</span></span>

<span data-ttu-id="38ec0-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="38ec0-144">ALIASES</span></span>

## <span data-ttu-id="38ec0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38ec0-145">RELATED LINKS</span></span>

