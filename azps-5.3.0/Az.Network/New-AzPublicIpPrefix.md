---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427550"
---
# <span data-ttu-id="7f9ad-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="7f9ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9ad-103">Cria um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="7f9ad-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="7f9ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f9ad-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f9ad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f9ad-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9ad-106">O cmdlet **New-AzPublicIpPrefix** cria um prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="7f9ad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f9ad-107">EXAMPLES</span></span>

### <span data-ttu-id="7f9ad-108">Exemplo 1: criar um novo prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="7f9ad-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="7f9ad-109">Esse comando cria um novo recurso de prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="7f9ad-110">Exemplo 2: criar um novo prefixo de IP público global</span><span class="sxs-lookup"><span data-stu-id="7f9ad-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="7f9ad-111">Esse comando cria um novo recurso de prefixo de IP público global.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="7f9ad-112">OS</span><span class="sxs-lookup"><span data-stu-id="7f9ad-112">PARAMETERS</span></span>

### <span data-ttu-id="7f9ad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f9ad-113">-AsJob</span></span>
<span data-ttu-id="7f9ad-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7f9ad-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f9ad-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-115">-CustomIpPrefix</span></span>
<span data-ttu-id="7f9ad-116">O CustomIpPrefix ao qual este PublicIpPrefix será associado</span><span class="sxs-lookup"><span data-stu-id="7f9ad-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9ad-117">-DefaultProfile</span></span>
<span data-ttu-id="7f9ad-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f9ad-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7f9ad-119">-Force</span></span>
<span data-ttu-id="7f9ad-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="7f9ad-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7f9ad-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7f9ad-121">-IpAddressVersion</span></span>
<span data-ttu-id="7f9ad-122">A versão do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-122">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="7f9ad-123">-IpTag</span></span>
<span data-ttu-id="7f9ad-124">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-125">-Local</span><span class="sxs-lookup"><span data-stu-id="7f9ad-125">-Location</span></span>
<span data-ttu-id="7f9ad-126">O local do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="7f9ad-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f9ad-127">-Name</span></span>
<span data-ttu-id="7f9ad-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="7f9ad-129">-PrefixLength</span></span>
<span data-ttu-id="7f9ad-130">O comprimento PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f9ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="7f9ad-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-132">The resource group name.</span></span>

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

### <span data-ttu-id="7f9ad-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="7f9ad-133">-Sku</span></span>
<span data-ttu-id="7f9ad-134">O nome SKU do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="7f9ad-135">-Tag</span></span>
<span data-ttu-id="7f9ad-136">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7f9ad-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="7f9ad-137">-Tier</span></span>
<span data-ttu-id="7f9ad-138">A camada de SKU de prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9ad-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="7f9ad-139">-Zone</span></span>
<span data-ttu-id="7f9ad-140">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7f9ad-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f9ad-141">-Confirm</span></span>
<span data-ttu-id="7f9ad-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f9ad-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9ad-143">-WhatIf</span></span>
<span data-ttu-id="7f9ad-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f9ad-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f9ad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9ad-146">CommonParameters</span></span>
<span data-ttu-id="7f9ad-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f9ad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9ad-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f9ad-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9ad-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f9ad-149">INPUTS</span></span>

### <span data-ttu-id="7f9ad-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7f9ad-150">System.String</span></span>

### <span data-ttu-id="7f9ad-151">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="7f9ad-151">System.UInt16</span></span>

### <span data-ttu-id="7f9ad-152">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="7f9ad-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="7f9ad-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="7f9ad-153">System.String[]</span></span>

### <span data-ttu-id="7f9ad-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f9ad-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7f9ad-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f9ad-155">OUTPUTS</span></span>

### <span data-ttu-id="7f9ad-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="7f9ad-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f9ad-157">NOTES</span></span>

## <span data-ttu-id="7f9ad-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f9ad-158">RELATED LINKS</span></span>

[<span data-ttu-id="7f9ad-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="7f9ad-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="7f9ad-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7f9ad-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
