---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272519"
---
# <span data-ttu-id="91d04-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="91d04-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="91d04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91d04-102">SYNOPSIS</span></span>
<span data-ttu-id="91d04-103">Define ou atualiza uma ASN registrada do recurso de emparelhamento primário.</span><span class="sxs-lookup"><span data-stu-id="91d04-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="91d04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91d04-104">SYNTAX</span></span>

### <span data-ttu-id="91d04-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="91d04-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91d04-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="91d04-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91d04-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91d04-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91d04-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91d04-108">DESCRIPTION</span></span>
<span data-ttu-id="91d04-109">Permite a atualização de um ASN registrado do recurso de emparelhamento pai.</span><span class="sxs-lookup"><span data-stu-id="91d04-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="91d04-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91d04-110">EXAMPLES</span></span>

### <span data-ttu-id="91d04-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91d04-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="91d04-112">Atualiza o ASN por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="91d04-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="91d04-113">OS</span><span class="sxs-lookup"><span data-stu-id="91d04-113">PARAMETERS</span></span>

### <span data-ttu-id="91d04-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91d04-114">-AsJob</span></span>
<span data-ttu-id="91d04-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="91d04-115">Run in the background.</span></span>

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

### <span data-ttu-id="91d04-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="91d04-116">-Asn</span></span>
<span data-ttu-id="91d04-117">A ASN a ser registrada</span><span class="sxs-lookup"><span data-stu-id="91d04-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="91d04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d04-118">-DefaultProfile</span></span>
<span data-ttu-id="91d04-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91d04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d04-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91d04-120">-InputObject</span></span>
<span data-ttu-id="91d04-121">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="91d04-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="91d04-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="91d04-122">-Name</span></span>
<span data-ttu-id="91d04-123">A ASN a ser registrada</span><span class="sxs-lookup"><span data-stu-id="91d04-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="91d04-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="91d04-124">-PeeringName</span></span>
<span data-ttu-id="91d04-125">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="91d04-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="91d04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91d04-126">-ResourceGroupName</span></span>
<span data-ttu-id="91d04-127">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="91d04-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="91d04-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91d04-128">-ResourceId</span></span>
<span data-ttu-id="91d04-129">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="91d04-129">The resource id string name.</span></span>

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

### <span data-ttu-id="91d04-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91d04-130">-Confirm</span></span>
<span data-ttu-id="91d04-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91d04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d04-132">-WhatIf</span></span>
<span data-ttu-id="91d04-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91d04-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91d04-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91d04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d04-135">CommonParameters</span></span>
<span data-ttu-id="91d04-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d04-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91d04-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d04-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91d04-138">INPUTS</span></span>

### <span data-ttu-id="91d04-139">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="91d04-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="91d04-140">System. String</span><span class="sxs-lookup"><span data-stu-id="91d04-140">System.String</span></span>

## <span data-ttu-id="91d04-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91d04-141">OUTPUTS</span></span>

### <span data-ttu-id="91d04-142">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="91d04-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="91d04-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91d04-143">NOTES</span></span>

## <span data-ttu-id="91d04-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91d04-144">RELATED LINKS</span></span>
