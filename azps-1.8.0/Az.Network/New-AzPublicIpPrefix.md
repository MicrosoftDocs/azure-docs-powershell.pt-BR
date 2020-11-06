---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 6ee4f046281a36f0d0da798f1954a29f8d98d9c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600287"
---
# <span data-ttu-id="cf2d5-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cf2d5-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="cf2d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2d5-103">Cria um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="cf2d5-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="cf2d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf2d5-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf2d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2d5-106">O cmdlet **New-AzPublicIpPrefix** cria um prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="cf2d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf2d5-107">EXAMPLES</span></span>

### <span data-ttu-id="cf2d5-108">1: criar um novo prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="cf2d5-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="cf2d5-109">Esse comando cria um novo recurso de prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="cf2d5-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf2d5-110">PARAMETERS</span></span>

### <span data-ttu-id="cf2d5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf2d5-111">-AsJob</span></span>
<span data-ttu-id="cf2d5-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cf2d5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf2d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2d5-113">-DefaultProfile</span></span>
<span data-ttu-id="cf2d5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf2d5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cf2d5-115">-Force</span></span>
<span data-ttu-id="cf2d5-116">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="cf2d5-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="cf2d5-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cf2d5-117">-IpAddressVersion</span></span>
<span data-ttu-id="cf2d5-118">A versão do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-118">The public IP address version.</span></span>

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

### <span data-ttu-id="cf2d5-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="cf2d5-119">-IpTag</span></span>
<span data-ttu-id="cf2d5-120">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-120">IpTag List.</span></span>

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

### <span data-ttu-id="cf2d5-121">-Local</span><span class="sxs-lookup"><span data-stu-id="cf2d5-121">-Location</span></span>
<span data-ttu-id="cf2d5-122">O local do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="cf2d5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf2d5-123">-Name</span></span>
<span data-ttu-id="cf2d5-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-124">The resource name.</span></span>

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

### <span data-ttu-id="cf2d5-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="cf2d5-125">-PrefixLength</span></span>
<span data-ttu-id="cf2d5-126">O comprimento PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="cf2d5-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="cf2d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf2d5-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-128">The resource group name.</span></span>

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

### <span data-ttu-id="cf2d5-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="cf2d5-129">-Sku</span></span>
<span data-ttu-id="cf2d5-130">O nome SKU do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="cf2d5-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="cf2d5-131">-Tag</span></span>
<span data-ttu-id="cf2d5-132">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cf2d5-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="cf2d5-133">-Zone</span></span>
<span data-ttu-id="cf2d5-134">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="cf2d5-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf2d5-135">-Confirm</span></span>
<span data-ttu-id="cf2d5-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf2d5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2d5-137">-WhatIf</span></span>
<span data-ttu-id="cf2d5-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf2d5-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf2d5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2d5-140">CommonParameters</span></span>
<span data-ttu-id="cf2d5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2d5-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2d5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2d5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf2d5-143">INPUTS</span></span>

### <span data-ttu-id="cf2d5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cf2d5-144">System.String</span></span>

### <span data-ttu-id="cf2d5-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="cf2d5-145">System.UInt16</span></span>

### <span data-ttu-id="cf2d5-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="cf2d5-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="cf2d5-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="cf2d5-147">System.String[]</span></span>

### <span data-ttu-id="cf2d5-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cf2d5-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cf2d5-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf2d5-149">OUTPUTS</span></span>

### <span data-ttu-id="cf2d5-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cf2d5-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="cf2d5-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf2d5-151">NOTES</span></span>

## <span data-ttu-id="cf2d5-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf2d5-152">RELATED LINKS</span></span>

[<span data-ttu-id="cf2d5-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cf2d5-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="cf2d5-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cf2d5-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="cf2d5-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cf2d5-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
