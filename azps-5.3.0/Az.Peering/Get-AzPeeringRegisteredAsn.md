---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428860"
---
# <span data-ttu-id="763c3-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="763c3-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="763c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="763c3-102">SYNOPSIS</span></span>
<span data-ttu-id="763c3-103">Obtém o ASN registrado para o tipo de servidor de rota do Exchange Exchange tipos de pares.</span><span class="sxs-lookup"><span data-stu-id="763c3-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="763c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="763c3-104">SYNTAX</span></span>

### <span data-ttu-id="763c3-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="763c3-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="763c3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="763c3-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="763c3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="763c3-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="763c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="763c3-108">DESCRIPTION</span></span>
<span data-ttu-id="763c3-109">Obtenha ou liste uma ASN registrada.</span><span class="sxs-lookup"><span data-stu-id="763c3-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="763c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="763c3-110">EXAMPLES</span></span>

### <span data-ttu-id="763c3-111">Lista ASNs registrada para emparelhamento</span><span class="sxs-lookup"><span data-stu-id="763c3-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="763c3-112">Listar a ASN registrada.</span><span class="sxs-lookup"><span data-stu-id="763c3-112">Lists registered asn.</span></span>

### <span data-ttu-id="763c3-113">Recebe a ASN registrada para emparelhamento por nome</span><span class="sxs-lookup"><span data-stu-id="763c3-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="763c3-114">É um ASN de emparelhamento registrado.</span><span class="sxs-lookup"><span data-stu-id="763c3-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="763c3-115">OS</span><span class="sxs-lookup"><span data-stu-id="763c3-115">PARAMETERS</span></span>

### <span data-ttu-id="763c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763c3-116">-DefaultProfile</span></span>
<span data-ttu-id="763c3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="763c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="763c3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="763c3-118">-InputObject</span></span>
<span data-ttu-id="763c3-119">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="763c3-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="763c3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="763c3-120">-Name</span></span>
<span data-ttu-id="763c3-121">O nome da ASN registrada</span><span class="sxs-lookup"><span data-stu-id="763c3-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="763c3-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="763c3-122">-PeeringName</span></span>
<span data-ttu-id="763c3-123">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="763c3-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="763c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="763c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="763c3-125">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="763c3-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="763c3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="763c3-126">-ResourceId</span></span>
<span data-ttu-id="763c3-127">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="763c3-127">The resource id string name.</span></span>

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

### <span data-ttu-id="763c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763c3-128">CommonParameters</span></span>
<span data-ttu-id="763c3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="763c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763c3-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="763c3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763c3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="763c3-131">INPUTS</span></span>

### <span data-ttu-id="763c3-132">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="763c3-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="763c3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="763c3-133">System.String</span></span>

## <span data-ttu-id="763c3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="763c3-134">OUTPUTS</span></span>

### <span data-ttu-id="763c3-135">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="763c3-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="763c3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="763c3-136">NOTES</span></span>

## <span data-ttu-id="763c3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="763c3-137">RELATED LINKS</span></span>
