---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430133"
---
# <span data-ttu-id="a4cec-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="a4cec-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="a4cec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4cec-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cec-103">Remove um recurso do VpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cec-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4cec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4cec-104">SYNTAX</span></span>

### <span data-ttu-id="a4cec-105">ByVpnSiteName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a4cec-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4cec-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="a4cec-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4cec-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cec-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4cec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4cec-108">DESCRIPTION</span></span>
<span data-ttu-id="a4cec-109">Remove um recurso do VpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cec-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="a4cec-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4cec-110">EXAMPLES</span></span>

### <span data-ttu-id="a4cec-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4cec-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="a4cec-112">A seguir, você criará um grupo de recursos, uma WAN virtual no oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cec-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="a4cec-113">Em seguida, ele cria um VpnSite para representar uma ramificação do cliente e a vincula à rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="a4cec-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="a4cec-114">Depois que o site for criado, ele será removido imediatamente usando o comando Remove-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="a4cec-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="a4cec-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a4cec-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="a4cec-116">Mesmo que o exemplo 1, mas aqui, a remoção ocorre usando a saída de pipe do Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="a4cec-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="a4cec-117">OS</span><span class="sxs-lookup"><span data-stu-id="a4cec-117">PARAMETERS</span></span>

### <span data-ttu-id="a4cec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cec-118">-DefaultProfile</span></span>
<span data-ttu-id="a4cec-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cec-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a4cec-120">-Force</span></span>
<span data-ttu-id="a4cec-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a4cec-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a4cec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4cec-122">-InputObject</span></span>
<span data-ttu-id="a4cec-123">O objeto vpnSite a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="a4cec-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="a4cec-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4cec-124">-Name</span></span>
<span data-ttu-id="a4cec-125">O nome vpnSite.</span><span class="sxs-lookup"><span data-stu-id="a4cec-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="a4cec-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4cec-126">-PassThru</span></span>
<span data-ttu-id="a4cec-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a4cec-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a4cec-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a4cec-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4cec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cec-129">-ResourceGroupName</span></span>
<span data-ttu-id="a4cec-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4cec-130">The resource group name.</span></span>

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

### <span data-ttu-id="a4cec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cec-131">-ResourceId</span></span>
<span data-ttu-id="a4cec-132">A ID de recurso do Azure para o vpnSite a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="a4cec-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="a4cec-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a4cec-133">-Confirm</span></span>
<span data-ttu-id="a4cec-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4cec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4cec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4cec-135">-WhatIf</span></span>
<span data-ttu-id="a4cec-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4cec-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4cec-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4cec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4cec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cec-138">CommonParameters</span></span>
<span data-ttu-id="a4cec-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cec-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4cec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cec-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4cec-141">INPUTS</span></span>

### <span data-ttu-id="a4cec-142">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="a4cec-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="a4cec-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a4cec-143">System.String</span></span>

## <span data-ttu-id="a4cec-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4cec-144">OUTPUTS</span></span>

### <span data-ttu-id="a4cec-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4cec-145">System.Boolean</span></span>

## <span data-ttu-id="a4cec-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4cec-146">NOTES</span></span>

## <span data-ttu-id="a4cec-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4cec-147">RELATED LINKS</span></span>
