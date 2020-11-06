---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433065"
---
# <span data-ttu-id="3ef77-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef77-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="3ef77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ef77-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef77-103">Cria um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="3ef77-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ef77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ef77-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ef77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ef77-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef77-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="3ef77-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="3ef77-107">O cmdlet **New-AzureRmLocalNetworkGateway** cria o objeto que representa o gateway local de acordo com o nome, o nome do grupo de recursos, o local e o endereço IP do gateway, bem como o prefixo do endereço da rede local que será conectada ao Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef77-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="3ef77-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ef77-108">EXAMPLES</span></span>

### <span data-ttu-id="3ef77-109">1: criar um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="3ef77-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="3ef77-110">Cria o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" no local "West US" com o endereço IP "23.99.221.164" e o prefixo de endereço "10.5.51.0/24" local.</span><span class="sxs-lookup"><span data-stu-id="3ef77-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="3ef77-111">OS</span><span class="sxs-lookup"><span data-stu-id="3ef77-111">PARAMETERS</span></span>

### <span data-ttu-id="3ef77-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3ef77-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="3ef77-113">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3ef77-114">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3ef77-115">-Force</span></span>
<span data-ttu-id="3ef77-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3ef77-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ef77-117">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ef77-117">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-118">-Local</span><span class="sxs-lookup"><span data-stu-id="3ef77-118">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ef77-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3ef77-120">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef77-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ef77-122">Especifica o grupo de recursos ao qual pertence o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="3ef77-122">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="3ef77-123">-Tag</span></span>
<span data-ttu-id="3ef77-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3ef77-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ef77-125">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3ef77-125">For example:</span></span>

<span data-ttu-id="3ef77-126">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3ef77-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ef77-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ef77-127">-Confirm</span></span>
<span data-ttu-id="3ef77-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ef77-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef77-129">-WhatIf</span></span>
<span data-ttu-id="3ef77-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ef77-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef77-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ef77-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef77-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef77-132">-DefaultProfile</span></span>
<span data-ttu-id="3ef77-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef77-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ef77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef77-134">CommonParameters</span></span>
<span data-ttu-id="3ef77-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef77-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef77-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef77-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ef77-137">INPUTS</span></span>

## <span data-ttu-id="3ef77-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ef77-138">OUTPUTS</span></span>

### <span data-ttu-id="3ef77-139">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef77-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3ef77-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ef77-140">NOTES</span></span>

## <span data-ttu-id="3ef77-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ef77-141">RELATED LINKS</span></span>

[<span data-ttu-id="3ef77-142">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef77-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3ef77-143">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef77-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3ef77-144">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef77-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
