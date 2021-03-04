---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 4218dd5441c4f580c89d770556f2d5c329cfd06c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890176"
---
# <span data-ttu-id="4ef53-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4ef53-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4ef53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef53-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef53-103">Obtém o ASN registrado para peerings de tipo de servidor de rota do exchange da Internet.</span><span class="sxs-lookup"><span data-stu-id="4ef53-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="4ef53-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ef53-104">SYNTAX</span></span>

### <span data-ttu-id="4ef53-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ef53-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ef53-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4ef53-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ef53-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ef53-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef53-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ef53-108">DESCRIPTION</span></span>
<span data-ttu-id="4ef53-109">Obter ou listar um ASN registrado.</span><span class="sxs-lookup"><span data-stu-id="4ef53-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="4ef53-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ef53-110">EXAMPLES</span></span>

### <span data-ttu-id="4ef53-111">Listar ASNs registradas para peering</span><span class="sxs-lookup"><span data-stu-id="4ef53-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="4ef53-112">Lista asn registradas.</span><span class="sxs-lookup"><span data-stu-id="4ef53-112">Lists registered asn.</span></span>

### <span data-ttu-id="4ef53-113">Obtém ASN registrado para peering by name</span><span class="sxs-lookup"><span data-stu-id="4ef53-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="4ef53-114">Obtém asn de paração registrada.</span><span class="sxs-lookup"><span data-stu-id="4ef53-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="4ef53-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ef53-115">PARAMETERS</span></span>

### <span data-ttu-id="4ef53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef53-116">-DefaultProfile</span></span>
<span data-ttu-id="4ef53-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ef53-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ef53-118">-InputObject</span></span>
<span data-ttu-id="4ef53-119">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4ef53-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef53-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4ef53-120">-Name</span></span>
<span data-ttu-id="4ef53-121">O nome do ASN registrado</span><span class="sxs-lookup"><span data-stu-id="4ef53-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef53-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="4ef53-122">-PeeringName</span></span>
<span data-ttu-id="4ef53-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="4ef53-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4ef53-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef53-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ef53-125">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="4ef53-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4ef53-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ef53-126">-ResourceId</span></span>
<span data-ttu-id="4ef53-127">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="4ef53-127">The resource id string name.</span></span>

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

### <span data-ttu-id="4ef53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef53-128">CommonParameters</span></span>
<span data-ttu-id="4ef53-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef53-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ef53-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef53-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ef53-131">INPUTS</span></span>

### <span data-ttu-id="4ef53-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="4ef53-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="4ef53-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4ef53-133">System.String</span></span>

## <span data-ttu-id="4ef53-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ef53-134">OUTPUTS</span></span>

### <span data-ttu-id="4ef53-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4ef53-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4ef53-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ef53-136">NOTES</span></span>

## <span data-ttu-id="4ef53-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ef53-137">RELATED LINKS</span></span>
