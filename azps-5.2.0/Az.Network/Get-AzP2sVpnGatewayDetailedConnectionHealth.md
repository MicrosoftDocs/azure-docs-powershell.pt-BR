---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264196"
---
# <span data-ttu-id="fadc6-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="fadc6-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="fadc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fadc6-102">SYNOPSIS</span></span>
<span data-ttu-id="fadc6-103">Obtém as informações detalhadas do ponto atual para conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fadc6-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="fadc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fadc6-104">SYNTAX</span></span>

### <span data-ttu-id="fadc6-105">ByP2SVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fadc6-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fadc6-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fadc6-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fadc6-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fadc6-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fadc6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fadc6-108">DESCRIPTION</span></span>
<span data-ttu-id="fadc6-109">O cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** permite que você obtenha as informações detalhadas do ponto atual para conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fadc6-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="fadc6-110">O cliente precisa passar pela URL SAS, onde poderemos colocar essas informações detalhadas sobre a saúde.</span><span class="sxs-lookup"><span data-stu-id="fadc6-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="fadc6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fadc6-111">EXAMPLES</span></span>

### <span data-ttu-id="fadc6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fadc6-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="fadc6-113">O cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** permite que você obtenha as informações detalhadas do ponto atual para conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fadc6-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="fadc6-114">O cliente pode baixar detalhes de integridade do download da URL SAS aprovada.</span><span class="sxs-lookup"><span data-stu-id="fadc6-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="fadc6-115">Isso mostrará as informações de cada ponto para conexão do site com nomes de email, bytes em bytes de saída, endereço IP alocado, etc.</span><span class="sxs-lookup"><span data-stu-id="fadc6-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="fadc6-116">OS</span><span class="sxs-lookup"><span data-stu-id="fadc6-116">PARAMETERS</span></span>

### <span data-ttu-id="fadc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadc6-117">-DefaultProfile</span></span>
<span data-ttu-id="fadc6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fadc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fadc6-119">-InputObject</span></span>
<span data-ttu-id="fadc6-120">O objeto de gateway de VPN P2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="fadc6-120">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fadc6-121">-Name</span></span>
<span data-ttu-id="fadc6-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fadc6-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="fadc6-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="fadc6-124">OutputBlob a URL SAS à qual a integridade da conexão VPN do P2s será gravada.</span><span class="sxs-lookup"><span data-stu-id="fadc6-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadc6-125">-ResourceGroupName</span></span>
<span data-ttu-id="fadc6-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fadc6-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fadc6-127">-ResourceId</span></span>
<span data-ttu-id="fadc6-128">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="fadc6-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="fadc6-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="fadc6-130">A lista de nomes de usuários VPN P2S para filtrar.</span><span class="sxs-lookup"><span data-stu-id="fadc6-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadc6-131">CommonParameters</span></span>
<span data-ttu-id="fadc6-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fadc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadc6-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fadc6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadc6-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fadc6-134">INPUTS</span></span>

### <span data-ttu-id="fadc6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fadc6-135">System.String</span></span>
<span data-ttu-id="fadc6-136">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fadc6-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="fadc6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fadc6-137">OUTPUTS</span></span>

### <span data-ttu-id="fadc6-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="fadc6-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="fadc6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fadc6-139">NOTES</span></span>

## <span data-ttu-id="fadc6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fadc6-140">RELATED LINKS</span></span>
