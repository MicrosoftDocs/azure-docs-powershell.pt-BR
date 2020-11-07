---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 1404acfa32de79096e990adbe2f66b43af0d4e96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786450"
---
# <span data-ttu-id="8bdbd-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bdbd-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="8bdbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdbd-103">Obtém um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bdbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bdbd-104">SYNTAX</span></span>

### <span data-ttu-id="8bdbd-105">NoExpandStandAloneIp (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bdbd-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bdbd-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="8bdbd-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bdbd-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="8bdbd-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bdbd-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="8bdbd-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bdbd-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bdbd-109">DESCRIPTION</span></span>
<span data-ttu-id="8bdbd-110">O cmdlet **Get-AzureRmPublicIPAddress** Obtém um ou mais endereços IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="8bdbd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bdbd-111">EXAMPLES</span></span>

### <span data-ttu-id="8bdbd-112">1: obter um recurso de IP público</span><span class="sxs-lookup"><span data-stu-id="8bdbd-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="8bdbd-113">Este comando obtém um recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="8bdbd-114">OS</span><span class="sxs-lookup"><span data-stu-id="8bdbd-114">PARAMETERS</span></span>

### <span data-ttu-id="8bdbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdbd-115">-DefaultProfile</span></span>
<span data-ttu-id="8bdbd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8bdbd-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8bdbd-118">-IpConfigurationName</span></span>
<span data-ttu-id="8bdbd-119">Nome de configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bdbd-120">-Name</span></span>
<span data-ttu-id="8bdbd-121">Especifica o nome do endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-122">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="8bdbd-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="8bdbd-123">Nome da interface de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdbd-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bdbd-125">Especifica o nome do grupo de recursos que contém o endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="8bdbd-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="8bdbd-127">Índice da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8bdbd-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="8bdbd-129">Nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdbd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdbd-130">CommonParameters</span></span>
<span data-ttu-id="8bdbd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdbd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdbd-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdbd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdbd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bdbd-133">INPUTS</span></span>

## <span data-ttu-id="8bdbd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bdbd-134">OUTPUTS</span></span>

### <span data-ttu-id="8bdbd-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bdbd-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8bdbd-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bdbd-136">NOTES</span></span>

## <span data-ttu-id="8bdbd-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bdbd-137">RELATED LINKS</span></span>

[<span data-ttu-id="8bdbd-138">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bdbd-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8bdbd-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bdbd-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8bdbd-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bdbd-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


