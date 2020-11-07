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
ms.locfileid: "93774110"
---
# <span data-ttu-id="c3add-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="c3add-101">New-AzsIpPool</span></span>

## <span data-ttu-id="c3add-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3add-102">SYNOPSIS</span></span>
<span data-ttu-id="c3add-103">Crie um pool de IP de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c3add-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="c3add-104">Após a criação de um pool de IPs não pode ser excluído ou modificado.</span><span class="sxs-lookup"><span data-stu-id="c3add-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="c3add-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3add-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3add-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3add-106">DESCRIPTION</span></span>
<span data-ttu-id="c3add-107">Crie um pool de IP de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c3add-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="c3add-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3add-108">EXAMPLES</span></span>

### <span data-ttu-id="c3add-109">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c3add-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="c3add-110">Crie um novo pool de IP.</span><span class="sxs-lookup"><span data-stu-id="c3add-110">Create a new IP pool.</span></span>

## <span data-ttu-id="c3add-111">OS</span><span class="sxs-lookup"><span data-stu-id="c3add-111">PARAMETERS</span></span>

### <span data-ttu-id="c3add-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c3add-112">-AddressPrefix</span></span>
<span data-ttu-id="c3add-113">O prefixo do endereço.</span><span class="sxs-lookup"><span data-stu-id="c3add-113">The address prefix.</span></span>

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

### <span data-ttu-id="c3add-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3add-114">-AsJob</span></span>
<span data-ttu-id="c3add-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c3add-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c3add-116">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="c3add-116">-EndIpAddress</span></span>
<span data-ttu-id="c3add-117">O endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="c3add-117">The ending IP address.</span></span>

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

### <span data-ttu-id="c3add-118">-Local</span><span class="sxs-lookup"><span data-stu-id="c3add-118">-Location</span></span>
<span data-ttu-id="c3add-119">A região em que o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="c3add-119">The region where the resource is located.</span></span>

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

### <span data-ttu-id="c3add-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3add-120">-Name</span></span>
<span data-ttu-id="c3add-121">Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="c3add-121">IP pool name.</span></span>

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

### <span data-ttu-id="c3add-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3add-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3add-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="c3add-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c3add-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3add-124">-StartIpAddress</span></span>
<span data-ttu-id="c3add-125">O endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="c3add-125">The starting IP address.</span></span>

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

### <span data-ttu-id="c3add-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="c3add-126">-Tags</span></span>
<span data-ttu-id="c3add-127">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="c3add-127">List of key-value pairs.</span></span>

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

### <span data-ttu-id="c3add-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3add-128">-Confirm</span></span>
<span data-ttu-id="c3add-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3add-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3add-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3add-130">-WhatIf</span></span>
<span data-ttu-id="c3add-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3add-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3add-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3add-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3add-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3add-133">CommonParameters</span></span>
<span data-ttu-id="c3add-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3add-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3add-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3add-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3add-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3add-136">INPUTS</span></span>

## <span data-ttu-id="c3add-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3add-137">OUTPUTS</span></span>

### <span data-ttu-id="c3add-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="c3add-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="c3add-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3add-139">NOTES</span></span>

## <span data-ttu-id="c3add-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3add-140">RELATED LINKS</span></span>

