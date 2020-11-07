---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775488"
---
# <span data-ttu-id="35c6e-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="35c6e-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="35c6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="35c6e-103">Obtém um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="35c6e-103">Gets a public IP address.</span></span>

## <span data-ttu-id="35c6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35c6e-104">SYNTAX</span></span>

### <span data-ttu-id="35c6e-105">NoExpandStandAloneIp (padrão)</span><span class="sxs-lookup"><span data-stu-id="35c6e-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35c6e-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="35c6e-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35c6e-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="35c6e-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35c6e-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="35c6e-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c6e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35c6e-109">DESCRIPTION</span></span>
<span data-ttu-id="35c6e-110">O cmdlet **Get-AzPublicIPAddress** Obtém um ou mais endereços IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35c6e-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="35c6e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35c6e-111">EXAMPLES</span></span>

### <span data-ttu-id="35c6e-112">1: obter um recurso de IP público</span><span class="sxs-lookup"><span data-stu-id="35c6e-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="35c6e-113">Este comando obtém um recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35c6e-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="35c6e-114">OS</span><span class="sxs-lookup"><span data-stu-id="35c6e-114">PARAMETERS</span></span>

### <span data-ttu-id="35c6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c6e-115">-DefaultProfile</span></span>
<span data-ttu-id="35c6e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35c6e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c6e-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="35c6e-117">-ExpandResource</span></span>
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

### <span data-ttu-id="35c6e-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="35c6e-118">-IpConfigurationName</span></span>
<span data-ttu-id="35c6e-119">Nome de configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="35c6e-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="35c6e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="35c6e-120">-Name</span></span>
<span data-ttu-id="35c6e-121">Especifica o nome do endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="35c6e-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="35c6e-122">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="35c6e-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="35c6e-123">Nome da interface de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35c6e-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="35c6e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c6e-124">-ResourceGroupName</span></span>
<span data-ttu-id="35c6e-125">Especifica o nome do grupo de recursos que contém o endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="35c6e-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="35c6e-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="35c6e-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="35c6e-127">Índice da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35c6e-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="35c6e-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="35c6e-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="35c6e-129">Nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35c6e-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="35c6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c6e-130">CommonParameters</span></span>
<span data-ttu-id="35c6e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c6e-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c6e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c6e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35c6e-133">INPUTS</span></span>

## <span data-ttu-id="35c6e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35c6e-134">OUTPUTS</span></span>

### <span data-ttu-id="35c6e-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="35c6e-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="35c6e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35c6e-136">NOTES</span></span>

## <span data-ttu-id="35c6e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35c6e-137">RELATED LINKS</span></span>

[<span data-ttu-id="35c6e-138">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="35c6e-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="35c6e-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="35c6e-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="35c6e-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="35c6e-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


