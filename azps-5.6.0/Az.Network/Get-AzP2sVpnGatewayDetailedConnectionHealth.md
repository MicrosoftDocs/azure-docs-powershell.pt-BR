---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 17092ab89ded950678e60b079cd30558f7ce2aac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885667"
---
# <span data-ttu-id="1ecc9-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1ecc9-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="1ecc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecc9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecc9-103">Obtém as informações detalhadas do ponto atual para conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="1ecc9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ecc9-104">SYNTAX</span></span>

### <span data-ttu-id="1ecc9-105">ByP2SVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1ecc9-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ecc9-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1ecc9-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ecc9-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="1ecc9-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecc9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ecc9-108">DESCRIPTION</span></span>
<span data-ttu-id="1ecc9-109">O cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** permite que você receba as informações detalhadas de conexões de ponto atual para site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="1ecc9-110">O cliente precisa passar a URL do SAS onde podemos colocar essas informações detalhadas de saúde.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="1ecc9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ecc9-111">EXAMPLES</span></span>

### <span data-ttu-id="1ecc9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ecc9-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="1ecc9-113">O cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** permite que você receba as informações detalhadas de conexões de ponto atual para site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="1ecc9-114">O cliente pode baixar detalhes de saúde do download de url do SAS passado.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="1ecc9-115">Isso mostrará informações de cada ponto para conexão de site com nomes de usuário, bytes, bytes para fora, endereço ip alocado etc.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="1ecc9-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ecc9-116">PARAMETERS</span></span>

### <span data-ttu-id="1ecc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecc9-117">-DefaultProfile</span></span>
<span data-ttu-id="1ecc9-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ecc9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ecc9-119">-InputObject</span></span>
<span data-ttu-id="1ecc9-120">O objeto gateway vpn p2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="1ecc9-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="1ecc9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1ecc9-121">-Name</span></span>
<span data-ttu-id="1ecc9-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-122">The resource name.</span></span>

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

### <span data-ttu-id="1ecc9-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="1ecc9-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="1ecc9-124">Url outputBlob Sas para a qual a saúde da conexão vpn p2s será escrita.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="1ecc9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecc9-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ecc9-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-126">The resource group name.</span></span>

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

### <span data-ttu-id="1ecc9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ecc9-127">-ResourceId</span></span>
<span data-ttu-id="1ecc9-128">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="1ecc9-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="1ecc9-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="1ecc9-130">A lista de nomes de usuário vpn P2S para filtrar.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="1ecc9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecc9-131">CommonParameters</span></span>
<span data-ttu-id="1ecc9-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecc9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecc9-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecc9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecc9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ecc9-134">INPUTS</span></span>

### <span data-ttu-id="1ecc9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1ecc9-135">System.String</span></span>
<span data-ttu-id="1ecc9-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1ecc9-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="1ecc9-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ecc9-137">OUTPUTS</span></span>

### <span data-ttu-id="1ecc9-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1ecc9-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="1ecc9-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ecc9-139">NOTES</span></span>

## <span data-ttu-id="1ecc9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ecc9-140">RELATED LINKS</span></span>
