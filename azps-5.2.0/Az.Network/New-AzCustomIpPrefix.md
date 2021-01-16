---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260615"
---
# <span data-ttu-id="4735e-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4735e-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="4735e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4735e-102">SYNOPSIS</span></span>
<span data-ttu-id="4735e-103">Cria um recurso do CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4735e-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="4735e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4735e-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4735e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4735e-105">DESCRIPTION</span></span>
<span data-ttu-id="4735e-106">O cmdlet **New-AzCustomIpPrefix** cria um recurso CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="4735e-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="4735e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4735e-107">EXAMPLES</span></span>

### <span data-ttu-id="4735e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4735e-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="4735e-109">Esse comando cria um novo recurso CustomIpPrefix com o nome $prefixName no grupo $rgName de recursos com um CIDR de 40.40.40.0/24 na westus</span><span class="sxs-lookup"><span data-stu-id="4735e-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="4735e-110">OS</span><span class="sxs-lookup"><span data-stu-id="4735e-110">PARAMETERS</span></span>

### <span data-ttu-id="4735e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4735e-111">-AsJob</span></span>
<span data-ttu-id="4735e-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4735e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4735e-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="4735e-113">-Cidr</span></span>
<span data-ttu-id="4735e-114">O CIDR CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="4735e-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="4735e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4735e-115">-DefaultProfile</span></span>
<span data-ttu-id="4735e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4735e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4735e-117">-Local</span><span class="sxs-lookup"><span data-stu-id="4735e-117">-Location</span></span>
<span data-ttu-id="4735e-118">O local do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="4735e-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="4735e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4735e-119">-Name</span></span>
<span data-ttu-id="4735e-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4735e-120">The resource name.</span></span>

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

### <span data-ttu-id="4735e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4735e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4735e-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4735e-122">The resource group name.</span></span>

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

### <span data-ttu-id="4735e-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="4735e-123">-Tag</span></span>
<span data-ttu-id="4735e-124">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="4735e-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4735e-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="4735e-125">-Zone</span></span>
<span data-ttu-id="4735e-126">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="4735e-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4735e-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4735e-127">-Confirm</span></span>
<span data-ttu-id="4735e-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4735e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4735e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4735e-129">-WhatIf</span></span>
<span data-ttu-id="4735e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4735e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4735e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4735e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4735e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4735e-132">CommonParameters</span></span>
<span data-ttu-id="4735e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4735e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4735e-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4735e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4735e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4735e-135">INPUTS</span></span>

### <span data-ttu-id="4735e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4735e-136">System.String</span></span>

### <span data-ttu-id="4735e-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="4735e-137">System.String[]</span></span>

### <span data-ttu-id="4735e-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4735e-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4735e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4735e-139">OUTPUTS</span></span>

### <span data-ttu-id="4735e-140">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4735e-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="4735e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4735e-141">NOTES</span></span>

## <span data-ttu-id="4735e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4735e-142">RELATED LINKS</span></span>

[<span data-ttu-id="4735e-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4735e-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="4735e-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4735e-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="4735e-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4735e-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)