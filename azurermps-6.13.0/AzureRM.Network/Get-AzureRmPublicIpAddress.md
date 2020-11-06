---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429507"
---
# <span data-ttu-id="ca723-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca723-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="ca723-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca723-102">SYNOPSIS</span></span>
<span data-ttu-id="ca723-103">Obtém um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="ca723-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca723-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca723-104">SYNTAX</span></span>

### <span data-ttu-id="ca723-105">NoExpandStandAloneIp (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca723-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca723-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="ca723-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca723-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="ca723-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca723-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="ca723-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca723-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca723-109">DESCRIPTION</span></span>
<span data-ttu-id="ca723-110">O cmdlet **Get-AzureRmPublicIPAddress** Obtém um ou mais endereços IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca723-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="ca723-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca723-111">EXAMPLES</span></span>

### <span data-ttu-id="ca723-112">1: obter um recurso de IP público</span><span class="sxs-lookup"><span data-stu-id="ca723-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="ca723-113">Este comando obtém um recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca723-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="ca723-114">OS</span><span class="sxs-lookup"><span data-stu-id="ca723-114">PARAMETERS</span></span>

### <span data-ttu-id="ca723-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca723-115">-DefaultProfile</span></span>
<span data-ttu-id="ca723-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca723-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca723-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ca723-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ca723-118">-IpConfigurationName</span></span>
<span data-ttu-id="ca723-119">Nome de configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="ca723-119">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca723-120">-Name</span></span>
<span data-ttu-id="ca723-121">Especifica o nome do endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ca723-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-122">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="ca723-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="ca723-123">Nome da interface de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca723-123">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca723-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca723-125">Especifica o nome do grupo de recursos que contém o endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ca723-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="ca723-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="ca723-127">Índice da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca723-127">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ca723-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="ca723-129">Nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca723-129">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca723-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca723-130">CommonParameters</span></span>
<span data-ttu-id="ca723-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca723-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca723-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca723-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca723-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca723-133">INPUTS</span></span>

### <span data-ttu-id="ca723-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ca723-134">System.String</span></span>

## <span data-ttu-id="ca723-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca723-135">OUTPUTS</span></span>

### <span data-ttu-id="ca723-136">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca723-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="ca723-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca723-137">NOTES</span></span>

## <span data-ttu-id="ca723-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca723-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca723-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca723-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="ca723-140">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca723-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="ca723-141">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca723-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


