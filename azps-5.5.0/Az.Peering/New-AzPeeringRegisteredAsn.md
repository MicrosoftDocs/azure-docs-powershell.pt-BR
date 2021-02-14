---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117284"
---
# <span data-ttu-id="ae237-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="ae237-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="ae237-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae237-102">SYNOPSIS</span></span>
<span data-ttu-id="ae237-103">Criar ASN registrado para peering</span><span class="sxs-lookup"><span data-stu-id="ae237-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="ae237-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae237-104">SYNTAX</span></span>

### <span data-ttu-id="ae237-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae237-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae237-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ae237-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae237-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae237-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae237-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae237-108">DESCRIPTION</span></span>
<span data-ttu-id="ae237-109">Crie ASNs registradas para objetos de peering.</span><span class="sxs-lookup"><span data-stu-id="ae237-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="ae237-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae237-110">EXAMPLES</span></span>

### <span data-ttu-id="ae237-111">Obter o peering e criar uma ASN registrada</span><span class="sxs-lookup"><span data-stu-id="ae237-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="ae237-112">Obter o par que você deseja adicionar uma ASN registrada.</span><span class="sxs-lookup"><span data-stu-id="ae237-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="ae237-113">Em seguida, passe-o para o commandlet.</span><span class="sxs-lookup"><span data-stu-id="ae237-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="ae237-114">Usar o peering resourceId para criar uma asn registrada</span><span class="sxs-lookup"><span data-stu-id="ae237-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="ae237-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae237-115">PARAMETERS</span></span>

### <span data-ttu-id="ae237-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae237-116">-AsJob</span></span>
<span data-ttu-id="ae237-117">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ae237-117">Run in the background.</span></span>

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

### <span data-ttu-id="ae237-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="ae237-118">-Asn</span></span>
<span data-ttu-id="ae237-119">O ASN a ser registrado</span><span class="sxs-lookup"><span data-stu-id="ae237-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="ae237-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae237-120">-DefaultProfile</span></span>
<span data-ttu-id="ae237-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae237-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae237-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae237-122">-InputObject</span></span>
<span data-ttu-id="ae237-123">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="ae237-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="ae237-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae237-124">-Name</span></span>
<span data-ttu-id="ae237-125">O ASN a ser registrado</span><span class="sxs-lookup"><span data-stu-id="ae237-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="ae237-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="ae237-126">-PeeringName</span></span>
<span data-ttu-id="ae237-127">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ae237-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ae237-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae237-128">-ResourceGroupName</span></span>
<span data-ttu-id="ae237-129">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="ae237-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ae237-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae237-130">-ResourceId</span></span>
<span data-ttu-id="ae237-131">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae237-131">The resource id string name.</span></span>

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

### <span data-ttu-id="ae237-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ae237-132">-Confirm</span></span>
<span data-ttu-id="ae237-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae237-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae237-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae237-134">-WhatIf</span></span>
<span data-ttu-id="ae237-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ae237-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae237-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae237-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae237-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae237-137">CommonParameters</span></span>
<span data-ttu-id="ae237-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae237-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae237-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae237-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae237-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="ae237-140">INPUTS</span></span>

### <span data-ttu-id="ae237-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="ae237-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="ae237-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ae237-142">System.String</span></span>

## <span data-ttu-id="ae237-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="ae237-143">OUTPUTS</span></span>

### <span data-ttu-id="ae237-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="ae237-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="ae237-145">Notas</span><span class="sxs-lookup"><span data-stu-id="ae237-145">NOTES</span></span>

## <span data-ttu-id="ae237-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae237-146">RELATED LINKS</span></span>
