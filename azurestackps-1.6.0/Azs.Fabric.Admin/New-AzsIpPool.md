---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425737"
---
# <span data-ttu-id="cb2b6-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="cb2b6-101">New-AzsIpPool</span></span>

## <span data-ttu-id="cb2b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2b6-103">Crie um pool de IP de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="cb2b6-104">Após a criação de um pool de IPs não pode ser excluído ou modificado.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="cb2b6-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb2b6-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb2b6-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb2b6-106">DESCRIPTION</span></span>
<span data-ttu-id="cb2b6-107">Crie um pool de IP de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="cb2b6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb2b6-108">EXAMPLES</span></span>

### <span data-ttu-id="cb2b6-109">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb2b6-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="cb2b6-110">Crie um novo pool de IP.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-110">Create a new IP pool.</span></span>

## <span data-ttu-id="cb2b6-111">OS</span><span class="sxs-lookup"><span data-stu-id="cb2b6-111">PARAMETERS</span></span>

### <span data-ttu-id="cb2b6-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cb2b6-112">-AddressPrefix</span></span>
<span data-ttu-id="cb2b6-113">O prefixo do endereço.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb2b6-114">-AsJob</span></span>
<span data-ttu-id="cb2b6-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-116">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="cb2b6-116">-EndIpAddress</span></span>
<span data-ttu-id="cb2b6-117">O endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-118">-Local</span><span class="sxs-lookup"><span data-stu-id="cb2b6-118">-Location</span></span>
<span data-ttu-id="cb2b6-119">A região em que o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb2b6-120">-Name</span></span>
<span data-ttu-id="cb2b6-121">Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb2b6-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="cb2b6-124">-StartIpAddress</span></span>
<span data-ttu-id="cb2b6-125">O endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="cb2b6-126">-Tags</span></span>
<span data-ttu-id="cb2b6-127">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2b6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb2b6-128">-Confirm</span></span>
<span data-ttu-id="cb2b6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2b6-130">-WhatIf</span></span>
<span data-ttu-id="cb2b6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb2b6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2b6-133">CommonParameters</span></span>
<span data-ttu-id="cb2b6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2b6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2b6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2b6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb2b6-136">INPUTS</span></span>

## <span data-ttu-id="cb2b6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb2b6-137">OUTPUTS</span></span>

### <span data-ttu-id="cb2b6-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="cb2b6-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="cb2b6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb2b6-139">NOTES</span></span>

## <span data-ttu-id="cb2b6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb2b6-140">RELATED LINKS</span></span>

