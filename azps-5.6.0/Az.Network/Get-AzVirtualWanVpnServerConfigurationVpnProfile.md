---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: e0a39aac53b13356eb9719cad6e2ade11483cfe7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889193"
---
# <span data-ttu-id="dc34d-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="dc34d-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="dc34d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc34d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc34d-103">Gera e baixa o perfil vpn no nível VirtualWan-VpnServerConfiguration configuração de cliente ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dc34d-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="dc34d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc34d-104">SYNTAX</span></span>

### <span data-ttu-id="dc34d-105">ByVirtualWanNameByVpnServerConfigurationObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc34d-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc34d-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="dc34d-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc34d-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dc34d-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc34d-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="dc34d-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc34d-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dc34d-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc34d-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="dc34d-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc34d-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc34d-111">DESCRIPTION</span></span>
<span data-ttu-id="dc34d-112">O cmdlet **Get-AzVirtualWanVpnServerConfigurationVpnProfile** permite que você gere e baixe o perfil vpn no nível VirtualWan-VpnServerConfiguration configuração do cliente ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dc34d-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="dc34d-113">Isso é necessário para a conectividade ponto a site de ponto para cliente de site para o Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="dc34d-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="dc34d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc34d-114">EXAMPLES</span></span>

### <span data-ttu-id="dc34d-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc34d-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="dc34d-116">O comando acima gerará e retornará a Url do SAS para o cliente baixar o perfil vpn no nível VirtualWan-VpnServerConfiguration para a configuração do cliente ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dc34d-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="dc34d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc34d-117">PARAMETERS</span></span>

### <span data-ttu-id="dc34d-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="dc34d-118">-AuthenticationMethod</span></span>
<span data-ttu-id="dc34d-119">Método Authentication</span><span class="sxs-lookup"><span data-stu-id="dc34d-119">Authentication Method</span></span>

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

### <span data-ttu-id="dc34d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc34d-120">-DefaultProfile</span></span>
<span data-ttu-id="dc34d-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc34d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc34d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dc34d-122">-Name</span></span>
<span data-ttu-id="dc34d-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dc34d-123">The resource name.</span></span>

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

### <span data-ttu-id="dc34d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc34d-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc34d-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc34d-125">The resource group name.</span></span>

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

### <span data-ttu-id="dc34d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc34d-126">-ResourceId</span></span>
<span data-ttu-id="dc34d-127">A ID de recurso do Azure para a wan virtual.</span><span class="sxs-lookup"><span data-stu-id="dc34d-127">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="dc34d-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="dc34d-128">-VirtualWanObject</span></span>
<span data-ttu-id="dc34d-129">O objeto wan virtual.</span><span class="sxs-lookup"><span data-stu-id="dc34d-129">The virtual wan object.</span></span>

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

### <span data-ttu-id="dc34d-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc34d-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="dc34d-131">O VpnServerConfiguration ao qual este VirtualWan está associado.</span><span class="sxs-lookup"><span data-stu-id="dc34d-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

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

### <span data-ttu-id="dc34d-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dc34d-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="dc34d-133">A id do objeto configuraiton do servidor Vpn que essa wan virtual será associada.</span><span class="sxs-lookup"><span data-stu-id="dc34d-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

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

### <span data-ttu-id="dc34d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc34d-134">CommonParameters</span></span>
<span data-ttu-id="dc34d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc34d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc34d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc34d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc34d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc34d-137">INPUTS</span></span>

### <span data-ttu-id="dc34d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dc34d-138">System.String</span></span>
<span data-ttu-id="dc34d-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc34d-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="dc34d-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc34d-140">OUTPUTS</span></span>

### <span data-ttu-id="dc34d-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="dc34d-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="dc34d-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc34d-142">NOTES</span></span>

## <span data-ttu-id="dc34d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc34d-143">RELATED LINKS</span></span>
