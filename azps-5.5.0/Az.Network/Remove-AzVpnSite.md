---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117333"
---
# <span data-ttu-id="8492d-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8492d-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="8492d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8492d-102">SYNOPSIS</span></span>
<span data-ttu-id="8492d-103">Remove um recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="8492d-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="8492d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8492d-104">SYNTAX</span></span>

### <span data-ttu-id="8492d-105">ByVpnSiteName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8492d-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8492d-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="8492d-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8492d-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="8492d-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8492d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8492d-108">DESCRIPTION</span></span>
<span data-ttu-id="8492d-109">Remove um recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="8492d-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="8492d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8492d-110">EXAMPLES</span></span>

### <span data-ttu-id="8492d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8492d-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="8492d-112">O acima criará um grupo de recursos, Wan Virtual no oeste dos EUA, no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="8492d-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="8492d-113">Em seguida, ele cria um VpnSite para representar uma ramificação de cliente e a vincula à WAN Virtual.</span><span class="sxs-lookup"><span data-stu-id="8492d-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="8492d-114">Depois que o site é criado, ele é imediatamente removido usando o comando Remove-AzVpnSite usuário.</span><span class="sxs-lookup"><span data-stu-id="8492d-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="8492d-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8492d-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="8492d-116">O mesmo que o exemplo 1, mas aqui a remoção acontece usando a saída encadeada do Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="8492d-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="8492d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8492d-117">PARAMETERS</span></span>

### <span data-ttu-id="8492d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8492d-118">-DefaultProfile</span></span>
<span data-ttu-id="8492d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8492d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8492d-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8492d-120">-Force</span></span>
<span data-ttu-id="8492d-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8492d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8492d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8492d-122">-InputObject</span></span>
<span data-ttu-id="8492d-123">O objeto vpnSite a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8492d-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="8492d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8492d-124">-Name</span></span>
<span data-ttu-id="8492d-125">O nome do Site vpn.</span><span class="sxs-lookup"><span data-stu-id="8492d-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="8492d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8492d-126">-PassThru</span></span>
<span data-ttu-id="8492d-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8492d-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8492d-128">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="8492d-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8492d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8492d-129">-ResourceGroupName</span></span>
<span data-ttu-id="8492d-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8492d-130">The resource group name.</span></span>

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

### <span data-ttu-id="8492d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8492d-131">-ResourceId</span></span>
<span data-ttu-id="8492d-132">A ID de recurso do Azure para o Site vpn ser excluída.</span><span class="sxs-lookup"><span data-stu-id="8492d-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="8492d-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8492d-133">-Confirm</span></span>
<span data-ttu-id="8492d-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8492d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8492d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8492d-135">-WhatIf</span></span>
<span data-ttu-id="8492d-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8492d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8492d-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8492d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8492d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8492d-138">CommonParameters</span></span>
<span data-ttu-id="8492d-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8492d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8492d-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8492d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8492d-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="8492d-141">INPUTS</span></span>

### <span data-ttu-id="8492d-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="8492d-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="8492d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8492d-143">System.String</span></span>

## <span data-ttu-id="8492d-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="8492d-144">OUTPUTS</span></span>

### <span data-ttu-id="8492d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8492d-145">System.Boolean</span></span>

## <span data-ttu-id="8492d-146">Notas</span><span class="sxs-lookup"><span data-stu-id="8492d-146">NOTES</span></span>

## <span data-ttu-id="8492d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8492d-147">RELATED LINKS</span></span>

[<span data-ttu-id="8492d-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8492d-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="8492d-149">Novo-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8492d-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="8492d-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8492d-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
