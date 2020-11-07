---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954859"
---
# <span data-ttu-id="16797-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="16797-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="16797-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16797-102">SYNOPSIS</span></span>
<span data-ttu-id="16797-103">Obtém a lista de todos os VpnServerConfigurations associados a este VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="16797-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="16797-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16797-104">SYNTAX</span></span>

### <span data-ttu-id="16797-105">ByVirtualWanName (padrão)</span><span class="sxs-lookup"><span data-stu-id="16797-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16797-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="16797-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16797-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="16797-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16797-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16797-108">DESCRIPTION</span></span>
<span data-ttu-id="16797-109">O cmdlet **Get-AzVirtualWanVpnServerConfiguration** retornará a lista de todos os VpnServerConfigurations associados a essa VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="16797-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="16797-110">ou seja, todos os VpnServerConfigurations que são anexados a qualquer P2SVpnGateways em VirutalHubs desse VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="16797-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="16797-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16797-111">EXAMPLES</span></span>

### <span data-ttu-id="16797-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16797-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="16797-113">OS</span><span class="sxs-lookup"><span data-stu-id="16797-113">PARAMETERS</span></span>

### <span data-ttu-id="16797-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16797-114">-DefaultProfile</span></span>
<span data-ttu-id="16797-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16797-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16797-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="16797-116">-Name</span></span>
<span data-ttu-id="16797-117">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="16797-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16797-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16797-118">-ResourceGroupName</span></span>
<span data-ttu-id="16797-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16797-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16797-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16797-120">-ResourceId</span></span>
<span data-ttu-id="16797-121">A ID de recurso do Azure para a rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="16797-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16797-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="16797-122">-VirtualWanObject</span></span>
<span data-ttu-id="16797-123">O objeto de WAN virtual.</span><span class="sxs-lookup"><span data-stu-id="16797-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16797-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16797-124">CommonParameters</span></span>
<span data-ttu-id="16797-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16797-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16797-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16797-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16797-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16797-127">INPUTS</span></span>

### <span data-ttu-id="16797-128">System. String</span><span class="sxs-lookup"><span data-stu-id="16797-128">System.String</span></span>
<span data-ttu-id="16797-129">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="16797-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="16797-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16797-130">OUTPUTS</span></span>

### <span data-ttu-id="16797-131">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="16797-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="16797-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16797-132">NOTES</span></span>

## <span data-ttu-id="16797-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16797-133">RELATED LINKS</span></span>
