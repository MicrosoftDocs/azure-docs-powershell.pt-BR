---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114581"
---
# <span data-ttu-id="d8f5d-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d8f5d-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d8f5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f5d-103">Obtém ou lista o prefixo registrado para pares.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="d8f5d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8f5d-104">SYNTAX</span></span>

### <span data-ttu-id="d8f5d-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8f5d-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f5d-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8f5d-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f5d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f5d-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8f5d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8f5d-108">DESCRIPTION</span></span>
<span data-ttu-id="d8f5d-109">Obtém ou lista o prefixo registrado para pares.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="d8f5d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8f5d-110">EXAMPLES</span></span>

### <span data-ttu-id="d8f5d-111">Lista de ASNs registradas para peering</span><span class="sxs-lookup"><span data-stu-id="d8f5d-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="d8f5d-112">Listas registradas.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-112">Lists registered asn.</span></span>

### <span data-ttu-id="d8f5d-113">É registrada COMON para o peering por nome</span><span class="sxs-lookup"><span data-stu-id="d8f5d-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="d8f5d-114">É registrada a asn de par.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-114">Gets registered peering asn.</span></span>

<span data-ttu-id="d8f5d-115">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="d8f5d-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="d8f5d-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8f5d-116">PARAMETERS</span></span>

### <span data-ttu-id="d8f5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f5d-117">-DefaultProfile</span></span>
<span data-ttu-id="d8f5d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f5d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f5d-119">-InputObject</span></span>
<span data-ttu-id="d8f5d-120">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d8f5d-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="d8f5d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8f5d-121">-Name</span></span>
<span data-ttu-id="d8f5d-122">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-122">The name of prefix.</span></span>

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

### <span data-ttu-id="d8f5d-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d8f5d-123">-PeeringName</span></span>
<span data-ttu-id="d8f5d-124">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="d8f5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8f5d-126">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d8f5d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f5d-127">-ResourceId</span></span>
<span data-ttu-id="d8f5d-128">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-128">The resource id string name.</span></span>

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

### <span data-ttu-id="d8f5d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f5d-129">CommonParameters</span></span>
<span data-ttu-id="d8f5d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f5d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f5d-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f5d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f5d-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8f5d-132">INPUTS</span></span>

### <span data-ttu-id="d8f5d-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="d8f5d-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="d8f5d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d8f5d-134">System.String</span></span>

## <span data-ttu-id="d8f5d-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8f5d-135">OUTPUTS</span></span>

### <span data-ttu-id="d8f5d-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d8f5d-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d8f5d-137">Notas</span><span class="sxs-lookup"><span data-stu-id="d8f5d-137">NOTES</span></span>

## <span data-ttu-id="d8f5d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8f5d-138">RELATED LINKS</span></span>
