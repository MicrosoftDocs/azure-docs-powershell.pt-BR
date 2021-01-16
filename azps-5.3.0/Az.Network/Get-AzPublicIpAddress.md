---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428534"
---
# <span data-ttu-id="a1e33-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1e33-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="a1e33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1e33-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e33-103">Obtém um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="a1e33-103">Gets a public IP address.</span></span>

## <span data-ttu-id="a1e33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1e33-104">SYNTAX</span></span>

### <span data-ttu-id="a1e33-105">NoExpandStandAloneIp (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1e33-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1e33-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="a1e33-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e33-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="a1e33-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e33-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="a1e33-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e33-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1e33-109">DESCRIPTION</span></span>
<span data-ttu-id="a1e33-110">O cmdlet **Get-AzPublicIPAddress** Obtém um ou mais endereços IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1e33-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="a1e33-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1e33-111">EXAMPLES</span></span>

### <span data-ttu-id="a1e33-112">Exemplo 1: obter um recurso de IP público</span><span class="sxs-lookup"><span data-stu-id="a1e33-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="a1e33-113">Esse comando obtém um recurso de endereço IP público com o nome myPublicIp na myRg do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1e33-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="a1e33-114">Exemplo 2: obter recursos de IP público usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="a1e33-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="a1e33-115">Esse comando obtém todos os recursos de endereço IP público cujo nome começa com myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="a1e33-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="a1e33-116">OS</span><span class="sxs-lookup"><span data-stu-id="a1e33-116">PARAMETERS</span></span>

### <span data-ttu-id="a1e33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e33-117">-DefaultProfile</span></span>
<span data-ttu-id="a1e33-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e33-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e33-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a1e33-119">-ExpandResource</span></span>
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

### <span data-ttu-id="a1e33-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a1e33-120">-IpConfigurationName</span></span>
<span data-ttu-id="a1e33-121">Nome de configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a1e33-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="a1e33-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1e33-122">-Name</span></span>
<span data-ttu-id="a1e33-123">Especifica o nome do endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a1e33-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a1e33-124">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="a1e33-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="a1e33-125">Nome da interface de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1e33-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="a1e33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e33-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1e33-127">Especifica o nome do grupo de recursos que contém o endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a1e33-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a1e33-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="a1e33-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="a1e33-129">Índice da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1e33-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="a1e33-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a1e33-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="a1e33-131">Nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1e33-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="a1e33-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e33-132">CommonParameters</span></span>
<span data-ttu-id="a1e33-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e33-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e33-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1e33-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e33-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1e33-135">INPUTS</span></span>

### <span data-ttu-id="a1e33-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e33-136">System.String</span></span>

## <span data-ttu-id="a1e33-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1e33-137">OUTPUTS</span></span>

### <span data-ttu-id="a1e33-138">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1e33-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a1e33-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1e33-139">NOTES</span></span>

## <span data-ttu-id="a1e33-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1e33-140">RELATED LINKS</span></span>

[<span data-ttu-id="a1e33-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1e33-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a1e33-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1e33-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="a1e33-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1e33-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


