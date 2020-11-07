---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774613"
---
# <span data-ttu-id="2cc0a-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="2cc0a-101">New-AzsIpPool</span></span>

## <span data-ttu-id="2cc0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc0a-103">Crie um pool de IP de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="2cc0a-104">Após a criação de um pool de IPs não pode ser excluído ou modificado.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="2cc0a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cc0a-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cc0a-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cc0a-106">DESCRIPTION</span></span>
<span data-ttu-id="2cc0a-107">Crie um pool de IP de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="2cc0a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cc0a-108">EXAMPLES</span></span>

### <span data-ttu-id="2cc0a-109">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="2cc0a-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="2cc0a-110">Crie um novo pool de IP.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-110">Create a new IP pool.</span></span>

## <span data-ttu-id="2cc0a-111">OS</span><span class="sxs-lookup"><span data-stu-id="2cc0a-111">PARAMETERS</span></span>

### <span data-ttu-id="2cc0a-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cc0a-112">-Name</span></span>
<span data-ttu-id="2cc0a-113">Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-113">IP pool name.</span></span>

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

### <span data-ttu-id="2cc0a-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2cc0a-114">-AddressPrefix</span></span>
<span data-ttu-id="2cc0a-115">O prefixo do endereço.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-115">The address prefix.</span></span>

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

### <span data-ttu-id="2cc0a-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cc0a-116">-StartIpAddress</span></span>
<span data-ttu-id="2cc0a-117">O endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-117">The starting IP address.</span></span>

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

### <span data-ttu-id="2cc0a-118">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="2cc0a-118">-EndIpAddress</span></span>
<span data-ttu-id="2cc0a-119">O endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-119">The ending IP address.</span></span>

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

### <span data-ttu-id="2cc0a-120">-Local</span><span class="sxs-lookup"><span data-stu-id="2cc0a-120">-Location</span></span>
<span data-ttu-id="2cc0a-121">A região em que o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="2cc0a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc0a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2cc0a-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2cc0a-124">-Marcas</span><span class="sxs-lookup"><span data-stu-id="2cc0a-124">-Tags</span></span>
<span data-ttu-id="2cc0a-125">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="2cc0a-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cc0a-126">-AsJob</span></span>
<span data-ttu-id="2cc0a-127">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2cc0a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc0a-128">-WhatIf</span></span>
<span data-ttu-id="2cc0a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cc0a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc0a-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2cc0a-131">-Confirm</span></span>
<span data-ttu-id="2cc0a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc0a-133">CommonParameters</span></span>
<span data-ttu-id="2cc0a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc0a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc0a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc0a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cc0a-136">INPUTS</span></span>

## <span data-ttu-id="2cc0a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cc0a-137">OUTPUTS</span></span>

### <span data-ttu-id="2cc0a-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="2cc0a-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="2cc0a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cc0a-139">NOTES</span></span>

## <span data-ttu-id="2cc0a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cc0a-140">RELATED LINKS</span></span>
