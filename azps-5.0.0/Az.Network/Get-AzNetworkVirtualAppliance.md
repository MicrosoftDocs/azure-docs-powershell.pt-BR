---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115984"
---
# <span data-ttu-id="77f73-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="77f73-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="77f73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77f73-102">SYNOPSIS</span></span>
<span data-ttu-id="77f73-103">Obter ou listar dispositivos virtuais de rede.</span><span class="sxs-lookup"><span data-stu-id="77f73-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="77f73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77f73-104">SYNTAX</span></span>

### <span data-ttu-id="77f73-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="77f73-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77f73-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77f73-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77f73-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77f73-107">DESCRIPTION</span></span>
<span data-ttu-id="77f73-108">Os comandos Get-AzNetworkVirtualAppliance Obtém ou lista recursos de dispositivos virtuais da rede.</span><span class="sxs-lookup"><span data-stu-id="77f73-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="77f73-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77f73-109">EXAMPLES</span></span>

### <span data-ttu-id="77f73-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77f73-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="77f73-111">Obter um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="77f73-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="77f73-112">OS</span><span class="sxs-lookup"><span data-stu-id="77f73-112">PARAMETERS</span></span>

### <span data-ttu-id="77f73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f73-113">-DefaultProfile</span></span>
<span data-ttu-id="77f73-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77f73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f73-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="77f73-115">-Name</span></span>
<span data-ttu-id="77f73-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="77f73-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f73-117">-ResourceGroupName</span></span>
<span data-ttu-id="77f73-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="77f73-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f73-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77f73-119">-ResourceId</span></span>
<span data-ttu-id="77f73-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="77f73-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f73-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f73-121">CommonParameters</span></span>
<span data-ttu-id="77f73-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f73-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f73-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77f73-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f73-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77f73-124">INPUTS</span></span>

### <span data-ttu-id="77f73-125">System. String</span><span class="sxs-lookup"><span data-stu-id="77f73-125">System.String</span></span>

## <span data-ttu-id="77f73-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77f73-126">OUTPUTS</span></span>

### <span data-ttu-id="77f73-127">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="77f73-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="77f73-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77f73-128">NOTES</span></span>

## <span data-ttu-id="77f73-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77f73-129">RELATED LINKS</span></span>
