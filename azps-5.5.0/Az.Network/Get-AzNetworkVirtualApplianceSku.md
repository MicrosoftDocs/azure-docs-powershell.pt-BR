---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115169"
---
# <span data-ttu-id="4e94c-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="4e94c-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="4e94c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e94c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e94c-103">Obter ou Listar SKIs de Dispositivo Virtual de Rede disponíveis no estoque.</span><span class="sxs-lookup"><span data-stu-id="4e94c-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="4e94c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e94c-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e94c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e94c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e94c-106">O Get-AzNetworkVirtualApplianceSku obtém ou lista as SKUs de Dispositivo Virtual de Rede disponíveis no inventário do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e94c-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="4e94c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e94c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e94c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e94c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="4e94c-109">Obter uma SKU por nome.</span><span class="sxs-lookup"><span data-stu-id="4e94c-109">Get a sku by name.</span></span>

### <span data-ttu-id="4e94c-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4e94c-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="4e94c-111">Listar todas as SKIs disponíveis do Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="4e94c-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="4e94c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e94c-112">PARAMETERS</span></span>

### <span data-ttu-id="4e94c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e94c-113">-DefaultProfile</span></span>
<span data-ttu-id="4e94c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e94c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e94c-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4e94c-115">-SkuName</span></span>
<span data-ttu-id="4e94c-116">O nome SKU.</span><span class="sxs-lookup"><span data-stu-id="4e94c-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e94c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e94c-117">CommonParameters</span></span>
<span data-ttu-id="4e94c-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e94c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e94c-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e94c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e94c-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="4e94c-120">INPUTS</span></span>

### <span data-ttu-id="4e94c-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4e94c-121">None</span></span>

## <span data-ttu-id="4e94c-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="4e94c-122">OUTPUTS</span></span>

### <span data-ttu-id="4e94c-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="4e94c-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="4e94c-124">Notas</span><span class="sxs-lookup"><span data-stu-id="4e94c-124">NOTES</span></span>

## <span data-ttu-id="4e94c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e94c-125">RELATED LINKS</span></span>
