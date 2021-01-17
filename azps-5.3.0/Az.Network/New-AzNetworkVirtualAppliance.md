---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427575"
---
# <span data-ttu-id="161a2-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="161a2-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="161a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="161a2-102">SYNOPSIS</span></span>
<span data-ttu-id="161a2-103">Crie um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="161a2-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="161a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="161a2-104">SYNTAX</span></span>

### <span data-ttu-id="161a2-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="161a2-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="161a2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="161a2-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="161a2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="161a2-107">DESCRIPTION</span></span>
<span data-ttu-id="161a2-108">O comando New-AzNetworkVirtualAppliance cria um recurso de dispositivo virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="161a2-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="161a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="161a2-109">EXAMPLES</span></span>

### <span data-ttu-id="161a2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="161a2-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="161a2-111">Cria um novo recurso de dispositivo virtual de rede no grupo de recursos: testrg.</span><span class="sxs-lookup"><span data-stu-id="161a2-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="161a2-112">OS</span><span class="sxs-lookup"><span data-stu-id="161a2-112">PARAMETERS</span></span>

### <span data-ttu-id="161a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="161a2-113">-AsJob</span></span>
<span data-ttu-id="161a2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="161a2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="161a2-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="161a2-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="161a2-116">A URL do blob de configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="161a2-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="161a2-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="161a2-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="161a2-118">A configuração Cloudinit como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="161a2-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="161a2-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="161a2-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="161a2-120">A URL de armazenamento de blob de configuração do Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="161a2-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="161a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161a2-121">-DefaultProfile</span></span>
<span data-ttu-id="161a2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="161a2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="161a2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="161a2-123">-Force</span></span>
<span data-ttu-id="161a2-124">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="161a2-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="161a2-125">-Identidade</span><span class="sxs-lookup"><span data-stu-id="161a2-125">-Identity</span></span>
<span data-ttu-id="161a2-126">A identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="161a2-126">The Managed identity.</span></span>

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

### <span data-ttu-id="161a2-127">-Local</span><span class="sxs-lookup"><span data-stu-id="161a2-127">-Location</span></span>
<span data-ttu-id="161a2-128">O local do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="161a2-128">The public IP address location.</span></span>

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

### <span data-ttu-id="161a2-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="161a2-129">-Name</span></span>
<span data-ttu-id="161a2-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="161a2-130">The resource name.</span></span>

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

### <span data-ttu-id="161a2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161a2-131">-ResourceGroupName</span></span>
<span data-ttu-id="161a2-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="161a2-132">The resource group name.</span></span>

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

### <span data-ttu-id="161a2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="161a2-133">-ResourceId</span></span>
<span data-ttu-id="161a2-134">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="161a2-134">The resource Id.</span></span>

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

### <span data-ttu-id="161a2-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="161a2-135">-Sku</span></span>
<span data-ttu-id="161a2-136">A SKU do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="161a2-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="161a2-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="161a2-137">-Tag</span></span>
<span data-ttu-id="161a2-138">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="161a2-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="161a2-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="161a2-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="161a2-140">O número ASN do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="161a2-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="161a2-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="161a2-141">-VirtualHubId</span></span>
<span data-ttu-id="161a2-142">A ID do recurso do Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="161a2-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="161a2-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="161a2-143">-Confirm</span></span>
<span data-ttu-id="161a2-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="161a2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="161a2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="161a2-145">-WhatIf</span></span>
<span data-ttu-id="161a2-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="161a2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="161a2-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="161a2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="161a2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161a2-148">CommonParameters</span></span>
<span data-ttu-id="161a2-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="161a2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161a2-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="161a2-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161a2-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="161a2-151">INPUTS</span></span>

### <span data-ttu-id="161a2-152">System. String</span><span class="sxs-lookup"><span data-stu-id="161a2-152">System.String</span></span>

### <span data-ttu-id="161a2-153">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="161a2-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="161a2-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="161a2-154">System.Int32</span></span>

### <span data-ttu-id="161a2-155">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="161a2-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="161a2-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="161a2-156">System.String[]</span></span>

### <span data-ttu-id="161a2-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="161a2-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="161a2-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="161a2-158">OUTPUTS</span></span>

### <span data-ttu-id="161a2-159">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="161a2-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="161a2-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="161a2-160">NOTES</span></span>

## <span data-ttu-id="161a2-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="161a2-161">RELATED LINKS</span></span>
