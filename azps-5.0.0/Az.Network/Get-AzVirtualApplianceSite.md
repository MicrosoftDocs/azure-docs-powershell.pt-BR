---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282212"
---
# <span data-ttu-id="ab5fb-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ab5fb-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="ab5fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5fb-103">Obter ou listar sites conectados a um (s) recurso (s) de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="ab5fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab5fb-104">SYNTAX</span></span>

### <span data-ttu-id="ab5fb-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab5fb-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab5fb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab5fb-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab5fb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab5fb-107">DESCRIPTION</span></span>
<span data-ttu-id="ab5fb-108">O Get-AzVirtualApplianceSite Obtém ou lista os sites conectados a um ou mais recursos de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="ab5fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab5fb-109">EXAMPLES</span></span>

### <span data-ttu-id="ab5fb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab5fb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="ab5fb-111">Obter um recurso de site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="ab5fb-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ab5fb-112">Example 2</span></span>
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

<span data-ttu-id="ab5fb-113">Listar recursos do site de dispositivos virtuais em um aplicativo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="ab5fb-114">OS</span><span class="sxs-lookup"><span data-stu-id="ab5fb-114">PARAMETERS</span></span>

### <span data-ttu-id="ab5fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab5fb-115">-DefaultProfile</span></span>
<span data-ttu-id="ab5fb-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab5fb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab5fb-117">-Name</span></span>
<span data-ttu-id="ab5fb-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-118">The resource name.</span></span>

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

### <span data-ttu-id="ab5fb-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="ab5fb-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="ab5fb-120">O dispositivo virtual de rede no qual o site está anexado.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="ab5fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab5fb-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-122">The resource group name.</span></span>

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

### <span data-ttu-id="ab5fb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab5fb-123">-ResourceId</span></span>
<span data-ttu-id="ab5fb-124">A ID do recurso do site de dispositivos virtuais.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="ab5fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5fb-125">CommonParameters</span></span>
<span data-ttu-id="ab5fb-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab5fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5fb-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab5fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5fb-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab5fb-128">INPUTS</span></span>

### <span data-ttu-id="ab5fb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ab5fb-129">System.String</span></span>

## <span data-ttu-id="ab5fb-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab5fb-130">OUTPUTS</span></span>

### <span data-ttu-id="ab5fb-131">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ab5fb-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="ab5fb-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab5fb-132">NOTES</span></span>

## <span data-ttu-id="ab5fb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab5fb-133">RELATED LINKS</span></span>
