---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117289"
---
# <span data-ttu-id="1350d-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="1350d-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="1350d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1350d-102">SYNOPSIS</span></span>
<span data-ttu-id="1350d-103">Obtém o ASN registrado para os pares de servidor de rota de troca de internet.</span><span class="sxs-lookup"><span data-stu-id="1350d-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="1350d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1350d-104">SYNTAX</span></span>

### <span data-ttu-id="1350d-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1350d-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1350d-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1350d-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1350d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1350d-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1350d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1350d-108">DESCRIPTION</span></span>
<span data-ttu-id="1350d-109">Obter ou listar uma ASN registrada.</span><span class="sxs-lookup"><span data-stu-id="1350d-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="1350d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1350d-110">EXAMPLES</span></span>

### <span data-ttu-id="1350d-111">Lista de ASNs registradas para peering</span><span class="sxs-lookup"><span data-stu-id="1350d-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="1350d-112">Listas registradas.</span><span class="sxs-lookup"><span data-stu-id="1350d-112">Lists registered asn.</span></span>

### <span data-ttu-id="1350d-113">É registrada COMON para o peering por nome</span><span class="sxs-lookup"><span data-stu-id="1350d-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="1350d-114">É registrada a asn de par.</span><span class="sxs-lookup"><span data-stu-id="1350d-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="1350d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1350d-115">PARAMETERS</span></span>

### <span data-ttu-id="1350d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1350d-116">-DefaultProfile</span></span>
<span data-ttu-id="1350d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1350d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1350d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1350d-118">-InputObject</span></span>
<span data-ttu-id="1350d-119">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="1350d-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="1350d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1350d-120">-Name</span></span>
<span data-ttu-id="1350d-121">O nome da ASN registrada</span><span class="sxs-lookup"><span data-stu-id="1350d-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="1350d-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="1350d-122">-PeeringName</span></span>
<span data-ttu-id="1350d-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1350d-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1350d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1350d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1350d-125">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="1350d-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1350d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1350d-126">-ResourceId</span></span>
<span data-ttu-id="1350d-127">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1350d-127">The resource id string name.</span></span>

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

### <span data-ttu-id="1350d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1350d-128">CommonParameters</span></span>
<span data-ttu-id="1350d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1350d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1350d-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1350d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1350d-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="1350d-131">INPUTS</span></span>

### <span data-ttu-id="1350d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="1350d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="1350d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1350d-133">System.String</span></span>

## <span data-ttu-id="1350d-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1350d-134">OUTPUTS</span></span>

### <span data-ttu-id="1350d-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="1350d-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="1350d-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1350d-136">NOTES</span></span>

## <span data-ttu-id="1350d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1350d-137">RELATED LINKS</span></span>
