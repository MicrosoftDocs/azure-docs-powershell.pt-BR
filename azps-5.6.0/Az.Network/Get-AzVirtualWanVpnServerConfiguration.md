---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 2919c007852961386fb1ab444e43d855ced2a8d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886916"
---
# <span data-ttu-id="ed7a5-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed7a5-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="ed7a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7a5-103">Obtém a lista de todos os VpnServerConfigurations associados a este VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="ed7a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed7a5-104">SYNTAX</span></span>

### <span data-ttu-id="ed7a5-105">ByVirtualWanName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed7a5-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed7a5-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ed7a5-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed7a5-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ed7a5-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed7a5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed7a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ed7a5-109">O cmdlet **Get-AzVirtualWanVpnServerConfiguration** retornará a lista de todos os VpnServerConfigurations associados a este VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="ed7a5-110">ou seja, todas as VpnServerConfigurations que estão anexadas a qualquer P2SVpnGateways em VirutalHubs deste VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="ed7a5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed7a5-111">EXAMPLES</span></span>

### <span data-ttu-id="ed7a5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed7a5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="ed7a5-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed7a5-113">PARAMETERS</span></span>

### <span data-ttu-id="ed7a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7a5-114">-DefaultProfile</span></span>
<span data-ttu-id="ed7a5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed7a5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ed7a5-116">-Name</span></span>
<span data-ttu-id="ed7a5-117">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-117">The resource name.</span></span>

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

### <span data-ttu-id="ed7a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="ed7a5-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-119">The resource group name.</span></span>

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

### <span data-ttu-id="ed7a5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed7a5-120">-ResourceId</span></span>
<span data-ttu-id="ed7a5-121">A ID de recurso do Azure para a wan virtual.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="ed7a5-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ed7a5-122">-VirtualWanObject</span></span>
<span data-ttu-id="ed7a5-123">O objeto wan virtual.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="ed7a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7a5-124">CommonParameters</span></span>
<span data-ttu-id="ed7a5-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7a5-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7a5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7a5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed7a5-127">INPUTS</span></span>

### <span data-ttu-id="ed7a5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ed7a5-128">System.String</span></span>
<span data-ttu-id="ed7a5-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ed7a5-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="ed7a5-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed7a5-130">OUTPUTS</span></span>

### <span data-ttu-id="ed7a5-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="ed7a5-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="ed7a5-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed7a5-132">NOTES</span></span>

## <span data-ttu-id="ed7a5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed7a5-133">RELATED LINKS</span></span>
