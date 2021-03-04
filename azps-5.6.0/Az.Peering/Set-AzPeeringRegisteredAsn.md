---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: b4533497c1be0fd42e70cc0b7636aa2d4d5a7a98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890123"
---
# <span data-ttu-id="4a44e-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4a44e-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4a44e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a44e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a44e-103">Define ou atualiza um ASN registrado do recurso de paração pai.</span><span class="sxs-lookup"><span data-stu-id="4a44e-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="4a44e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4a44e-104">SYNTAX</span></span>

### <span data-ttu-id="4a44e-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4a44e-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a44e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4a44e-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a44e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a44e-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a44e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4a44e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a44e-109">Permite a atualização de um ASN registrado a partir do recurso de paração pai.</span><span class="sxs-lookup"><span data-stu-id="4a44e-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="4a44e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a44e-110">EXAMPLES</span></span>

### <span data-ttu-id="4a44e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a44e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="4a44e-112">Atualiza o ASN por id de recurso.</span><span class="sxs-lookup"><span data-stu-id="4a44e-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="4a44e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4a44e-113">PARAMETERS</span></span>

### <span data-ttu-id="4a44e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a44e-114">-AsJob</span></span>
<span data-ttu-id="4a44e-115">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4a44e-115">Run in the background.</span></span>

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

### <span data-ttu-id="4a44e-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="4a44e-116">-Asn</span></span>
<span data-ttu-id="4a44e-117">O ASN a ser registrado</span><span class="sxs-lookup"><span data-stu-id="4a44e-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="4a44e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a44e-118">-DefaultProfile</span></span>
<span data-ttu-id="4a44e-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a44e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a44e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a44e-120">-InputObject</span></span>
<span data-ttu-id="4a44e-121">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4a44e-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a44e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4a44e-122">-Name</span></span>
<span data-ttu-id="4a44e-123">O ASN a ser registrado</span><span class="sxs-lookup"><span data-stu-id="4a44e-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a44e-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="4a44e-124">-PeeringName</span></span>
<span data-ttu-id="4a44e-125">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="4a44e-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4a44e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a44e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4a44e-127">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="4a44e-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4a44e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a44e-128">-ResourceId</span></span>
<span data-ttu-id="4a44e-129">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="4a44e-129">The resource id string name.</span></span>

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

### <span data-ttu-id="4a44e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a44e-130">-Confirm</span></span>
<span data-ttu-id="4a44e-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a44e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a44e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a44e-132">-WhatIf</span></span>
<span data-ttu-id="4a44e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a44e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a44e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a44e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a44e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a44e-135">CommonParameters</span></span>
<span data-ttu-id="4a44e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a44e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a44e-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a44e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a44e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a44e-138">INPUTS</span></span>

### <span data-ttu-id="4a44e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4a44e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="4a44e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4a44e-140">System.String</span></span>

## <span data-ttu-id="4a44e-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4a44e-141">OUTPUTS</span></span>

### <span data-ttu-id="4a44e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4a44e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4a44e-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="4a44e-143">NOTES</span></span>

## <span data-ttu-id="4a44e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a44e-144">RELATED LINKS</span></span>
