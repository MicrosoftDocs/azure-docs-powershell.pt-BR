---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 50e335825fb43a85286be5f95696c1dd1a537129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886720"
---
# <span data-ttu-id="16b8c-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="16b8c-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="16b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="16b8c-103">Remove um recurso VpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="16b8c-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="16b8c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="16b8c-104">SYNTAX</span></span>

### <span data-ttu-id="16b8c-105">ByVpnSiteName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16b8c-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b8c-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="16b8c-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b8c-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="16b8c-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16b8c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="16b8c-108">DESCRIPTION</span></span>
<span data-ttu-id="16b8c-109">Remove um recurso VpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="16b8c-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="16b8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16b8c-110">EXAMPLES</span></span>

### <span data-ttu-id="16b8c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16b8c-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="16b8c-112">O acima criará um grupo de recursos, a WAN Virtual no Oeste dos EUA, no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="16b8c-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="16b8c-113">Em seguida, ele cria um VpnSite para representar uma filial de cliente e o vincula à WAN Virtual.</span><span class="sxs-lookup"><span data-stu-id="16b8c-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="16b8c-114">Depois que o site é criado, ele é imediatamente removido usando o comando Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="16b8c-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="16b8c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="16b8c-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="16b8c-116">O mesmo que o exemplo 1, mas aqui a remoção acontece usando a saída canalada do Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="16b8c-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="16b8c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="16b8c-117">PARAMETERS</span></span>

### <span data-ttu-id="16b8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b8c-118">-DefaultProfile</span></span>
<span data-ttu-id="16b8c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16b8c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b8c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="16b8c-120">-Force</span></span>
<span data-ttu-id="16b8c-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="16b8c-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16b8c-122">-InputObject</span></span>
<span data-ttu-id="16b8c-123">O objeto vpnSite a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="16b8c-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="16b8c-124">-Name</span></span>
<span data-ttu-id="16b8c-125">O nome vpnSite.</span><span class="sxs-lookup"><span data-stu-id="16b8c-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16b8c-126">-PassThru</span></span>
<span data-ttu-id="16b8c-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="16b8c-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="16b8c-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="16b8c-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b8c-129">-ResourceGroupName</span></span>
<span data-ttu-id="16b8c-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16b8c-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16b8c-131">-ResourceId</span></span>
<span data-ttu-id="16b8c-132">A ID de recurso do Azure para o vpnSite a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="16b8c-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16b8c-133">-Confirm</span></span>
<span data-ttu-id="16b8c-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16b8c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b8c-135">-WhatIf</span></span>
<span data-ttu-id="16b8c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16b8c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16b8c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16b8c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b8c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b8c-138">CommonParameters</span></span>
<span data-ttu-id="16b8c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b8c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b8c-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16b8c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b8c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16b8c-141">INPUTS</span></span>

### <span data-ttu-id="16b8c-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="16b8c-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="16b8c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="16b8c-143">System.String</span></span>

## <span data-ttu-id="16b8c-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="16b8c-144">OUTPUTS</span></span>

### <span data-ttu-id="16b8c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16b8c-145">System.Boolean</span></span>

## <span data-ttu-id="16b8c-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="16b8c-146">NOTES</span></span>

## <span data-ttu-id="16b8c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16b8c-147">RELATED LINKS</span></span>

[<span data-ttu-id="16b8c-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="16b8c-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="16b8c-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="16b8c-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="16b8c-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="16b8c-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
