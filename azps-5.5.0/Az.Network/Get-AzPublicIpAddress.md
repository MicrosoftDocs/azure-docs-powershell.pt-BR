---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112892"
---
# <span data-ttu-id="f6680-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6680-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="f6680-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6680-102">SYNOPSIS</span></span>
<span data-ttu-id="f6680-103">Obtém um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="f6680-103">Gets a public IP address.</span></span>

## <span data-ttu-id="f6680-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6680-104">SYNTAX</span></span>

### <span data-ttu-id="f6680-105">NoExpandStandAloneIp (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6680-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6680-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="f6680-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6680-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="f6680-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6680-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="f6680-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6680-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6680-109">DESCRIPTION</span></span>
<span data-ttu-id="f6680-110">O cmdlet **Get-AzPublicIPAddress** obtém um ou mais endereços IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6680-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="f6680-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6680-111">EXAMPLES</span></span>

### <span data-ttu-id="f6680-112">Exemplo 1: Obter um recurso IP público</span><span class="sxs-lookup"><span data-stu-id="f6680-112">Example 1: Get a public IP resource</span></span>
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

<span data-ttu-id="f6680-113">Esse comando obtém um recurso de endereço IP público com o nome meuPublicIp no grupo de recursos myRg.</span><span class="sxs-lookup"><span data-stu-id="f6680-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="f6680-114">Exemplo 2: Obter recursos ip públicos usando filtragem</span><span class="sxs-lookup"><span data-stu-id="f6680-114">Example 2: Get public IP resources using filtering</span></span>
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

<span data-ttu-id="f6680-115">Esse comando obtém todos os recursos de endereço IP públicos cujo nome começa com meuPublicIp.</span><span class="sxs-lookup"><span data-stu-id="f6680-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="f6680-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6680-116">PARAMETERS</span></span>

### <span data-ttu-id="f6680-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6680-117">-DefaultProfile</span></span>
<span data-ttu-id="f6680-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f6680-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6680-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f6680-119">-ExpandResource</span></span>
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

### <span data-ttu-id="f6680-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6680-120">-IpConfigurationName</span></span>
<span data-ttu-id="f6680-121">Nome de configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f6680-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="f6680-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6680-122">-Name</span></span>
<span data-ttu-id="f6680-123">Especifica o nome do endereço IP público que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6680-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f6680-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f6680-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="f6680-125">Nome da interface de rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6680-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="f6680-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6680-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6680-127">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6680-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f6680-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="f6680-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="f6680-129">Índice de Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="f6680-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="f6680-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f6680-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="f6680-131">Nome de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6680-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="f6680-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6680-132">CommonParameters</span></span>
<span data-ttu-id="f6680-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6680-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6680-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6680-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6680-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6680-135">INPUTS</span></span>

### <span data-ttu-id="f6680-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f6680-136">System.String</span></span>

## <span data-ttu-id="f6680-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6680-137">OUTPUTS</span></span>

### <span data-ttu-id="f6680-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6680-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f6680-139">Notas</span><span class="sxs-lookup"><span data-stu-id="f6680-139">NOTES</span></span>

## <span data-ttu-id="f6680-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6680-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6680-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6680-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="f6680-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6680-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="f6680-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6680-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


