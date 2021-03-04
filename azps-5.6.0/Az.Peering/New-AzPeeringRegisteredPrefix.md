---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 212daeffe2ded2dd2571d78afe79fd238349bf3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890143"
---
# <span data-ttu-id="3d55f-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="3d55f-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="3d55f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d55f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d55f-103">Crie prefixos registrados para objetos de peering.</span><span class="sxs-lookup"><span data-stu-id="3d55f-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="3d55f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d55f-104">SYNTAX</span></span>

### <span data-ttu-id="3d55f-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d55f-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d55f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3d55f-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d55f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d55f-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d55f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d55f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d55f-109">Crie prefixos registrados para objetos de peering.</span><span class="sxs-lookup"><span data-stu-id="3d55f-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="3d55f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d55f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d55f-111">Obter peering e criar um prefixo registrado</span><span class="sxs-lookup"><span data-stu-id="3d55f-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="3d55f-112">Obter o paring que você deseja adicionar um prefixo registrado.</span><span class="sxs-lookup"><span data-stu-id="3d55f-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="3d55f-113">Em seguida, passe isso para o commandlet.</span><span class="sxs-lookup"><span data-stu-id="3d55f-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="3d55f-114">Usar resourceId de peering para criar uma asn registrada</span><span class="sxs-lookup"><span data-stu-id="3d55f-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="3d55f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d55f-115">PARAMETERS</span></span>

### <span data-ttu-id="3d55f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d55f-116">-AsJob</span></span>
<span data-ttu-id="3d55f-117">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3d55f-117">Run in the background.</span></span>

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

### <span data-ttu-id="3d55f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d55f-118">-DefaultProfile</span></span>
<span data-ttu-id="3d55f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d55f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d55f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d55f-120">-InputObject</span></span>
<span data-ttu-id="3d55f-121">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="3d55f-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d55f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3d55f-122">-Name</span></span>
<span data-ttu-id="3d55f-123">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="3d55f-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d55f-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="3d55f-124">-PeeringName</span></span>
<span data-ttu-id="3d55f-125">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3d55f-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d55f-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="3d55f-126">-Prefix</span></span>
<span data-ttu-id="3d55f-127">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="3d55f-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="3d55f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d55f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3d55f-129">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="3d55f-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d55f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d55f-130">-ResourceId</span></span>
<span data-ttu-id="3d55f-131">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="3d55f-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d55f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d55f-132">-Confirm</span></span>
<span data-ttu-id="3d55f-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d55f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d55f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d55f-134">-WhatIf</span></span>
<span data-ttu-id="3d55f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d55f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d55f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d55f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d55f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d55f-137">CommonParameters</span></span>
<span data-ttu-id="3d55f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d55f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d55f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d55f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d55f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d55f-140">INPUTS</span></span>

### <span data-ttu-id="3d55f-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="3d55f-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="3d55f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3d55f-142">System.String</span></span>

## <span data-ttu-id="3d55f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d55f-143">OUTPUTS</span></span>

### <span data-ttu-id="3d55f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="3d55f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="3d55f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d55f-145">NOTES</span></span>

## <span data-ttu-id="3d55f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d55f-146">RELATED LINKS</span></span>
