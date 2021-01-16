---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271718"
---
# <span data-ttu-id="f9305-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9305-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="f9305-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9305-102">SYNOPSIS</span></span>
<span data-ttu-id="f9305-103">Cria uma rede de longa distância virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9305-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="f9305-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9305-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9305-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9305-105">DESCRIPTION</span></span>
<span data-ttu-id="f9305-106">Cria um novo recurso do Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="f9305-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="f9305-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9305-107">EXAMPLES</span></span>

### <span data-ttu-id="f9305-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9305-108">Example 1</span></span>

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

<span data-ttu-id="f9305-109">A seguir, você criará um grupo de recursos "testRG" na região "oeste dos EUA" e uma WAN virtual do Azure com o tráfego de ramificação para ramificação permitido no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9305-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="f9305-110">OS</span><span class="sxs-lookup"><span data-stu-id="f9305-110">PARAMETERS</span></span>

### <span data-ttu-id="f9305-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="f9305-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="f9305-112">Permitir o tráfego de ramificação para o VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f9305-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="f9305-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="f9305-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="f9305-114">Permitir tráfego vnet para vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f9305-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="f9305-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9305-115">-AsJob</span></span>
<span data-ttu-id="f9305-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f9305-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9305-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9305-117">-DefaultProfile</span></span>
<span data-ttu-id="f9305-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9305-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9305-119">-Local</span><span class="sxs-lookup"><span data-stu-id="f9305-119">-Location</span></span>
<span data-ttu-id="f9305-120">O local do recurso VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="f9305-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="f9305-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9305-121">-Name</span></span>
<span data-ttu-id="f9305-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f9305-122">The resource name.</span></span>

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

### <span data-ttu-id="f9305-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9305-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9305-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9305-124">The resource group name.</span></span>

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

### <span data-ttu-id="f9305-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="f9305-125">-Tag</span></span>
<span data-ttu-id="f9305-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9305-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f9305-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f9305-127">-VirtualWANType</span></span>
<span data-ttu-id="f9305-128">O tipo da rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="f9305-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="f9305-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9305-129">-Confirm</span></span>
<span data-ttu-id="f9305-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9305-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9305-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9305-131">-WhatIf</span></span>
<span data-ttu-id="f9305-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9305-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9305-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9305-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9305-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9305-134">CommonParameters</span></span>
<span data-ttu-id="f9305-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9305-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9305-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9305-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9305-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9305-137">INPUTS</span></span>

### <span data-ttu-id="f9305-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f9305-138">None</span></span>

## <span data-ttu-id="f9305-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9305-139">OUTPUTS</span></span>

### <span data-ttu-id="f9305-140">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9305-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="f9305-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9305-141">NOTES</span></span>

## <span data-ttu-id="f9305-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9305-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9305-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9305-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="f9305-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9305-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="f9305-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9305-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
