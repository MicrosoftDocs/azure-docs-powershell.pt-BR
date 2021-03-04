---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 38292351f091528ef4e153f9374dff75ccbfe941
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887155"
---
# <span data-ttu-id="a9ad6-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a9ad6-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="a9ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ad6-103">Criar ou atualizar um applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="a9ad6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9ad6-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9ad6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ad6-106">Criar ou atualizar um applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="a9ad6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ad6-108">Exemplo 1: Criar um Grupo de Aplicativos de Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="a9ad6-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="a9ad6-109">Este comando cria um Windows Virtual Desktop ApplicationGroup em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="a9ad6-110">Exemplo 2: Criar um Grupo de Aplicativos de Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="a9ad6-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="a9ad6-111">Este comando cria um Windows Virtual Desktop ApplicationGroup em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="a9ad6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="a9ad6-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="a9ad6-113">-ApplicationGroupType</span></span>
<span data-ttu-id="a9ad6-114">Tipo de recurso do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ad6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ad6-115">-DefaultProfile</span></span>
<span data-ttu-id="a9ad6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ad6-117">-Description</span><span class="sxs-lookup"><span data-stu-id="a9ad6-117">-Description</span></span>
<span data-ttu-id="a9ad6-118">Descrição do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="a9ad6-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9ad6-119">-FriendlyName</span></span>
<span data-ttu-id="a9ad6-120">Nome amigável de ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="a9ad6-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="a9ad6-121">-HostPoolArmPath</span></span>
<span data-ttu-id="a9ad6-122">Caminho do braço hostPool do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="a9ad6-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a9ad6-123">-Location</span></span>
<span data-ttu-id="a9ad6-124">A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="a9ad6-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="a9ad6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a9ad6-125">-Name</span></span>
<span data-ttu-id="a9ad6-126">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a9ad6-126">The name of the application group</span></span>

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

### <span data-ttu-id="a9ad6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ad6-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9ad6-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-128">The name of the resource group.</span></span>
<span data-ttu-id="a9ad6-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a9ad6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9ad6-130">-SubscriptionId</span></span>
<span data-ttu-id="a9ad6-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a9ad6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9ad6-132">-Tag</span></span>
<span data-ttu-id="a9ad6-133">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-133">Resource tags.</span></span>

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

### <span data-ttu-id="a9ad6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9ad6-134">-Confirm</span></span>
<span data-ttu-id="a9ad6-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ad6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ad6-136">-WhatIf</span></span>
<span data-ttu-id="a9ad6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ad6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ad6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ad6-139">CommonParameters</span></span>
<span data-ttu-id="a9ad6-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ad6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ad6-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9ad6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ad6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9ad6-142">INPUTS</span></span>

## <span data-ttu-id="a9ad6-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9ad6-143">OUTPUTS</span></span>

### <span data-ttu-id="a9ad6-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a9ad6-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="a9ad6-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9ad6-145">NOTES</span></span>

<span data-ttu-id="a9ad6-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a9ad6-146">ALIASES</span></span>

## <span data-ttu-id="a9ad6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9ad6-147">RELATED LINKS</span></span>

