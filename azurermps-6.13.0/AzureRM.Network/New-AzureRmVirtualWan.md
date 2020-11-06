---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440747"
---
# <span data-ttu-id="43999-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43999-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="43999-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43999-102">SYNOPSIS</span></span>
<span data-ttu-id="43999-103">Cria uma rede de longa distância virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="43999-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43999-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43999-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43999-105">DESCRIPTION</span></span>
<span data-ttu-id="43999-106">Cria um novo recurso do Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="43999-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="43999-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43999-107">EXAMPLES</span></span>

### <span data-ttu-id="43999-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43999-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="43999-109">A seguir, você criará um grupo de recursos "testRG" na região "oeste dos EUA" e uma WAN virtual do Azure com o tráfego de ramificação para ramificação permitido no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="43999-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="43999-110">OS</span><span class="sxs-lookup"><span data-stu-id="43999-110">PARAMETERS</span></span>

### <span data-ttu-id="43999-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="43999-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="43999-112">Permitir o tráfego de ramificação para o VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="43999-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="43999-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="43999-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="43999-114">Permitir tráfego vnet para vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="43999-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="43999-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43999-115">-AsJob</span></span>
<span data-ttu-id="43999-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="43999-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43999-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43999-117">-DefaultProfile</span></span>
<span data-ttu-id="43999-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43999-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43999-119">-Local</span><span class="sxs-lookup"><span data-stu-id="43999-119">-Location</span></span>
<span data-ttu-id="43999-120">O local do recurso VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="43999-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43999-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="43999-121">-Name</span></span>
<span data-ttu-id="43999-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="43999-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43999-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43999-123">-ResourceGroupName</span></span>
<span data-ttu-id="43999-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43999-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43999-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="43999-125">-Tag</span></span>
<span data-ttu-id="43999-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="43999-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43999-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43999-127">-Confirm</span></span>
<span data-ttu-id="43999-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43999-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43999-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43999-129">-WhatIf</span></span>
<span data-ttu-id="43999-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43999-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43999-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43999-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43999-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43999-132">CommonParameters</span></span>
<span data-ttu-id="43999-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43999-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43999-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43999-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43999-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43999-135">INPUTS</span></span>

### <span data-ttu-id="43999-136">System. String</span><span class="sxs-lookup"><span data-stu-id="43999-136">System.String</span></span>

### <span data-ttu-id="43999-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="43999-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="43999-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43999-138">OUTPUTS</span></span>

### <span data-ttu-id="43999-139">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43999-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="43999-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43999-140">NOTES</span></span>

## <span data-ttu-id="43999-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43999-141">RELATED LINKS</span></span>
