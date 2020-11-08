---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116900"
---
# <span data-ttu-id="58c04-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="58c04-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="58c04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58c04-102">SYNOPSIS</span></span>
<span data-ttu-id="58c04-103">Obtém uma WAN virtual ou todas as WANs virtuais em um grupo de recursos ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="58c04-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="58c04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c04-104">SYNTAX</span></span>

### <span data-ttu-id="58c04-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="58c04-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c04-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c04-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58c04-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58c04-107">DESCRIPTION</span></span>
<span data-ttu-id="58c04-108">Obtém uma WAN virtual ou todas as WANs virtuais em um grupo de recursos ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="58c04-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="58c04-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58c04-109">EXAMPLES</span></span>

### <span data-ttu-id="58c04-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58c04-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="58c04-111">Esse comando obtém a WAN virtual chamada myVirtualWAN na testRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58c04-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="58c04-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="58c04-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="58c04-113">Esse comando obtém todas as WANs virtuais começando com "Test".</span><span class="sxs-lookup"><span data-stu-id="58c04-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="58c04-114">OS</span><span class="sxs-lookup"><span data-stu-id="58c04-114">PARAMETERS</span></span>

### <span data-ttu-id="58c04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c04-115">-DefaultProfile</span></span>
<span data-ttu-id="58c04-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58c04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c04-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="58c04-117">-Name</span></span>
<span data-ttu-id="58c04-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="58c04-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="58c04-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c04-119">-ResourceGroupName</span></span>
<span data-ttu-id="58c04-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58c04-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="58c04-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c04-121">CommonParameters</span></span>
<span data-ttu-id="58c04-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c04-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c04-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58c04-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c04-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58c04-124">INPUTS</span></span>

### <span data-ttu-id="58c04-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="58c04-125">None</span></span>

## <span data-ttu-id="58c04-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58c04-126">OUTPUTS</span></span>

### <span data-ttu-id="58c04-127">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="58c04-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="58c04-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58c04-128">NOTES</span></span>

## <span data-ttu-id="58c04-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58c04-129">RELATED LINKS</span></span>

[<span data-ttu-id="58c04-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="58c04-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="58c04-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="58c04-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="58c04-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="58c04-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
