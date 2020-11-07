---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955871"
---
# <span data-ttu-id="b71b2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="b71b2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="b71b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b71b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b71b2-103">Gera e baixa o perfil VPN em nível VirtualWan-VpnServerConfiguration para a configuração do cliente do site.</span><span class="sxs-lookup"><span data-stu-id="b71b2-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="b71b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b71b2-104">SYNTAX</span></span>

### <span data-ttu-id="b71b2-105">ByVirtualWanNameByVpnServerConfigurationObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="b71b2-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71b2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b71b2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b71b2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b71b2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71b2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b71b2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b71b2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b71b2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71b2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b71b2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b71b2-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b71b2-111">DESCRIPTION</span></span>
<span data-ttu-id="b71b2-112">O cmdlet **Get-AzVirtualWanVpnServerConfigurationVpnProfile** permite que você gere e baixe o perfil de VPN em nível VirtualWan-VpnServerConfiguration para a configuração do cliente do site.</span><span class="sxs-lookup"><span data-stu-id="b71b2-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="b71b2-113">Isso é necessário para a conectividade do site ponto a ponto para o cliente do site para o P2SVpnGateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="b71b2-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="b71b2-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b71b2-114">EXAMPLES</span></span>

### <span data-ttu-id="b71b2-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b71b2-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="b71b2-116">O comando acima gerará e retornará a URL SAS para o cliente baixar o perfil VPN em nível VirtualWan-VpnServerConfiguration para configuração do cliente do site.</span><span class="sxs-lookup"><span data-stu-id="b71b2-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="b71b2-117">OS</span><span class="sxs-lookup"><span data-stu-id="b71b2-117">PARAMETERS</span></span>

### <span data-ttu-id="b71b2-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="b71b2-118">-AuthenticationMethod</span></span>
<span data-ttu-id="b71b2-119">Método de autenticação</span><span class="sxs-lookup"><span data-stu-id="b71b2-119">Authentication Method</span></span>

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

### <span data-ttu-id="b71b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71b2-120">-DefaultProfile</span></span>
<span data-ttu-id="b71b2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b71b2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b71b2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b71b2-122">-Name</span></span>
<span data-ttu-id="b71b2-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b71b2-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b71b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b71b2-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b71b2-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b71b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b71b2-126">-ResourceId</span></span>
<span data-ttu-id="b71b2-127">A ID de recurso do Azure para a rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="b71b2-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b2-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="b71b2-128">-VirtualWanObject</span></span>
<span data-ttu-id="b71b2-129">O objeto de WAN virtual.</span><span class="sxs-lookup"><span data-stu-id="b71b2-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b2-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b71b2-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="b71b2-131">O VpnServerConfiguration com o qual este VirtualWan está associado.</span><span class="sxs-lookup"><span data-stu-id="b71b2-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b2-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b71b2-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="b71b2-133">A ID do servidor VPN configuraiton o objeto com o qual essa Wan virtual estará associada.</span><span class="sxs-lookup"><span data-stu-id="b71b2-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71b2-134">CommonParameters</span></span>
<span data-ttu-id="b71b2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71b2-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71b2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71b2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b71b2-137">INPUTS</span></span>

### <span data-ttu-id="b71b2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b71b2-138">System.String</span></span>
<span data-ttu-id="b71b2-139">Microsoft. Azure. Commands. Network. Models. PSVirtualWan Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b71b2-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b71b2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b71b2-140">OUTPUTS</span></span>

### <span data-ttu-id="b71b2-141">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="b71b2-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="b71b2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b71b2-142">NOTES</span></span>

## <span data-ttu-id="b71b2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b71b2-143">RELATED LINKS</span></span>
