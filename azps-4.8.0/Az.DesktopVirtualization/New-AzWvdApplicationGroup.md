---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112262"
---
# <span data-ttu-id="d7b0f-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="d7b0f-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="d7b0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b0f-103">Criar ou atualizar um FileApp.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="d7b0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7b0f-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7b0f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b0f-106">Criar ou atualizar um FileApp.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="d7b0f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b0f-108">Exemplo 1: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="d7b0f-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="d7b0f-109">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="d7b0f-110">Exemplo 2: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="d7b0f-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="d7b0f-111">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="d7b0f-112">OS</span><span class="sxs-lookup"><span data-stu-id="d7b0f-112">PARAMETERS</span></span>

### <span data-ttu-id="d7b0f-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="d7b0f-113">-ApplicationGroupType</span></span>
<span data-ttu-id="d7b0f-114">Tipo de recurso do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="d7b0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b0f-115">-DefaultProfile</span></span>
<span data-ttu-id="d7b0f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b0f-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b0f-117">-Description</span></span>
<span data-ttu-id="d7b0f-118">Descrição do FileApp.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="d7b0f-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d7b0f-119">-FriendlyName</span></span>
<span data-ttu-id="d7b0f-120">Nome amigável do nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="d7b0f-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="d7b0f-121">-HostPoolArmPath</span></span>
<span data-ttu-id="d7b0f-122">Caminho do braço HostPool do FileApp.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="d7b0f-123">-Local</span><span class="sxs-lookup"><span data-stu-id="d7b0f-123">-Location</span></span>
<span data-ttu-id="d7b0f-124">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="d7b0f-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d7b0f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7b0f-125">-Name</span></span>
<span data-ttu-id="d7b0f-126">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d7b0f-126">The name of the application group</span></span>

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

### <span data-ttu-id="d7b0f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b0f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7b0f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-128">The name of the resource group.</span></span>
<span data-ttu-id="d7b0f-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d7b0f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7b0f-130">-SubscriptionId</span></span>
<span data-ttu-id="d7b0f-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d7b0f-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="d7b0f-132">-Tag</span></span>
<span data-ttu-id="d7b0f-133">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-133">Resource tags.</span></span>

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

### <span data-ttu-id="d7b0f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7b0f-134">-Confirm</span></span>
<span data-ttu-id="d7b0f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b0f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b0f-136">-WhatIf</span></span>
<span data-ttu-id="d7b0f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b0f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b0f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b0f-139">CommonParameters</span></span>
<span data-ttu-id="d7b0f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b0f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b0f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7b0f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b0f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7b0f-142">INPUTS</span></span>

## <span data-ttu-id="d7b0f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7b0f-143">OUTPUTS</span></span>

### <span data-ttu-id="d7b0f-144">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="d7b0f-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="d7b0f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7b0f-145">NOTES</span></span>

<span data-ttu-id="d7b0f-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d7b0f-146">ALIASES</span></span>

## <span data-ttu-id="d7b0f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7b0f-147">RELATED LINKS</span></span>

