---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 9df5cdd2a601977b453cb8242a9241cede3d4539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110546"
---
# <span data-ttu-id="d86fa-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86fa-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="d86fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d86fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d86fa-103">Obtém um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="d86fa-103">Gets a public IP address.</span></span>

## <span data-ttu-id="d86fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d86fa-104">SYNTAX</span></span>

### <span data-ttu-id="d86fa-105">NoExpandStandAloneIp (padrão)</span><span class="sxs-lookup"><span data-stu-id="d86fa-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d86fa-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="d86fa-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d86fa-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="d86fa-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d86fa-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="d86fa-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d86fa-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d86fa-109">DESCRIPTION</span></span>
<span data-ttu-id="d86fa-110">O cmdlet **Get-AzPublicIPAddress** Obtém um ou mais endereços IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86fa-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="d86fa-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d86fa-111">EXAMPLES</span></span>

### <span data-ttu-id="d86fa-112">Exemplo 1: obter um recurso de IP público</span><span class="sxs-lookup"><span data-stu-id="d86fa-112">Example 1: Get a public IP resource</span></span>
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="d86fa-113">Esse comando obtém um recurso de endereço IP público com o nome myPublicIp na myRg do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86fa-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="d86fa-114">Exemplo 2: obter recursos de IP público usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="d86fa-114">Example 2: Get public IP resources using filtering</span></span>
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="d86fa-115">Esse comando obtém todos os recursos de endereço IP público cujo nome começa com myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="d86fa-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="d86fa-116">OS</span><span class="sxs-lookup"><span data-stu-id="d86fa-116">PARAMETERS</span></span>

### <span data-ttu-id="d86fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86fa-117">-DefaultProfile</span></span>
<span data-ttu-id="d86fa-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d86fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d86fa-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d86fa-119">-ExpandResource</span></span>
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

### <span data-ttu-id="d86fa-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d86fa-120">-IpConfigurationName</span></span>
<span data-ttu-id="d86fa-121">Nome de configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d86fa-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="d86fa-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d86fa-122">-Name</span></span>
<span data-ttu-id="d86fa-123">Especifica o nome do endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="d86fa-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d86fa-124">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="d86fa-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="d86fa-125">Nome da interface de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d86fa-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="d86fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d86fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="d86fa-127">Especifica o nome do grupo de recursos que contém o endereço IP público que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="d86fa-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d86fa-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="d86fa-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="d86fa-129">Índice da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d86fa-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="d86fa-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d86fa-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d86fa-131">Nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d86fa-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="d86fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86fa-132">CommonParameters</span></span>
<span data-ttu-id="d86fa-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d86fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86fa-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d86fa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86fa-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d86fa-135">INPUTS</span></span>

### <span data-ttu-id="d86fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d86fa-136">System.String</span></span>

## <span data-ttu-id="d86fa-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d86fa-137">OUTPUTS</span></span>

### <span data-ttu-id="d86fa-138">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86fa-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d86fa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d86fa-139">NOTES</span></span>

## <span data-ttu-id="d86fa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d86fa-140">RELATED LINKS</span></span>

[<span data-ttu-id="d86fa-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86fa-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d86fa-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86fa-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="d86fa-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86fa-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


