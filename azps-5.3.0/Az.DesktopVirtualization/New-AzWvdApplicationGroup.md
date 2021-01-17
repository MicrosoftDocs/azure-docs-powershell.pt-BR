---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429430"
---
# <span data-ttu-id="48cf1-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="48cf1-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="48cf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="48cf1-103">Criar ou atualizar um FileApp.</span><span class="sxs-lookup"><span data-stu-id="48cf1-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="48cf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48cf1-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48cf1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="48cf1-106">Criar ou atualizar um FileApp.</span><span class="sxs-lookup"><span data-stu-id="48cf1-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="48cf1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48cf1-107">EXAMPLES</span></span>

### <span data-ttu-id="48cf1-108">Exemplo 1: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="48cf1-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="48cf1-109">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48cf1-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="48cf1-110">Exemplo 2: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="48cf1-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="48cf1-111">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48cf1-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="48cf1-112">OS</span><span class="sxs-lookup"><span data-stu-id="48cf1-112">PARAMETERS</span></span>

### <span data-ttu-id="48cf1-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="48cf1-113">-ApplicationGroupType</span></span>
<span data-ttu-id="48cf1-114">Tipo de recurso do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="48cf1-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="48cf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cf1-115">-DefaultProfile</span></span>
<span data-ttu-id="48cf1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48cf1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cf1-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="48cf1-117">-Description</span></span>
<span data-ttu-id="48cf1-118">Descrição do FileApp.</span><span class="sxs-lookup"><span data-stu-id="48cf1-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="48cf1-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="48cf1-119">-FriendlyName</span></span>
<span data-ttu-id="48cf1-120">Nome amigável do nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48cf1-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="48cf1-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="48cf1-121">-HostPoolArmPath</span></span>
<span data-ttu-id="48cf1-122">Caminho do braço HostPool do FileApp.</span><span class="sxs-lookup"><span data-stu-id="48cf1-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="48cf1-123">-Local</span><span class="sxs-lookup"><span data-stu-id="48cf1-123">-Location</span></span>
<span data-ttu-id="48cf1-124">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="48cf1-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="48cf1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="48cf1-125">-Name</span></span>
<span data-ttu-id="48cf1-126">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="48cf1-126">The name of the application group</span></span>

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

### <span data-ttu-id="48cf1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cf1-127">-ResourceGroupName</span></span>
<span data-ttu-id="48cf1-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48cf1-128">The name of the resource group.</span></span>
<span data-ttu-id="48cf1-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="48cf1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="48cf1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48cf1-130">-SubscriptionId</span></span>
<span data-ttu-id="48cf1-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="48cf1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="48cf1-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="48cf1-132">-Tag</span></span>
<span data-ttu-id="48cf1-133">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="48cf1-133">Resource tags.</span></span>

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

### <span data-ttu-id="48cf1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48cf1-134">-Confirm</span></span>
<span data-ttu-id="48cf1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48cf1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48cf1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48cf1-136">-WhatIf</span></span>
<span data-ttu-id="48cf1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48cf1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48cf1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48cf1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48cf1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cf1-139">CommonParameters</span></span>
<span data-ttu-id="48cf1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48cf1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cf1-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48cf1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cf1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48cf1-142">INPUTS</span></span>

## <span data-ttu-id="48cf1-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48cf1-143">OUTPUTS</span></span>

### <span data-ttu-id="48cf1-144">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="48cf1-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="48cf1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48cf1-145">NOTES</span></span>

<span data-ttu-id="48cf1-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="48cf1-146">ALIASES</span></span>

## <span data-ttu-id="48cf1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48cf1-147">RELATED LINKS</span></span>

