---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: eb6611bef2499c9aaf164ddbe2e7a31c63051751
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885320"
---
# <span data-ttu-id="55f2d-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="55f2d-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="55f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="55f2d-103">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="55f2d-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="55f2d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55f2d-104">SYNTAX</span></span>

### <span data-ttu-id="55f2d-105">ByVirtualWanName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55f2d-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f2d-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="55f2d-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f2d-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="55f2d-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f2d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55f2d-108">DESCRIPTION</span></span>
<span data-ttu-id="55f2d-109">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="55f2d-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="55f2d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55f2d-110">EXAMPLES</span></span>

### <span data-ttu-id="55f2d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55f2d-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="55f2d-112">O acima criará um grupo de recursos "testRG" na região "Oeste dos EUA" e uma WAN Virtual do Azure nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="55f2d-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="55f2d-113">VirtualWan é atualizado com novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="55f2d-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="55f2d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55f2d-114">PARAMETERS</span></span>

### <span data-ttu-id="55f2d-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="55f2d-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="55f2d-116">Permitir ramificação para o tráfego de filial para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="55f2d-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f2d-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="55f2d-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="55f2d-118">Permitir vnet para tráfego de vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="55f2d-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f2d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55f2d-119">-AsJob</span></span>
<span data-ttu-id="55f2d-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="55f2d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55f2d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f2d-121">-DefaultProfile</span></span>
<span data-ttu-id="55f2d-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55f2d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f2d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="55f2d-123">-Force</span></span>
<span data-ttu-id="55f2d-124">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="55f2d-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="55f2d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55f2d-125">-InputObject</span></span>
<span data-ttu-id="55f2d-126">O objeto wan virtual a ser modificado</span><span class="sxs-lookup"><span data-stu-id="55f2d-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f2d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="55f2d-127">-Name</span></span>
<span data-ttu-id="55f2d-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="55f2d-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f2d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f2d-129">-ResourceGroupName</span></span>
<span data-ttu-id="55f2d-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55f2d-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f2d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55f2d-131">-ResourceId</span></span>
<span data-ttu-id="55f2d-132">A ID de recurso do Azure para a wan virtual.</span><span class="sxs-lookup"><span data-stu-id="55f2d-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f2d-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="55f2d-133">-Tag</span></span>
<span data-ttu-id="55f2d-134">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="55f2d-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="55f2d-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="55f2d-135">-VirtualWANType</span></span>
<span data-ttu-id="55f2d-136">O tipo da Wan Virtual.</span><span class="sxs-lookup"><span data-stu-id="55f2d-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="55f2d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55f2d-137">-Confirm</span></span>
<span data-ttu-id="55f2d-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f2d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f2d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f2d-139">-WhatIf</span></span>
<span data-ttu-id="55f2d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55f2d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f2d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55f2d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f2d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f2d-142">CommonParameters</span></span>
<span data-ttu-id="55f2d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f2d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f2d-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55f2d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f2d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55f2d-145">INPUTS</span></span>

### <span data-ttu-id="55f2d-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="55f2d-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="55f2d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="55f2d-147">System.String</span></span>

## <span data-ttu-id="55f2d-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55f2d-148">OUTPUTS</span></span>

### <span data-ttu-id="55f2d-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="55f2d-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="55f2d-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="55f2d-150">NOTES</span></span>

## <span data-ttu-id="55f2d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55f2d-151">RELATED LINKS</span></span>

[<span data-ttu-id="55f2d-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="55f2d-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="55f2d-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="55f2d-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="55f2d-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="55f2d-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
