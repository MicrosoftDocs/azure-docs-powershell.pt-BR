---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114290"
---
# <span data-ttu-id="7ba58-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7ba58-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7ba58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ba58-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba58-103">Crie prefixos registrados para objetos de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7ba58-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="7ba58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ba58-104">SYNTAX</span></span>

### <span data-ttu-id="7ba58-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ba58-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba58-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7ba58-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba58-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ba58-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ba58-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ba58-108">DESCRIPTION</span></span>
<span data-ttu-id="7ba58-109">Crie prefixos registrados para objetos de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7ba58-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="7ba58-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ba58-110">EXAMPLES</span></span>

### <span data-ttu-id="7ba58-111">Obter emparelhamento e criar um prefixo cadastrado</span><span class="sxs-lookup"><span data-stu-id="7ba58-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="7ba58-112">Obtenha a correspondência que você deseja adicionar um prefixo registrado.</span><span class="sxs-lookup"><span data-stu-id="7ba58-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="7ba58-113">Em seguida, passe isso para o commandlet.</span><span class="sxs-lookup"><span data-stu-id="7ba58-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="7ba58-114">Usar o ResourceId de emparelhamento para criar um ASN cadastrado</span><span class="sxs-lookup"><span data-stu-id="7ba58-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="7ba58-115">OS</span><span class="sxs-lookup"><span data-stu-id="7ba58-115">PARAMETERS</span></span>

### <span data-ttu-id="7ba58-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ba58-116">-AsJob</span></span>
<span data-ttu-id="7ba58-117">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7ba58-117">Run in the background.</span></span>

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

### <span data-ttu-id="7ba58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba58-118">-DefaultProfile</span></span>
<span data-ttu-id="7ba58-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba58-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ba58-120">-InputObject</span></span>
<span data-ttu-id="7ba58-121">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="7ba58-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="7ba58-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ba58-122">-Name</span></span>
<span data-ttu-id="7ba58-123">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="7ba58-123">The name of prefix.</span></span>

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

### <span data-ttu-id="7ba58-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="7ba58-124">-PeeringName</span></span>
<span data-ttu-id="7ba58-125">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7ba58-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7ba58-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7ba58-126">-Prefix</span></span>
<span data-ttu-id="7ba58-127">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="7ba58-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="7ba58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba58-128">-ResourceGroupName</span></span>
<span data-ttu-id="7ba58-129">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="7ba58-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7ba58-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ba58-130">-ResourceId</span></span>
<span data-ttu-id="7ba58-131">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7ba58-131">The resource id string name.</span></span>

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

### <span data-ttu-id="7ba58-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ba58-132">-Confirm</span></span>
<span data-ttu-id="7ba58-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba58-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ba58-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba58-134">-WhatIf</span></span>
<span data-ttu-id="7ba58-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ba58-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba58-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ba58-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ba58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba58-137">CommonParameters</span></span>
<span data-ttu-id="7ba58-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba58-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ba58-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba58-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ba58-140">INPUTS</span></span>

### <span data-ttu-id="7ba58-141">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="7ba58-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="7ba58-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7ba58-142">System.String</span></span>

## <span data-ttu-id="7ba58-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ba58-143">OUTPUTS</span></span>

### <span data-ttu-id="7ba58-144">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7ba58-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7ba58-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ba58-145">NOTES</span></span>

## <span data-ttu-id="7ba58-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ba58-146">RELATED LINKS</span></span>
