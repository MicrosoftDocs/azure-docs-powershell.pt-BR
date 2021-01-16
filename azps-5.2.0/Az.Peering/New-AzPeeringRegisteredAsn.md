---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260609"
---
# <span data-ttu-id="02ddf-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="02ddf-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="02ddf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="02ddf-103">Criar a ASN registrada para emparelhamento</span><span class="sxs-lookup"><span data-stu-id="02ddf-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="02ddf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02ddf-104">SYNTAX</span></span>

### <span data-ttu-id="02ddf-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="02ddf-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ddf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="02ddf-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ddf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02ddf-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ddf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="02ddf-109">Crie ASNs registrados para objetos de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="02ddf-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="02ddf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="02ddf-111">Obtenha correspondência e crie um ASN cadastrado</span><span class="sxs-lookup"><span data-stu-id="02ddf-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="02ddf-112">Obtenha a correspondência que você deseja adicionar à ASN registrada.</span><span class="sxs-lookup"><span data-stu-id="02ddf-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="02ddf-113">Em seguida, passe isso para o commandlet.</span><span class="sxs-lookup"><span data-stu-id="02ddf-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="02ddf-114">Usar o ResourceId de emparelhamento para criar um ASN cadastrado</span><span class="sxs-lookup"><span data-stu-id="02ddf-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="02ddf-115">OS</span><span class="sxs-lookup"><span data-stu-id="02ddf-115">PARAMETERS</span></span>

### <span data-ttu-id="02ddf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ddf-116">-AsJob</span></span>
<span data-ttu-id="02ddf-117">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="02ddf-117">Run in the background.</span></span>

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

### <span data-ttu-id="02ddf-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="02ddf-118">-Asn</span></span>
<span data-ttu-id="02ddf-119">A ASN a ser registrada</span><span class="sxs-lookup"><span data-stu-id="02ddf-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ddf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ddf-120">-DefaultProfile</span></span>
<span data-ttu-id="02ddf-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02ddf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ddf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02ddf-122">-InputObject</span></span>
<span data-ttu-id="02ddf-123">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="02ddf-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="02ddf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="02ddf-124">-Name</span></span>
<span data-ttu-id="02ddf-125">A ASN a ser registrada</span><span class="sxs-lookup"><span data-stu-id="02ddf-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="02ddf-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="02ddf-126">-PeeringName</span></span>
<span data-ttu-id="02ddf-127">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="02ddf-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="02ddf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ddf-128">-ResourceGroupName</span></span>
<span data-ttu-id="02ddf-129">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="02ddf-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="02ddf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ddf-130">-ResourceId</span></span>
<span data-ttu-id="02ddf-131">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="02ddf-131">The resource id string name.</span></span>

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

### <span data-ttu-id="02ddf-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02ddf-132">-Confirm</span></span>
<span data-ttu-id="02ddf-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ddf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ddf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ddf-134">-WhatIf</span></span>
<span data-ttu-id="02ddf-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02ddf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ddf-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02ddf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ddf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ddf-137">CommonParameters</span></span>
<span data-ttu-id="02ddf-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ddf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ddf-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ddf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ddf-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02ddf-140">INPUTS</span></span>

### <span data-ttu-id="02ddf-141">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="02ddf-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="02ddf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="02ddf-142">System.String</span></span>

## <span data-ttu-id="02ddf-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02ddf-143">OUTPUTS</span></span>

### <span data-ttu-id="02ddf-144">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="02ddf-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="02ddf-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02ddf-145">NOTES</span></span>

## <span data-ttu-id="02ddf-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02ddf-146">RELATED LINKS</span></span>
