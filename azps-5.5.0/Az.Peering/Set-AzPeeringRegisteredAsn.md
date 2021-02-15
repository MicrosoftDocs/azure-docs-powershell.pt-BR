---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115015"
---
# <span data-ttu-id="a849a-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a849a-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a849a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a849a-102">SYNOPSIS</span></span>
<span data-ttu-id="a849a-103">Define ou atualiza uma ASN registrada do recurso de parêntese pai.</span><span class="sxs-lookup"><span data-stu-id="a849a-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="a849a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a849a-104">SYNTAX</span></span>

### <span data-ttu-id="a849a-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a849a-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a849a-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a849a-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a849a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a849a-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a849a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a849a-108">DESCRIPTION</span></span>
<span data-ttu-id="a849a-109">Permite a atualização de uma ASN registrada do recurso de parêntese pai.</span><span class="sxs-lookup"><span data-stu-id="a849a-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="a849a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a849a-110">EXAMPLES</span></span>

### <span data-ttu-id="a849a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a849a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="a849a-112">Atualiza o ASN por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a849a-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="a849a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a849a-113">PARAMETERS</span></span>

### <span data-ttu-id="a849a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a849a-114">-AsJob</span></span>
<span data-ttu-id="a849a-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a849a-115">Run in the background.</span></span>

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

### <span data-ttu-id="a849a-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="a849a-116">-Asn</span></span>
<span data-ttu-id="a849a-117">O ASN a ser registrado</span><span class="sxs-lookup"><span data-stu-id="a849a-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="a849a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a849a-118">-DefaultProfile</span></span>
<span data-ttu-id="a849a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a849a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a849a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a849a-120">-InputObject</span></span>
<span data-ttu-id="a849a-121">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a849a-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="a849a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a849a-122">-Name</span></span>
<span data-ttu-id="a849a-123">O ASN a ser registrado</span><span class="sxs-lookup"><span data-stu-id="a849a-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="a849a-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a849a-124">-PeeringName</span></span>
<span data-ttu-id="a849a-125">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a849a-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a849a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a849a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a849a-127">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="a849a-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="a849a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a849a-128">-ResourceId</span></span>
<span data-ttu-id="a849a-129">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a849a-129">The resource id string name.</span></span>

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

### <span data-ttu-id="a849a-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a849a-130">-Confirm</span></span>
<span data-ttu-id="a849a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a849a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a849a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a849a-132">-WhatIf</span></span>
<span data-ttu-id="a849a-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a849a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a849a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a849a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a849a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a849a-135">CommonParameters</span></span>
<span data-ttu-id="a849a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a849a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a849a-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a849a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a849a-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a849a-138">INPUTS</span></span>

### <span data-ttu-id="a849a-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a849a-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="a849a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a849a-140">System.String</span></span>

## <span data-ttu-id="a849a-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="a849a-141">OUTPUTS</span></span>

### <span data-ttu-id="a849a-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a849a-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a849a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="a849a-143">NOTES</span></span>

## <span data-ttu-id="a849a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a849a-144">RELATED LINKS</span></span>
