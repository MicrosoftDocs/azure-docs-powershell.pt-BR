---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115128"
---
# <span data-ttu-id="f9404-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9404-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f9404-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9404-102">SYNOPSIS</span></span>
<span data-ttu-id="f9404-103">Cria um Gateway de Rede Local</span><span class="sxs-lookup"><span data-stu-id="f9404-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="f9404-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9404-104">SYNTAX</span></span>

### <span data-ttu-id="f9404-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9404-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9404-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="f9404-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9404-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9404-107">DESCRIPTION</span></span>
<span data-ttu-id="f9404-108">O Gateway de Rede Local é o objeto que representa seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="f9404-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f9404-109">O cmdlet **New-AzLocalNetworkGateway** cria o objeto que representa seu gateway local com base no Nome, Nome do Grupo de Recursos, Local e Endereço IP do gateway, bem como o Prefixo de Endereço da rede local que se conectará ao Azure.</span><span class="sxs-lookup"><span data-stu-id="f9404-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="f9404-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9404-110">EXAMPLES</span></span>

### <span data-ttu-id="f9404-111">Exemplo 1: Criar um Gateway de Rede Local</span><span class="sxs-lookup"><span data-stu-id="f9404-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="f9404-112">Cria o objeto do Gateway de Rede Local com o nome "myLocalGW" dentro do grupo de recursos "myRG" no local "Oeste dos EUA" com o endereço IP "23.99.221.164" e o prefixo de endereço "10.5.51.0/24" no local.</span><span class="sxs-lookup"><span data-stu-id="f9404-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="f9404-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9404-113">PARAMETERS</span></span>

### <span data-ttu-id="f9404-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f9404-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9404-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9404-115">-AsJob</span></span>
<span data-ttu-id="f9404-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f9404-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9404-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="f9404-117">-Asn</span></span>
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

### <span data-ttu-id="f9404-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f9404-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="f9404-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9404-119">-DefaultProfile</span></span>
<span data-ttu-id="f9404-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f9404-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9404-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f9404-121">-Force</span></span>
<span data-ttu-id="f9404-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9404-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9404-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="f9404-123">-Fqdn</span></span>
<span data-ttu-id="f9404-124">FQDN do gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="f9404-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9404-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9404-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9404-126">-Local</span><span class="sxs-lookup"><span data-stu-id="f9404-126">-Location</span></span>
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

### <span data-ttu-id="f9404-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9404-127">-Name</span></span>
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

### <span data-ttu-id="f9404-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f9404-128">-PeerWeight</span></span>
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

### <span data-ttu-id="f9404-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9404-129">-ResourceGroupName</span></span>
<span data-ttu-id="f9404-130">Especifica o grupo de recursos ao que o gateway de rede local pertence.</span><span class="sxs-lookup"><span data-stu-id="f9404-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="f9404-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9404-131">-Tag</span></span>
<span data-ttu-id="f9404-132">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f9404-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f9404-133">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f9404-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f9404-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f9404-134">-Confirm</span></span>
<span data-ttu-id="f9404-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9404-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9404-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9404-136">-WhatIf</span></span>
<span data-ttu-id="f9404-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f9404-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9404-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9404-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9404-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9404-139">CommonParameters</span></span>
<span data-ttu-id="f9404-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9404-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9404-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9404-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9404-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9404-142">INPUTS</span></span>

### <span data-ttu-id="f9404-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f9404-143">System.String</span></span>

### <span data-ttu-id="f9404-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f9404-144">System.String[]</span></span>

### <span data-ttu-id="f9404-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="f9404-145">System.UInt32</span></span>

### <span data-ttu-id="f9404-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f9404-146">System.Int32</span></span>

### <span data-ttu-id="f9404-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9404-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9404-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9404-148">OUTPUTS</span></span>

### <span data-ttu-id="f9404-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9404-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f9404-150">Notas</span><span class="sxs-lookup"><span data-stu-id="f9404-150">NOTES</span></span>

## <span data-ttu-id="f9404-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9404-151">RELATED LINKS</span></span>

[<span data-ttu-id="f9404-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9404-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="f9404-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9404-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="f9404-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9404-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
