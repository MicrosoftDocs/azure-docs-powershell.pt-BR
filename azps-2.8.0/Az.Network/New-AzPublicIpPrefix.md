---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 28c359c6d9ad9ebfa0d19d7fa4f8d5a72e4884dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771597"
---
# <span data-ttu-id="e82df-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e82df-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="e82df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e82df-102">SYNOPSIS</span></span>
<span data-ttu-id="e82df-103">Cria um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="e82df-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="e82df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e82df-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e82df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e82df-105">DESCRIPTION</span></span>
<span data-ttu-id="e82df-106">O cmdlet **New-AzPublicIpPrefix** cria um prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="e82df-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="e82df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e82df-107">EXAMPLES</span></span>

### <span data-ttu-id="e82df-108">1: criar um novo prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="e82df-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="e82df-109">Esse comando cria um novo recurso de prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="e82df-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="e82df-110">OS</span><span class="sxs-lookup"><span data-stu-id="e82df-110">PARAMETERS</span></span>

### <span data-ttu-id="e82df-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e82df-111">-AsJob</span></span>
<span data-ttu-id="e82df-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e82df-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e82df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82df-113">-DefaultProfile</span></span>
<span data-ttu-id="e82df-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e82df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e82df-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e82df-115">-Force</span></span>
<span data-ttu-id="e82df-116">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="e82df-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e82df-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e82df-117">-IpAddressVersion</span></span>
<span data-ttu-id="e82df-118">A versão do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="e82df-118">The public IP address version.</span></span>

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

### <span data-ttu-id="e82df-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e82df-119">-IpTag</span></span>
<span data-ttu-id="e82df-120">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="e82df-120">IpTag List.</span></span>

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

### <span data-ttu-id="e82df-121">-Local</span><span class="sxs-lookup"><span data-stu-id="e82df-121">-Location</span></span>
<span data-ttu-id="e82df-122">O local do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="e82df-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="e82df-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e82df-123">-Name</span></span>
<span data-ttu-id="e82df-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e82df-124">The resource name.</span></span>

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

### <span data-ttu-id="e82df-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="e82df-125">-PrefixLength</span></span>
<span data-ttu-id="e82df-126">O comprimento PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="e82df-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="e82df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82df-127">-ResourceGroupName</span></span>
<span data-ttu-id="e82df-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e82df-128">The resource group name.</span></span>

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

### <span data-ttu-id="e82df-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="e82df-129">-Sku</span></span>
<span data-ttu-id="e82df-130">O nome SKU do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="e82df-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="e82df-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="e82df-131">-Tag</span></span>
<span data-ttu-id="e82df-132">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="e82df-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e82df-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="e82df-133">-Zone</span></span>
<span data-ttu-id="e82df-134">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="e82df-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e82df-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e82df-135">-Confirm</span></span>
<span data-ttu-id="e82df-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e82df-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e82df-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e82df-137">-WhatIf</span></span>
<span data-ttu-id="e82df-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e82df-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e82df-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e82df-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e82df-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82df-140">CommonParameters</span></span>
<span data-ttu-id="e82df-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82df-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82df-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82df-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82df-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e82df-143">INPUTS</span></span>

### <span data-ttu-id="e82df-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e82df-144">System.String</span></span>

### <span data-ttu-id="e82df-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="e82df-145">System.UInt16</span></span>

### <span data-ttu-id="e82df-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="e82df-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="e82df-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="e82df-147">System.String[]</span></span>

### <span data-ttu-id="e82df-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e82df-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e82df-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e82df-149">OUTPUTS</span></span>

### <span data-ttu-id="e82df-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e82df-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e82df-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e82df-151">NOTES</span></span>

## <span data-ttu-id="e82df-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e82df-152">RELATED LINKS</span></span>

[<span data-ttu-id="e82df-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e82df-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="e82df-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e82df-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="e82df-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e82df-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
