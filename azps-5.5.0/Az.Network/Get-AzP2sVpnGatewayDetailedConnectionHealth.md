---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115160"
---
# <span data-ttu-id="173e7-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="173e7-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="173e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="173e7-102">SYNOPSIS</span></span>
<span data-ttu-id="173e7-103">Obtém as informações detalhadas do ponto atual para as conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="173e7-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="173e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="173e7-104">SYNTAX</span></span>

### <span data-ttu-id="173e7-105">ByP2SVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="173e7-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="173e7-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="173e7-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="173e7-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="173e7-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="173e7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="173e7-108">DESCRIPTION</span></span>
<span data-ttu-id="173e7-109">O cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** permite que você receba as informações detalhadas do ponto atual para as conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="173e7-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="173e7-110">O cliente precisa passar a URL do SAS onde podemos colocar essas informações de saúde detalhadas.</span><span class="sxs-lookup"><span data-stu-id="173e7-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="173e7-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="173e7-111">EXAMPLES</span></span>

### <span data-ttu-id="173e7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="173e7-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="173e7-113">O cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** permite que você receba as informações detalhadas do ponto atual para as conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="173e7-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="173e7-114">O cliente pode baixar detalhes de saúde do download de URL do SAS aprovado.</span><span class="sxs-lookup"><span data-stu-id="173e7-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="173e7-115">Isso mostrará informações de cada ponto para a conexão do site com nomes de usuário, bytes de, bytes para fora, endereço IP alocado etc.</span><span class="sxs-lookup"><span data-stu-id="173e7-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="173e7-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="173e7-116">PARAMETERS</span></span>

### <span data-ttu-id="173e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="173e7-117">-DefaultProfile</span></span>
<span data-ttu-id="173e7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="173e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="173e7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="173e7-119">-InputObject</span></span>
<span data-ttu-id="173e7-120">O objeto de gateway de vpn p2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="173e7-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="173e7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="173e7-121">-Name</span></span>
<span data-ttu-id="173e7-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="173e7-122">The resource name.</span></span>

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

### <span data-ttu-id="173e7-123">-OutputBlabSasUrl</span><span class="sxs-lookup"><span data-stu-id="173e7-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="173e7-124">Url outputB url Sas para a qual a saúde da conexão vpn p2s será escrita.</span><span class="sxs-lookup"><span data-stu-id="173e7-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="173e7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="173e7-125">-ResourceGroupName</span></span>
<span data-ttu-id="173e7-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="173e7-126">The resource group name.</span></span>

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

### <span data-ttu-id="173e7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="173e7-127">-ResourceId</span></span>
<span data-ttu-id="173e7-128">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="173e7-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="173e7-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="173e7-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="173e7-130">A lista de nomes de usuário de vpn P2S para filtrar.</span><span class="sxs-lookup"><span data-stu-id="173e7-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="173e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="173e7-131">CommonParameters</span></span>
<span data-ttu-id="173e7-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="173e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="173e7-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="173e7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="173e7-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="173e7-134">INPUTS</span></span>

### <span data-ttu-id="173e7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="173e7-135">System.String</span></span>
<span data-ttu-id="173e7-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="173e7-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="173e7-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="173e7-137">OUTPUTS</span></span>

### <span data-ttu-id="173e7-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="173e7-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="173e7-139">Notas</span><span class="sxs-lookup"><span data-stu-id="173e7-139">NOTES</span></span>

## <span data-ttu-id="173e7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="173e7-140">RELATED LINKS</span></span>
