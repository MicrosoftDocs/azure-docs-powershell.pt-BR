---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 3bb2a2d7c8e53cc7ba336234e3c5b24ad58e2faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890998"
---
# <span data-ttu-id="4efd1-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4efd1-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="4efd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4efd1-102">SYNOPSIS</span></span>
<span data-ttu-id="4efd1-103">Cria uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4efd1-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="4efd1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4efd1-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efd1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4efd1-105">DESCRIPTION</span></span>
<span data-ttu-id="4efd1-106">Cria um novo recurso do Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="4efd1-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="4efd1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4efd1-107">EXAMPLES</span></span>

### <span data-ttu-id="4efd1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4efd1-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="4efd1-109">O acima criará um grupo de recursos "testRG" na região "Oeste dos EUA" e uma WAN Virtual do Azure com ramificação para o tráfego de filial permitido nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="4efd1-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="4efd1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4efd1-110">PARAMETERS</span></span>

### <span data-ttu-id="4efd1-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="4efd1-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="4efd1-112">Permitir ramificação para o tráfego de filial para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4efd1-112">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="4efd1-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="4efd1-114">Permitir vnet para tráfego de vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4efd1-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4efd1-115">-AsJob</span></span>
<span data-ttu-id="4efd1-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4efd1-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efd1-117">-DefaultProfile</span></span>
<span data-ttu-id="4efd1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4efd1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4efd1-119">-Location</span></span>
<span data-ttu-id="4efd1-120">O local do recurso VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="4efd1-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4efd1-121">-Name</span></span>
<span data-ttu-id="4efd1-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4efd1-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4efd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="4efd1-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4efd1-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4efd1-125">-Tag</span></span>
<span data-ttu-id="4efd1-126">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="4efd1-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="4efd1-127">-VirtualWANType</span></span>
<span data-ttu-id="4efd1-128">O tipo da Wan Virtual.</span><span class="sxs-lookup"><span data-stu-id="4efd1-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4efd1-129">-Confirm</span></span>
<span data-ttu-id="4efd1-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4efd1-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efd1-131">-WhatIf</span></span>
<span data-ttu-id="4efd1-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4efd1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4efd1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4efd1-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efd1-134">CommonParameters</span></span>
<span data-ttu-id="4efd1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efd1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efd1-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4efd1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efd1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4efd1-137">INPUTS</span></span>

### <span data-ttu-id="4efd1-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4efd1-138">None</span></span>

## <span data-ttu-id="4efd1-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4efd1-139">OUTPUTS</span></span>

### <span data-ttu-id="4efd1-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4efd1-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="4efd1-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="4efd1-141">NOTES</span></span>

## <span data-ttu-id="4efd1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4efd1-142">RELATED LINKS</span></span>

[<span data-ttu-id="4efd1-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4efd1-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="4efd1-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4efd1-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="4efd1-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4efd1-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
