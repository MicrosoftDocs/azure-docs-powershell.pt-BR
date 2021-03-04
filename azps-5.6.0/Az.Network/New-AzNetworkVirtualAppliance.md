---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3f95ad6b11e8ddf7baaf5bcdf312ec172a9d397a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892742"
---
# <span data-ttu-id="9d18b-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="9d18b-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="9d18b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d18b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d18b-103">Crie um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="9d18b-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="9d18b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9d18b-104">SYNTAX</span></span>

### <span data-ttu-id="9d18b-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9d18b-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d18b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d18b-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d18b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9d18b-107">DESCRIPTION</span></span>
<span data-ttu-id="9d18b-108">O New-AzNetworkVirtualAppliance cria um recurso de Dispositivo Virtual de Rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="9d18b-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="9d18b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d18b-109">EXAMPLES</span></span>

### <span data-ttu-id="9d18b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9d18b-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="9d18b-111">Cria um novo recurso de Dispositivo Virtual de Rede no grupo de recursos: testrg.</span><span class="sxs-lookup"><span data-stu-id="9d18b-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="9d18b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9d18b-112">PARAMETERS</span></span>

### <span data-ttu-id="9d18b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d18b-113">-AsJob</span></span>
<span data-ttu-id="9d18b-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9d18b-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="9d18b-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="9d18b-116">A URL de blob de configuração bootstrap.</span><span class="sxs-lookup"><span data-stu-id="9d18b-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d18b-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="9d18b-118">A configuração cloudinit como texto sem texto.</span><span class="sxs-lookup"><span data-stu-id="9d18b-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="9d18b-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="9d18b-120">A URL de armazenamento blob de configuração do Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="9d18b-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d18b-121">-DefaultProfile</span></span>
<span data-ttu-id="9d18b-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d18b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d18b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9d18b-123">-Force</span></span>
<span data-ttu-id="9d18b-124">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="9d18b-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="9d18b-125">-Identity</span></span>
<span data-ttu-id="9d18b-126">A identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="9d18b-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-127">-Location</span><span class="sxs-lookup"><span data-stu-id="9d18b-127">-Location</span></span>
<span data-ttu-id="9d18b-128">O local do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d18b-128">The public IP address location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9d18b-129">-Name</span></span>
<span data-ttu-id="9d18b-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9d18b-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d18b-131">-ResourceGroupName</span></span>
<span data-ttu-id="9d18b-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d18b-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d18b-133">-ResourceId</span></span>
<span data-ttu-id="9d18b-134">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9d18b-134">The resource Id.</span></span>

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

### <span data-ttu-id="9d18b-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="9d18b-135">-Sku</span></span>
<span data-ttu-id="9d18b-136">O Sku do Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="9d18b-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d18b-137">-Tag</span></span>
<span data-ttu-id="9d18b-138">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="9d18b-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="9d18b-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="9d18b-140">O número ASN do Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="9d18b-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="9d18b-141">-VirtualHubId</span></span>
<span data-ttu-id="9d18b-142">A ID de Recurso do Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="9d18b-142">The Resource Id of the Virtual Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d18b-143">-Confirm</span></span>
<span data-ttu-id="9d18b-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d18b-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d18b-145">-WhatIf</span></span>
<span data-ttu-id="9d18b-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d18b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d18b-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d18b-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d18b-148">CommonParameters</span></span>
<span data-ttu-id="9d18b-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d18b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d18b-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d18b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d18b-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d18b-151">INPUTS</span></span>

### <span data-ttu-id="9d18b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="9d18b-152">System.String</span></span>

### <span data-ttu-id="9d18b-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="9d18b-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="9d18b-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9d18b-154">System.Int32</span></span>

### <span data-ttu-id="9d18b-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="9d18b-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="9d18b-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9d18b-156">System.String[]</span></span>

### <span data-ttu-id="9d18b-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d18b-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d18b-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9d18b-158">OUTPUTS</span></span>

### <span data-ttu-id="9d18b-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="9d18b-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="9d18b-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="9d18b-160">NOTES</span></span>

## <span data-ttu-id="9d18b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d18b-161">RELATED LINKS</span></span>
