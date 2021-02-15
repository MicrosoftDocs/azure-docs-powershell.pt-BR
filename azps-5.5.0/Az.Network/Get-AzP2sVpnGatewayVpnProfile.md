---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115156"
---
# <span data-ttu-id="8f91a-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="8f91a-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="8f91a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f91a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f91a-103">Gera e retorna uma URL do SAS para o cliente baixar o perfil vpn para que a configuração do cliente aponte para o site e aponte para a conectividade do site com o P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8f91a-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="8f91a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f91a-104">SYNTAX</span></span>

### <span data-ttu-id="8f91a-105">ByP2SVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f91a-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f91a-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8f91a-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f91a-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8f91a-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f91a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f91a-108">DESCRIPTION</span></span>
<span data-ttu-id="8f91a-109">O cmdlet **Get-AzP2sVpnGatewayVpnProfile** permite que você gere e receba uma URL do SAS para que o cliente baixe o perfil vpn para que a configuração do cliente aponte para o site e tenha um ponto de conectividade com o P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8f91a-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="8f91a-110">Aponte para a configuração do cliente de site usando este perfil vpn pode se conectar somente a esse P2SVpnGateway específico.</span><span class="sxs-lookup"><span data-stu-id="8f91a-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="8f91a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f91a-111">EXAMPLES</span></span>

### <span data-ttu-id="8f91a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f91a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="8f91a-113">O cmdlet **Get-AzP2sVpnGatewayVpnProfile** permite que você gere e receba uma URL do SAS para que o cliente baixe o perfil vpn para que a configuração do cliente aponte para o site e tenha um ponto de conectividade com o P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8f91a-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="8f91a-114">ProfileUrl mostra a URL do SAS de onde o cliente pode baixar o perfil vpn para configurar o cliente de ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="8f91a-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="8f91a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f91a-115">PARAMETERS</span></span>

### <span data-ttu-id="8f91a-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="8f91a-116">-AuthenticationMethod</span></span>
<span data-ttu-id="8f91a-117">Método de Autenticação</span><span class="sxs-lookup"><span data-stu-id="8f91a-117">Authentication Method</span></span>

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

### <span data-ttu-id="8f91a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f91a-118">-DefaultProfile</span></span>
<span data-ttu-id="8f91a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f91a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f91a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f91a-120">-InputObject</span></span>
<span data-ttu-id="8f91a-121">O objeto de gateway de vpn p2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="8f91a-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="8f91a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f91a-122">-Name</span></span>
<span data-ttu-id="8f91a-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="8f91a-123">The resource name.</span></span>

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

### <span data-ttu-id="8f91a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f91a-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f91a-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f91a-125">The resource group name.</span></span>

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

### <span data-ttu-id="8f91a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f91a-126">-ResourceId</span></span>
<span data-ttu-id="8f91a-127">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="8f91a-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="8f91a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f91a-128">CommonParameters</span></span>
<span data-ttu-id="8f91a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f91a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f91a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f91a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f91a-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f91a-131">INPUTS</span></span>

### <span data-ttu-id="8f91a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8f91a-132">System.String</span></span>
<span data-ttu-id="8f91a-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8f91a-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="8f91a-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f91a-134">OUTPUTS</span></span>

### <span data-ttu-id="8f91a-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="8f91a-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="8f91a-136">Notas</span><span class="sxs-lookup"><span data-stu-id="8f91a-136">NOTES</span></span>

## <span data-ttu-id="8f91a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f91a-137">RELATED LINKS</span></span>
