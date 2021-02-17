---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399389"
---
# <span data-ttu-id="b68aa-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="b68aa-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="b68aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b68aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b68aa-103">Obtém informações sobre um pacote de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="b68aa-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="b68aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b68aa-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b68aa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b68aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b68aa-106">O cmdlet **Get-AzVpnClientPackage** obtém informações sobre os pacotes de cliente VPN disponíveis em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b68aa-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="b68aa-107">Os pacotes cliente contêm dados de configuração que permitem que um computador cliente faça uma conexão VPN com uma rede virtual do Azure; os computadores cliente devem ter o pacote de configuração correto instalado para fazer uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="b68aa-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="b68aa-108">Pacotes de configuração diferentes estão disponíveis com base na versão do Windows do computador cliente (por exemplo, Windows 7 ou Windows 10) e na arquitetura de processador do computador cliente (AMD64 ou x86).</span><span class="sxs-lookup"><span data-stu-id="b68aa-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="b68aa-109">Você deve especificar o tipo de arquitetura ao executar **Get-AzVpnClientPackage.**</span><span class="sxs-lookup"><span data-stu-id="b68aa-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="b68aa-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b68aa-110">EXAMPLES</span></span>

### <span data-ttu-id="b68aa-111">Exemplo 1: Obter informações sobre um pacote de cliente VPN de arquitetura de processador</span><span class="sxs-lookup"><span data-stu-id="b68aa-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="b68aa-112">Este comando obtém informações sobre os pacotes de cliente VPN AMD64 armazenados no gateway de rede virtual chamado ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="b68aa-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="b68aa-113">Para obter informações sobre os pacotes cliente x86, de definir o valor do parâmetro *ProcessorArchitecture* como x86.</span><span class="sxs-lookup"><span data-stu-id="b68aa-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="b68aa-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b68aa-114">PARAMETERS</span></span>

### <span data-ttu-id="b68aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68aa-115">-DefaultProfile</span></span>
<span data-ttu-id="b68aa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b68aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b68aa-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="b68aa-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="b68aa-118">Especifica o tipo de arquitetura de CPU para o qual o pacote cliente foi projetado.</span><span class="sxs-lookup"><span data-stu-id="b68aa-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="b68aa-119">Os valores válidos são Amd64 e X86.</span><span class="sxs-lookup"><span data-stu-id="b68aa-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b68aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b68aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="b68aa-121">Especifica o nome do grupo de recursos ao que o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b68aa-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="b68aa-122">Os grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de estoque e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="b68aa-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b68aa-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b68aa-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b68aa-124">Especifica o nome do gateway de rede virtual onde as informações do pacote do cliente são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="b68aa-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b68aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68aa-125">CommonParameters</span></span>
<span data-ttu-id="b68aa-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68aa-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b68aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68aa-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="b68aa-128">INPUTS</span></span>

### <span data-ttu-id="b68aa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b68aa-129">System.String</span></span>

## <span data-ttu-id="b68aa-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b68aa-130">OUTPUTS</span></span>

### <span data-ttu-id="b68aa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b68aa-131">System.String</span></span>

## <span data-ttu-id="b68aa-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b68aa-132">NOTES</span></span>

## <span data-ttu-id="b68aa-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b68aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="b68aa-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b68aa-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)



