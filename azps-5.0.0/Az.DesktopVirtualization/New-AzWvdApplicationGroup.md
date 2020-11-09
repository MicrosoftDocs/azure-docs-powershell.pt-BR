---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280563"
---
# <span data-ttu-id="35ac9-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="35ac9-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="35ac9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="35ac9-103">Criar ou atualizar um FileApp.</span><span class="sxs-lookup"><span data-stu-id="35ac9-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="35ac9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35ac9-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35ac9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="35ac9-106">Criar ou atualizar um FileApp.</span><span class="sxs-lookup"><span data-stu-id="35ac9-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="35ac9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="35ac9-108">Exemplo 1: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="35ac9-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="35ac9-109">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35ac9-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="35ac9-110">Exemplo 2: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="35ac9-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="35ac9-111">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35ac9-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="35ac9-112">OS</span><span class="sxs-lookup"><span data-stu-id="35ac9-112">PARAMETERS</span></span>

### <span data-ttu-id="35ac9-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="35ac9-113">-ApplicationGroupType</span></span>
<span data-ttu-id="35ac9-114">Tipo de recurso do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="35ac9-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="35ac9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ac9-115">-DefaultProfile</span></span>
<span data-ttu-id="35ac9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35ac9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ac9-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="35ac9-117">-Description</span></span>
<span data-ttu-id="35ac9-118">Descrição do FileApp.</span><span class="sxs-lookup"><span data-stu-id="35ac9-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="35ac9-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="35ac9-119">-FriendlyName</span></span>
<span data-ttu-id="35ac9-120">Nome amigável do nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35ac9-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="35ac9-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="35ac9-121">-HostPoolArmPath</span></span>
<span data-ttu-id="35ac9-122">Caminho do braço HostPool do FileApp.</span><span class="sxs-lookup"><span data-stu-id="35ac9-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="35ac9-123">-Local</span><span class="sxs-lookup"><span data-stu-id="35ac9-123">-Location</span></span>
<span data-ttu-id="35ac9-124">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="35ac9-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="35ac9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="35ac9-125">-Name</span></span>
<span data-ttu-id="35ac9-126">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="35ac9-126">The name of the application group</span></span>

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

### <span data-ttu-id="35ac9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ac9-127">-ResourceGroupName</span></span>
<span data-ttu-id="35ac9-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35ac9-128">The name of the resource group.</span></span>
<span data-ttu-id="35ac9-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="35ac9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="35ac9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35ac9-130">-SubscriptionId</span></span>
<span data-ttu-id="35ac9-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="35ac9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="35ac9-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="35ac9-132">-Tag</span></span>
<span data-ttu-id="35ac9-133">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="35ac9-133">Resource tags.</span></span>

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

### <span data-ttu-id="35ac9-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35ac9-134">-Confirm</span></span>
<span data-ttu-id="35ac9-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ac9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ac9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ac9-136">-WhatIf</span></span>
<span data-ttu-id="35ac9-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35ac9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ac9-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35ac9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ac9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ac9-139">CommonParameters</span></span>
<span data-ttu-id="35ac9-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ac9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ac9-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35ac9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ac9-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35ac9-142">INPUTS</span></span>

## <span data-ttu-id="35ac9-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35ac9-143">OUTPUTS</span></span>

### <span data-ttu-id="35ac9-144">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="35ac9-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="35ac9-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35ac9-145">NOTES</span></span>

<span data-ttu-id="35ac9-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35ac9-146">ALIASES</span></span>

## <span data-ttu-id="35ac9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35ac9-147">RELATED LINKS</span></span>

