---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112862"
---
# <span data-ttu-id="a5b7d-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5b7d-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="a5b7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b7d-103">Obtém uma WAN Virtual ou todos os WANs Virtuais em um grupo de recursos ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="a5b7d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5b7d-104">SYNTAX</span></span>

### <span data-ttu-id="a5b7d-105">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a5b7d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5b7d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b7d-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b7d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5b7d-107">DESCRIPTION</span></span>
<span data-ttu-id="a5b7d-108">Obtém uma WAN Virtual ou todos os WANs Virtuais em um grupo de recursos ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="a5b7d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5b7d-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b7d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5b7d-110">Example 1</span></span>

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

<span data-ttu-id="a5b7d-111">Esse comando obtém a WAN Virtual nomeada myVirtualWAN no testRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="a5b7d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a5b7d-112">Example 2</span></span>

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

<span data-ttu-id="a5b7d-113">Esse comando obtém todos os WANs Virtuais começando com "teste".</span><span class="sxs-lookup"><span data-stu-id="a5b7d-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="a5b7d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5b7d-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b7d-115">-DefaultProfile</span></span>
<span data-ttu-id="a5b7d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b7d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5b7d-117">-Name</span></span>
<span data-ttu-id="a5b7d-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-118">The resource name.</span></span>

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

### <span data-ttu-id="a5b7d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b7d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5b7d-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-120">The resource group name.</span></span>

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

### <span data-ttu-id="a5b7d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b7d-121">CommonParameters</span></span>
<span data-ttu-id="a5b7d-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b7d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b7d-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5b7d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b7d-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="a5b7d-124">INPUTS</span></span>

### <span data-ttu-id="a5b7d-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a5b7d-125">None</span></span>

## <span data-ttu-id="a5b7d-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="a5b7d-126">OUTPUTS</span></span>

### <span data-ttu-id="a5b7d-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5b7d-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="a5b7d-128">Notas</span><span class="sxs-lookup"><span data-stu-id="a5b7d-128">NOTES</span></span>

## <span data-ttu-id="a5b7d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5b7d-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5b7d-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5b7d-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="a5b7d-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5b7d-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="a5b7d-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5b7d-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
