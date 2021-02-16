---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113473"
---
# <span data-ttu-id="23bf6-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="23bf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="23bf6-103">Cria um Prefixo IP Público</span><span class="sxs-lookup"><span data-stu-id="23bf6-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="23bf6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23bf6-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23bf6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="23bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="23bf6-106">O **cmdlet New-AzPublicIpPrefix cria** um prefixo IP público.</span><span class="sxs-lookup"><span data-stu-id="23bf6-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="23bf6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="23bf6-108">Exemplo 1: Criar um novo prefixo Ip público</span><span class="sxs-lookup"><span data-stu-id="23bf6-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="23bf6-109">Esse comando cria um novo recurso de prefixo IP público.</span><span class="sxs-lookup"><span data-stu-id="23bf6-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="23bf6-110">Exemplo 2: Criar um novo prefixo Ip público global</span><span class="sxs-lookup"><span data-stu-id="23bf6-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="23bf6-111">Esse comando cria um novo recurso de prefixo IP público global.</span><span class="sxs-lookup"><span data-stu-id="23bf6-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="23bf6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23bf6-112">PARAMETERS</span></span>

### <span data-ttu-id="23bf6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23bf6-113">-AsJob</span></span>
<span data-ttu-id="23bf6-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="23bf6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23bf6-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-115">-CustomIpPrefix</span></span>
<span data-ttu-id="23bf6-116">O CustomIpPrefix ao que esta PublicIpPrefix será associada</span><span class="sxs-lookup"><span data-stu-id="23bf6-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

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

### <span data-ttu-id="23bf6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23bf6-117">-DefaultProfile</span></span>
<span data-ttu-id="23bf6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23bf6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23bf6-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="23bf6-119">-Force</span></span>
<span data-ttu-id="23bf6-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="23bf6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="23bf6-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="23bf6-121">-IpAddressVersion</span></span>
<span data-ttu-id="23bf6-122">A versão de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="23bf6-122">The public IP address version.</span></span>

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

### <span data-ttu-id="23bf6-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="23bf6-123">-IpTag</span></span>
<span data-ttu-id="23bf6-124">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="23bf6-124">IpTag List.</span></span>

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

### <span data-ttu-id="23bf6-125">-Local</span><span class="sxs-lookup"><span data-stu-id="23bf6-125">-Location</span></span>
<span data-ttu-id="23bf6-126">O local de prefixo IP público.</span><span class="sxs-lookup"><span data-stu-id="23bf6-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="23bf6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="23bf6-127">-Name</span></span>
<span data-ttu-id="23bf6-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="23bf6-128">The resource name.</span></span>

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

### <span data-ttu-id="23bf6-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="23bf6-129">-PrefixLength</span></span>
<span data-ttu-id="23bf6-130">O comprimento publicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-130">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="23bf6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23bf6-131">-ResourceGroupName</span></span>
<span data-ttu-id="23bf6-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23bf6-132">The resource group name.</span></span>

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

### <span data-ttu-id="23bf6-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="23bf6-133">-Sku</span></span>
<span data-ttu-id="23bf6-134">O nome SKU do Prefixo IP público.</span><span class="sxs-lookup"><span data-stu-id="23bf6-134">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="23bf6-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="23bf6-135">-Tag</span></span>
<span data-ttu-id="23bf6-136">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="23bf6-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="23bf6-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="23bf6-137">-Tier</span></span>
<span data-ttu-id="23bf6-138">O nível de SKU de prefixo IP público.</span><span class="sxs-lookup"><span data-stu-id="23bf6-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="23bf6-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="23bf6-139">-Zone</span></span>
<span data-ttu-id="23bf6-140">Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.</span><span class="sxs-lookup"><span data-stu-id="23bf6-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="23bf6-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="23bf6-141">-Confirm</span></span>
<span data-ttu-id="23bf6-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23bf6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23bf6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23bf6-143">-WhatIf</span></span>
<span data-ttu-id="23bf6-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="23bf6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23bf6-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23bf6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23bf6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bf6-146">CommonParameters</span></span>
<span data-ttu-id="23bf6-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23bf6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bf6-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23bf6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bf6-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="23bf6-149">INPUTS</span></span>

### <span data-ttu-id="23bf6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="23bf6-150">System.String</span></span>

### <span data-ttu-id="23bf6-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="23bf6-151">System.UInt16</span></span>

### <span data-ttu-id="23bf6-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="23bf6-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="23bf6-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="23bf6-153">System.String[]</span></span>

### <span data-ttu-id="23bf6-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="23bf6-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="23bf6-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="23bf6-155">OUTPUTS</span></span>

### <span data-ttu-id="23bf6-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="23bf6-157">Notas</span><span class="sxs-lookup"><span data-stu-id="23bf6-157">NOTES</span></span>

## <span data-ttu-id="23bf6-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23bf6-158">RELATED LINKS</span></span>

[<span data-ttu-id="23bf6-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="23bf6-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="23bf6-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="23bf6-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
