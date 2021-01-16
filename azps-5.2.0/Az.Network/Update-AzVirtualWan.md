---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261169"
---
# <span data-ttu-id="41798-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="41798-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="41798-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41798-102">SYNOPSIS</span></span>
<span data-ttu-id="41798-103">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="41798-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="41798-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41798-104">SYNTAX</span></span>

### <span data-ttu-id="41798-105">ByVirtualWanName (padrão)</span><span class="sxs-lookup"><span data-stu-id="41798-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41798-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="41798-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41798-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="41798-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41798-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41798-108">DESCRIPTION</span></span>
<span data-ttu-id="41798-109">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="41798-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="41798-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41798-110">EXAMPLES</span></span>

### <span data-ttu-id="41798-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41798-111">Example 1</span></span>

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

<span data-ttu-id="41798-112">A seguir, você criará um grupo de recursos "testRG" na região "oeste dos EUA" e uma WAN virtual do Azure nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="41798-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="41798-113">VirtualWan é atualizado com novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="41798-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="41798-114">OS</span><span class="sxs-lookup"><span data-stu-id="41798-114">PARAMETERS</span></span>

### <span data-ttu-id="41798-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="41798-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="41798-116">Permitir o tráfego de ramificação para o VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="41798-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="41798-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="41798-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="41798-118">Permitir tráfego vnet para vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="41798-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="41798-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41798-119">-AsJob</span></span>
<span data-ttu-id="41798-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="41798-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41798-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41798-121">-DefaultProfile</span></span>
<span data-ttu-id="41798-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41798-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41798-123">-Force</span><span class="sxs-lookup"><span data-stu-id="41798-123">-Force</span></span>
<span data-ttu-id="41798-124">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="41798-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="41798-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41798-125">-InputObject</span></span>
<span data-ttu-id="41798-126">O objeto de WAN virtual a ser modificado</span><span class="sxs-lookup"><span data-stu-id="41798-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="41798-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="41798-127">-Name</span></span>
<span data-ttu-id="41798-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="41798-128">The resource name.</span></span>

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

### <span data-ttu-id="41798-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41798-129">-ResourceGroupName</span></span>
<span data-ttu-id="41798-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41798-130">The resource group name.</span></span>

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

### <span data-ttu-id="41798-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41798-131">-ResourceId</span></span>
<span data-ttu-id="41798-132">A ID de recurso do Azure para a rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="41798-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="41798-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="41798-133">-Tag</span></span>
<span data-ttu-id="41798-134">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="41798-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="41798-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="41798-135">-VirtualWANType</span></span>
<span data-ttu-id="41798-136">O tipo da rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="41798-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="41798-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41798-137">-Confirm</span></span>
<span data-ttu-id="41798-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41798-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41798-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41798-139">-WhatIf</span></span>
<span data-ttu-id="41798-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41798-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41798-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41798-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41798-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41798-142">CommonParameters</span></span>
<span data-ttu-id="41798-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41798-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41798-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41798-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41798-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41798-145">INPUTS</span></span>

### <span data-ttu-id="41798-146">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="41798-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="41798-147">System. String</span><span class="sxs-lookup"><span data-stu-id="41798-147">System.String</span></span>

## <span data-ttu-id="41798-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41798-148">OUTPUTS</span></span>

### <span data-ttu-id="41798-149">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="41798-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="41798-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41798-150">NOTES</span></span>

## <span data-ttu-id="41798-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41798-151">RELATED LINKS</span></span>

[<span data-ttu-id="41798-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="41798-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="41798-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="41798-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="41798-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="41798-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
