---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110558"
---
# <span data-ttu-id="0a2e1-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="0a2e1-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="0a2e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2e1-103">Gera e retorna uma URL SAS para o cliente baixar o perfil de VPN da configuração do cliente do site para que ele tenha o ponto para a conectividade do site com o P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="0a2e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a2e1-104">SYNTAX</span></span>

### <span data-ttu-id="0a2e1-105">ByP2SVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a2e1-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a2e1-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0a2e1-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a2e1-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2e1-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a2e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a2e1-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2e1-109">O cmdlet **Get-AzP2sVpnGatewayVpnProfile** permite gerar e obter uma URL SAS para o cliente baixar o perfil VPN da configuração do site do cliente para o site para que ele tenha o ponto para a conectividade do site com o P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="0a2e1-110">A configuração de cliente do site que usa esse perfil VPN pode se conectar a esse P2SVpnGateway específico apenas.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="0a2e1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a2e1-111">EXAMPLES</span></span>

### <span data-ttu-id="0a2e1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a2e1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="0a2e1-113">O cmdlet **Get-AzP2sVpnGatewayVpnProfile** permite gerar e obter uma URL SAS para o cliente baixar o perfil VPN da configuração do site do cliente para o site para que ele tenha o ponto para a conectividade do site com o P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="0a2e1-114">O ProfileUrl mostra a URL da SAS a partir da qual o cliente pode baixar o perfil da VPN para a configuração do cliente do site do Point.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="0a2e1-115">OS</span><span class="sxs-lookup"><span data-stu-id="0a2e1-115">PARAMETERS</span></span>

### <span data-ttu-id="0a2e1-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="0a2e1-116">-AuthenticationMethod</span></span>
<span data-ttu-id="0a2e1-117">Método de autenticação</span><span class="sxs-lookup"><span data-stu-id="0a2e1-117">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2e1-118">-DefaultProfile</span></span>
<span data-ttu-id="0a2e1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a2e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a2e1-120">-InputObject</span></span>
<span data-ttu-id="0a2e1-121">O objeto de gateway de VPN P2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="0a2e1-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="0a2e1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a2e1-122">-Name</span></span>
<span data-ttu-id="0a2e1-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-123">The resource name.</span></span>

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

### <span data-ttu-id="0a2e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a2e1-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-125">The resource group name.</span></span>

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

### <span data-ttu-id="0a2e1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2e1-126">-ResourceId</span></span>
<span data-ttu-id="0a2e1-127">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="0a2e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2e1-128">CommonParameters</span></span>
<span data-ttu-id="0a2e1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2e1-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2e1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2e1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a2e1-131">INPUTS</span></span>

### <span data-ttu-id="0a2e1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0a2e1-132">System.String</span></span>
<span data-ttu-id="0a2e1-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0a2e1-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="0a2e1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a2e1-134">OUTPUTS</span></span>

### <span data-ttu-id="0a2e1-135">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="0a2e1-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="0a2e1-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a2e1-136">NOTES</span></span>

## <span data-ttu-id="0a2e1-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a2e1-137">RELATED LINKS</span></span>
