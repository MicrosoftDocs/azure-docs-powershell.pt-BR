---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115012"
---
# <span data-ttu-id="0320e-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="0320e-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="0320e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0320e-102">SYNOPSIS</span></span>
<span data-ttu-id="0320e-103">Criar ou atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0320e-103">Create or update a workspace.</span></span>

## <span data-ttu-id="0320e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0320e-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0320e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0320e-105">DESCRIPTION</span></span>
<span data-ttu-id="0320e-106">Criar ou atualizar um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0320e-106">Create or update a workspace.</span></span>

## <span data-ttu-id="0320e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0320e-107">EXAMPLES</span></span>

### <span data-ttu-id="0320e-108">Exemplo 1: criar um Worksapce de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="0320e-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="0320e-109">Esse comando cria um espaço de trabalho de área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0320e-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="0320e-110">Exemplo 2: criar um Worksapce de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="0320e-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="0320e-111">Esse comando cria um espaço de trabalho de área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0320e-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="0320e-112">OS</span><span class="sxs-lookup"><span data-stu-id="0320e-112">PARAMETERS</span></span>

### <span data-ttu-id="0320e-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="0320e-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="0320e-114">Lista de IDs de recursos de pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0320e-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="0320e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0320e-115">-DefaultProfile</span></span>
<span data-ttu-id="0320e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0320e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0320e-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0320e-117">-Description</span></span>
<span data-ttu-id="0320e-118">Descrição do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0320e-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="0320e-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0320e-119">-FriendlyName</span></span>
<span data-ttu-id="0320e-120">Nome amigável do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0320e-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="0320e-121">-Local</span><span class="sxs-lookup"><span data-stu-id="0320e-121">-Location</span></span>
<span data-ttu-id="0320e-122">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="0320e-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="0320e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0320e-123">-Name</span></span>
<span data-ttu-id="0320e-124">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0320e-124">The name of the workspace</span></span>

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

### <span data-ttu-id="0320e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0320e-125">-ResourceGroupName</span></span>
<span data-ttu-id="0320e-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0320e-126">The name of the resource group.</span></span>
<span data-ttu-id="0320e-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0320e-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0320e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0320e-128">-SubscriptionId</span></span>
<span data-ttu-id="0320e-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0320e-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0320e-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="0320e-130">-Tag</span></span>
<span data-ttu-id="0320e-131">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="0320e-131">Resource tags.</span></span>

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

### <span data-ttu-id="0320e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0320e-132">-Confirm</span></span>
<span data-ttu-id="0320e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0320e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0320e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0320e-134">-WhatIf</span></span>
<span data-ttu-id="0320e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0320e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0320e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0320e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0320e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0320e-137">CommonParameters</span></span>
<span data-ttu-id="0320e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0320e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0320e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0320e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0320e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0320e-140">INPUTS</span></span>

## <span data-ttu-id="0320e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0320e-141">OUTPUTS</span></span>

### <span data-ttu-id="0320e-142">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="0320e-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="0320e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0320e-143">NOTES</span></span>

<span data-ttu-id="0320e-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0320e-144">ALIASES</span></span>

## <span data-ttu-id="0320e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0320e-145">RELATED LINKS</span></span>

