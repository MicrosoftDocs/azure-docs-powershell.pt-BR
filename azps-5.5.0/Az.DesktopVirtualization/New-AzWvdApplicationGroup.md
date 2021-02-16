---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127018"
---
# <span data-ttu-id="20c1a-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="20c1a-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="20c1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="20c1a-103">Criar ou atualizar um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="20c1a-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="20c1a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20c1a-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20c1a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="20c1a-106">Criar ou atualizar um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="20c1a-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="20c1a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="20c1a-108">Exemplo 1: Criar um Grupo de Aplicativos da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="20c1a-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="20c1a-109">Esse comando cria um Grupo de Aplicativos da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="20c1a-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="20c1a-110">Exemplo 2: Criar um Grupo de Aplicativos da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="20c1a-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="20c1a-111">Esse comando cria um Grupo de Aplicativos da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="20c1a-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="20c1a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20c1a-112">PARAMETERS</span></span>

### <span data-ttu-id="20c1a-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="20c1a-113">-ApplicationGroupType</span></span>
<span data-ttu-id="20c1a-114">Tipo de Recurso do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="20c1a-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="20c1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c1a-115">-DefaultProfile</span></span>
<span data-ttu-id="20c1a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20c1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c1a-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="20c1a-117">-Description</span></span>
<span data-ttu-id="20c1a-118">Descrição do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="20c1a-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="20c1a-119">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="20c1a-119">-FriendlyName</span></span>
<span data-ttu-id="20c1a-120">Nome amigável do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="20c1a-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="20c1a-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="20c1a-121">-HostPoolArmPath</span></span>
<span data-ttu-id="20c1a-122">Caminho de armPool do ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="20c1a-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="20c1a-123">-Local</span><span class="sxs-lookup"><span data-stu-id="20c1a-123">-Location</span></span>
<span data-ttu-id="20c1a-124">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="20c1a-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="20c1a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="20c1a-125">-Name</span></span>
<span data-ttu-id="20c1a-126">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="20c1a-126">The name of the application group</span></span>

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

### <span data-ttu-id="20c1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="20c1a-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20c1a-128">The name of the resource group.</span></span>
<span data-ttu-id="20c1a-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="20c1a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="20c1a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20c1a-130">-SubscriptionId</span></span>
<span data-ttu-id="20c1a-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="20c1a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="20c1a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="20c1a-132">-Tag</span></span>
<span data-ttu-id="20c1a-133">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="20c1a-133">Resource tags.</span></span>

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

### <span data-ttu-id="20c1a-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="20c1a-134">-Confirm</span></span>
<span data-ttu-id="20c1a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20c1a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20c1a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20c1a-136">-WhatIf</span></span>
<span data-ttu-id="20c1a-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="20c1a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20c1a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20c1a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20c1a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c1a-139">CommonParameters</span></span>
<span data-ttu-id="20c1a-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c1a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c1a-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20c1a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c1a-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="20c1a-142">INPUTS</span></span>

## <span data-ttu-id="20c1a-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="20c1a-143">OUTPUTS</span></span>

### <span data-ttu-id="20c1a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="20c1a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="20c1a-145">Notas</span><span class="sxs-lookup"><span data-stu-id="20c1a-145">NOTES</span></span>

<span data-ttu-id="20c1a-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="20c1a-146">ALIASES</span></span>

## <span data-ttu-id="20c1a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20c1a-147">RELATED LINKS</span></span>

