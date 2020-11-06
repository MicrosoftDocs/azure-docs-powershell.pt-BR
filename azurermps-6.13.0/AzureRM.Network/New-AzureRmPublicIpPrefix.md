---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610555"
---
# <span data-ttu-id="0e15d-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0e15d-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="0e15d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e15d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e15d-103">Cria um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="0e15d-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e15d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e15d-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e15d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e15d-105">DESCRIPTION</span></span>
<span data-ttu-id="0e15d-106">O cmdlet **New-AzureRmPublicIpPrefix** cria um prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="0e15d-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="0e15d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e15d-107">EXAMPLES</span></span>

### <span data-ttu-id="0e15d-108">1: criar um novo prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="0e15d-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="0e15d-109">Esse comando cria um novo recurso de prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="0e15d-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="0e15d-110">OS</span><span class="sxs-lookup"><span data-stu-id="0e15d-110">PARAMETERS</span></span>

### <span data-ttu-id="0e15d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e15d-111">-AsJob</span></span>
<span data-ttu-id="0e15d-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0e15d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e15d-113">-DefaultProfile</span></span>
<span data-ttu-id="0e15d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e15d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0e15d-115">-Force</span></span>
<span data-ttu-id="0e15d-116">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="0e15d-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0e15d-117">-IpAddressVersion</span></span>
<span data-ttu-id="0e15d-118">A versão do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="0e15d-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="0e15d-119">-IpTag</span></span>
<span data-ttu-id="0e15d-120">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="0e15d-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-121">-Local</span><span class="sxs-lookup"><span data-stu-id="0e15d-121">-Location</span></span>
<span data-ttu-id="0e15d-122">O local do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="0e15d-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e15d-123">-Name</span></span>
<span data-ttu-id="0e15d-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0e15d-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="0e15d-125">-PrefixLength</span></span>
<span data-ttu-id="0e15d-126">O comprimento PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="0e15d-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e15d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e15d-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e15d-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="0e15d-129">-Sku</span></span>
<span data-ttu-id="0e15d-130">O nome SKU do prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="0e15d-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="0e15d-131">-Tag</span></span>
<span data-ttu-id="0e15d-132">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e15d-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="0e15d-133">-Zone</span></span>
<span data-ttu-id="0e15d-134">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="0e15d-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e15d-135">-Confirm</span></span>
<span data-ttu-id="0e15d-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e15d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e15d-137">-WhatIf</span></span>
<span data-ttu-id="0e15d-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e15d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e15d-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e15d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e15d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e15d-140">CommonParameters</span></span>
<span data-ttu-id="0e15d-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e15d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0e15d-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e15d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e15d-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e15d-143">INPUTS</span></span>

### <span data-ttu-id="0e15d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0e15d-144">System.String</span></span>
<span data-ttu-id="0e15d-145">System. UInt16 System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e15d-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="0e15d-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e15d-146">OUTPUTS</span></span>

### <span data-ttu-id="0e15d-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0e15d-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="0e15d-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e15d-148">NOTES</span></span>

## <span data-ttu-id="0e15d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e15d-149">RELATED LINKS</span></span>
