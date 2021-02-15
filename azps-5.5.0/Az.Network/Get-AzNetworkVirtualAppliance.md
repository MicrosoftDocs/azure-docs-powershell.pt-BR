---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114705"
---
# <span data-ttu-id="11ffe-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="11ffe-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="11ffe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="11ffe-103">Obter ou listar dispositivos virtuais de rede.</span><span class="sxs-lookup"><span data-stu-id="11ffe-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="11ffe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11ffe-104">SYNTAX</span></span>

### <span data-ttu-id="11ffe-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11ffe-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ffe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11ffe-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11ffe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11ffe-107">DESCRIPTION</span></span>
<span data-ttu-id="11ffe-108">Os Get-AzNetworkVirtualAppliance comandos são ou listam os recursos de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="11ffe-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="11ffe-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11ffe-109">EXAMPLES</span></span>

### <span data-ttu-id="11ffe-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11ffe-110">Example 1</span></span>
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

<span data-ttu-id="11ffe-111">Obter um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="11ffe-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="11ffe-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11ffe-112">PARAMETERS</span></span>

### <span data-ttu-id="11ffe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ffe-113">-DefaultProfile</span></span>
<span data-ttu-id="11ffe-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11ffe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ffe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="11ffe-115">-Name</span></span>
<span data-ttu-id="11ffe-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="11ffe-116">The resource name.</span></span>

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

### <span data-ttu-id="11ffe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ffe-117">-ResourceGroupName</span></span>
<span data-ttu-id="11ffe-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11ffe-118">The resource group name.</span></span>

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

### <span data-ttu-id="11ffe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ffe-119">-ResourceId</span></span>
<span data-ttu-id="11ffe-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="11ffe-120">The resource Id.</span></span>

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

### <span data-ttu-id="11ffe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ffe-121">CommonParameters</span></span>
<span data-ttu-id="11ffe-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ffe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ffe-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11ffe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ffe-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="11ffe-124">INPUTS</span></span>

### <span data-ttu-id="11ffe-125">System.String</span><span class="sxs-lookup"><span data-stu-id="11ffe-125">System.String</span></span>

## <span data-ttu-id="11ffe-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="11ffe-126">OUTPUTS</span></span>

### <span data-ttu-id="11ffe-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="11ffe-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="11ffe-128">Notas</span><span class="sxs-lookup"><span data-stu-id="11ffe-128">NOTES</span></span>

## <span data-ttu-id="11ffe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11ffe-129">RELATED LINKS</span></span>
