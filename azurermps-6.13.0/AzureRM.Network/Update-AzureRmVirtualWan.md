---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428449"
---
# <span data-ttu-id="ca698-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ca698-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="ca698-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca698-102">SYNOPSIS</span></span>
<span data-ttu-id="ca698-103">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca698-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca698-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca698-104">SYNTAX</span></span>

### <span data-ttu-id="ca698-105">ByVirtualWanName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca698-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca698-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ca698-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca698-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ca698-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca698-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca698-108">DESCRIPTION</span></span>
<span data-ttu-id="ca698-109">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca698-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="ca698-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca698-110">EXAMPLES</span></span>

### <span data-ttu-id="ca698-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca698-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="ca698-112">A seguir, você criará um grupo de recursos "testRG" na região "oeste dos EUA" e uma WAN virtual do Azure nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca698-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="ca698-113">VirtualWan é atualizado com novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca698-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="ca698-114">OS</span><span class="sxs-lookup"><span data-stu-id="ca698-114">PARAMETERS</span></span>

### <span data-ttu-id="ca698-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="ca698-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="ca698-116">Permitir o tráfego de ramificação para o VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ca698-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="ca698-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="ca698-118">Permitir tráfego vnet para vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ca698-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca698-119">-AsJob</span></span>
<span data-ttu-id="ca698-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ca698-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca698-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca698-121">-DefaultProfile</span></span>
<span data-ttu-id="ca698-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca698-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ca698-123">-Force</span></span>
<span data-ttu-id="ca698-124">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="ca698-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ca698-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca698-125">-InputObject</span></span>
<span data-ttu-id="ca698-126">O objeto de WAN virtual a ser modificado</span><span class="sxs-lookup"><span data-stu-id="ca698-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca698-127">-Name</span></span>
<span data-ttu-id="ca698-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca698-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca698-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca698-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca698-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca698-131">-ResourceId</span></span>
<span data-ttu-id="ca698-132">A ID de recurso do Azure para a rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="ca698-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="ca698-133">-Tag</span></span>
<span data-ttu-id="ca698-134">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca698-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca698-135">-Confirm</span></span>
<span data-ttu-id="ca698-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca698-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca698-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca698-137">-WhatIf</span></span>
<span data-ttu-id="ca698-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca698-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca698-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca698-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca698-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca698-140">CommonParameters</span></span>
<span data-ttu-id="ca698-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca698-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca698-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca698-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca698-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca698-143">INPUTS</span></span>

### <span data-ttu-id="ca698-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ca698-144">System.String</span></span>

### <span data-ttu-id="ca698-145">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ca698-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="ca698-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca698-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca698-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca698-147">OUTPUTS</span></span>

### <span data-ttu-id="ca698-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ca698-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="ca698-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca698-149">NOTES</span></span>

## <span data-ttu-id="ca698-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca698-150">RELATED LINKS</span></span>
