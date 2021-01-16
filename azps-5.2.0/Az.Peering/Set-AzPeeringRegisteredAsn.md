---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261405"
---
# <span data-ttu-id="04826-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="04826-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="04826-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04826-102">SYNOPSIS</span></span>
<span data-ttu-id="04826-103">Define ou atualiza uma ASN registrada do recurso de emparelhamento primário.</span><span class="sxs-lookup"><span data-stu-id="04826-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="04826-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04826-104">SYNTAX</span></span>

### <span data-ttu-id="04826-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="04826-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04826-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="04826-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04826-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="04826-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04826-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04826-108">DESCRIPTION</span></span>
<span data-ttu-id="04826-109">Permite a atualização de um ASN registrado do recurso de emparelhamento pai.</span><span class="sxs-lookup"><span data-stu-id="04826-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="04826-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04826-110">EXAMPLES</span></span>

### <span data-ttu-id="04826-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04826-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="04826-112">Atualiza o ASN por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="04826-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="04826-113">OS</span><span class="sxs-lookup"><span data-stu-id="04826-113">PARAMETERS</span></span>

### <span data-ttu-id="04826-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04826-114">-AsJob</span></span>
<span data-ttu-id="04826-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="04826-115">Run in the background.</span></span>

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

### <span data-ttu-id="04826-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="04826-116">-Asn</span></span>
<span data-ttu-id="04826-117">A ASN a ser registrada</span><span class="sxs-lookup"><span data-stu-id="04826-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="04826-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04826-118">-DefaultProfile</span></span>
<span data-ttu-id="04826-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04826-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04826-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04826-120">-InputObject</span></span>
<span data-ttu-id="04826-121">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="04826-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="04826-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="04826-122">-Name</span></span>
<span data-ttu-id="04826-123">A ASN a ser registrada</span><span class="sxs-lookup"><span data-stu-id="04826-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="04826-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="04826-124">-PeeringName</span></span>
<span data-ttu-id="04826-125">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="04826-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="04826-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04826-126">-ResourceGroupName</span></span>
<span data-ttu-id="04826-127">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="04826-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="04826-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04826-128">-ResourceId</span></span>
<span data-ttu-id="04826-129">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="04826-129">The resource id string name.</span></span>

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

### <span data-ttu-id="04826-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04826-130">-Confirm</span></span>
<span data-ttu-id="04826-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04826-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04826-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04826-132">-WhatIf</span></span>
<span data-ttu-id="04826-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04826-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04826-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04826-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04826-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04826-135">CommonParameters</span></span>
<span data-ttu-id="04826-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04826-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04826-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04826-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04826-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04826-138">INPUTS</span></span>

### <span data-ttu-id="04826-139">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="04826-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="04826-140">System. String</span><span class="sxs-lookup"><span data-stu-id="04826-140">System.String</span></span>

## <span data-ttu-id="04826-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04826-141">OUTPUTS</span></span>

### <span data-ttu-id="04826-142">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="04826-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="04826-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04826-143">NOTES</span></span>

## <span data-ttu-id="04826-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04826-144">RELATED LINKS</span></span>
