---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: 62e549ef01f77382226eaf83784add7005516230
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901602"
---
# <span data-ttu-id="07183-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="07183-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="07183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07183-102">SYNOPSIS</span></span>
<span data-ttu-id="07183-103">Obter ou listar sites conectados aos recursos do Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="07183-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="07183-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07183-104">SYNTAX</span></span>

### <span data-ttu-id="07183-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07183-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07183-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07183-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07183-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07183-107">DESCRIPTION</span></span>
<span data-ttu-id="07183-108">O Get-AzVirtualApplianceSite obtém ou lista sites conectados a um ou mais recursos de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="07183-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="07183-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07183-109">EXAMPLES</span></span>

### <span data-ttu-id="07183-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07183-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="07183-111">Obter um recurso de site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="07183-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="07183-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07183-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="07183-113">Listar os recursos do site do Dispositivo Virtual em um Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="07183-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="07183-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07183-114">PARAMETERS</span></span>

### <span data-ttu-id="07183-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07183-115">-DefaultProfile</span></span>
<span data-ttu-id="07183-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07183-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07183-117">-Name</span><span class="sxs-lookup"><span data-stu-id="07183-117">-Name</span></span>
<span data-ttu-id="07183-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="07183-118">The resource name.</span></span>

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

### <span data-ttu-id="07183-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="07183-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="07183-120">O Dispositivo Virtual de Rede que o site está anexado.</span><span class="sxs-lookup"><span data-stu-id="07183-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="07183-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07183-121">-ResourceGroupName</span></span>
<span data-ttu-id="07183-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07183-122">The resource group name.</span></span>

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

### <span data-ttu-id="07183-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07183-123">-ResourceId</span></span>
<span data-ttu-id="07183-124">A ID de recurso do Site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="07183-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="07183-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07183-125">CommonParameters</span></span>
<span data-ttu-id="07183-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07183-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07183-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07183-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07183-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07183-128">INPUTS</span></span>

### <span data-ttu-id="07183-129">System.String</span><span class="sxs-lookup"><span data-stu-id="07183-129">System.String</span></span>

## <span data-ttu-id="07183-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07183-130">OUTPUTS</span></span>

### <span data-ttu-id="07183-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="07183-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="07183-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="07183-132">NOTES</span></span>

## <span data-ttu-id="07183-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07183-133">RELATED LINKS</span></span>
