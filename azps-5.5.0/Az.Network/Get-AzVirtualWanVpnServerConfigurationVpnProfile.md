---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114700"
---
# <span data-ttu-id="df5ab-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="df5ab-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="df5ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="df5ab-103">Gera e baixa o perfil vpn no nível VirtualWan-VpnServerConfiguration para a configuração do cliente ponto a site.</span><span class="sxs-lookup"><span data-stu-id="df5ab-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="df5ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df5ab-104">SYNTAX</span></span>

### <span data-ttu-id="df5ab-105">ByVirtualWanNameByVpnServerConfigurationObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df5ab-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5ab-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="df5ab-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df5ab-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="df5ab-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5ab-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="df5ab-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df5ab-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="df5ab-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5ab-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="df5ab-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df5ab-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="df5ab-111">DESCRIPTION</span></span>
<span data-ttu-id="df5ab-112">O cmdlet **Get-AzVirtualWanVpnServerConfigurationVpnProfile** permite que você gere e baixe o perfil vpn no nível VirtualWan-VpnServerConfiguration para a configuração do cliente Ponto para site.</span><span class="sxs-lookup"><span data-stu-id="df5ab-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="df5ab-113">Isso é necessário para a conectividade De Ponto para Site, do cliente Ponto ao site para o Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="df5ab-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="df5ab-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df5ab-114">EXAMPLES</span></span>

### <span data-ttu-id="df5ab-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df5ab-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="df5ab-116">O comando acima gerará e retornará a Url do SAS para que o cliente baixe o perfil vpn no nível VirtualWan-VpnServerConfiguration para a configuração do cliente Ponto para site.</span><span class="sxs-lookup"><span data-stu-id="df5ab-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="df5ab-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df5ab-117">PARAMETERS</span></span>

### <span data-ttu-id="df5ab-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="df5ab-118">-AuthenticationMethod</span></span>
<span data-ttu-id="df5ab-119">Método de Autenticação</span><span class="sxs-lookup"><span data-stu-id="df5ab-119">Authentication Method</span></span>

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

### <span data-ttu-id="df5ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5ab-120">-DefaultProfile</span></span>
<span data-ttu-id="df5ab-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df5ab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df5ab-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="df5ab-122">-Name</span></span>
<span data-ttu-id="df5ab-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="df5ab-123">The resource name.</span></span>

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

### <span data-ttu-id="df5ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="df5ab-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df5ab-125">The resource group name.</span></span>

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

### <span data-ttu-id="df5ab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df5ab-126">-ResourceId</span></span>
<span data-ttu-id="df5ab-127">A ID de recurso do Azure para a wan virtual.</span><span class="sxs-lookup"><span data-stu-id="df5ab-127">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="df5ab-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="df5ab-128">-VirtualWanObject</span></span>
<span data-ttu-id="df5ab-129">O objeto wan virtual.</span><span class="sxs-lookup"><span data-stu-id="df5ab-129">The virtual wan object.</span></span>

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

### <span data-ttu-id="df5ab-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="df5ab-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="df5ab-131">A VpnServerConfiguration à qual este VirtualWan está associado.</span><span class="sxs-lookup"><span data-stu-id="df5ab-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

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

### <span data-ttu-id="df5ab-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="df5ab-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="df5ab-133">A id do objeto de configuração do servidor Vpn com o que essa wan virtual será associada.</span><span class="sxs-lookup"><span data-stu-id="df5ab-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

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

### <span data-ttu-id="df5ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5ab-134">CommonParameters</span></span>
<span data-ttu-id="df5ab-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5ab-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5ab-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5ab-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="df5ab-137">INPUTS</span></span>

### <span data-ttu-id="df5ab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="df5ab-138">System.String</span></span>
<span data-ttu-id="df5ab-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="df5ab-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="df5ab-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="df5ab-140">OUTPUTS</span></span>

### <span data-ttu-id="df5ab-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="df5ab-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="df5ab-142">Notas</span><span class="sxs-lookup"><span data-stu-id="df5ab-142">NOTES</span></span>

## <span data-ttu-id="df5ab-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df5ab-143">RELATED LINKS</span></span>
