---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775460"
---
# <span data-ttu-id="0479b-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="0479b-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="0479b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0479b-102">SYNOPSIS</span></span>
<span data-ttu-id="0479b-103">Obtém informações sobre um pacote de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="0479b-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="0479b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0479b-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0479b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0479b-105">DESCRIPTION</span></span>
<span data-ttu-id="0479b-106">O cmdlet **Get-AzVpnClientPackage** Obtém informações sobre os pacotes de cliente VPN disponíveis em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0479b-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="0479b-107">Os pacotes do cliente contêm dados de configuração que permitem que um computador cliente faça uma conexão VPN com uma rede virtual do Azure; os computadores cliente devem ter o pacote de configuração correto instalado para fazer uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="0479b-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="0479b-108">Pacotes de configuração diferentes estão disponíveis com base na versão do Windows do computador cliente (por exemplo, Windows 7 ou Windows 10) e na arquitetura do processador do computador cliente (AMD64 ou x86).</span><span class="sxs-lookup"><span data-stu-id="0479b-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="0479b-109">Você deve especificar o tipo de arquitetura ao executar **Get-AzVpnClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="0479b-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="0479b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0479b-110">EXAMPLES</span></span>

### <span data-ttu-id="0479b-111">Exemplo 1: obter informações sobre um pacote de cliente VPN da arquitetura do processador</span><span class="sxs-lookup"><span data-stu-id="0479b-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="0479b-112">Esse comando obtém informações sobre os pacotes do cliente VPN AMD64 armazenados no gateway de rede virtual chamado ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="0479b-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="0479b-113">Para obter informações sobre os pacotes do cliente x86, defina o valor do parâmetro *ProcessorArchitecture* para x86.</span><span class="sxs-lookup"><span data-stu-id="0479b-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="0479b-114">OS</span><span class="sxs-lookup"><span data-stu-id="0479b-114">PARAMETERS</span></span>

### <span data-ttu-id="0479b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0479b-115">-DefaultProfile</span></span>
<span data-ttu-id="0479b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0479b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0479b-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="0479b-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="0479b-118">Especifica o tipo de arquitetura de CPU para o qual o pacote do cliente foi projetado.</span><span class="sxs-lookup"><span data-stu-id="0479b-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="0479b-119">Os valores válidos são AMD64 e x86.</span><span class="sxs-lookup"><span data-stu-id="0479b-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0479b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0479b-120">-ResourceGroupName</span></span>
<span data-ttu-id="0479b-121">Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.</span><span class="sxs-lookup"><span data-stu-id="0479b-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="0479b-122">Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.</span><span class="sxs-lookup"><span data-stu-id="0479b-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0479b-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0479b-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0479b-124">Especifica o nome do gateway de rede virtual onde as informações do pacote do cliente são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="0479b-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0479b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0479b-125">CommonParameters</span></span>
<span data-ttu-id="0479b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0479b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0479b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0479b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0479b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0479b-128">INPUTS</span></span>

### <span data-ttu-id="0479b-129">String</span><span class="sxs-lookup"><span data-stu-id="0479b-129">String</span></span>
<span data-ttu-id="0479b-130">O parâmetro ' ResourceGroupName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0479b-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="0479b-131">String</span><span class="sxs-lookup"><span data-stu-id="0479b-131">String</span></span>
<span data-ttu-id="0479b-132">O parâmetro ' VirtualNetworkGatewayName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0479b-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0479b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0479b-133">OUTPUTS</span></span>

###  
<span data-ttu-id="0479b-134">**Get-AzVpnClientPackage** retorna instâncias do objeto System. String.</span><span class="sxs-lookup"><span data-stu-id="0479b-134">**Get-AzVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="0479b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0479b-135">NOTES</span></span>

## <span data-ttu-id="0479b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0479b-136">RELATED LINKS</span></span>

[<span data-ttu-id="0479b-137">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0479b-137">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0479b-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="0479b-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)

