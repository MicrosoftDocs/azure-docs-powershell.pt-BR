---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427613"
---
# <span data-ttu-id="93415-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93415-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="93415-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93415-102">SYNOPSIS</span></span>
<span data-ttu-id="93415-103">Remove um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="93415-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93415-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93415-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93415-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93415-105">DESCRIPTION</span></span>
<span data-ttu-id="93415-106">O cmdlet **Remove-AzureRmAvailabilitySet** remove um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="93415-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="93415-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93415-107">EXAMPLES</span></span>

### <span data-ttu-id="93415-108">Exemplo 1: remover um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="93415-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="93415-109">Esse comando Remove um conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="93415-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="93415-110">OS</span><span class="sxs-lookup"><span data-stu-id="93415-110">PARAMETERS</span></span>

### <span data-ttu-id="93415-111">-Force</span><span class="sxs-lookup"><span data-stu-id="93415-111">-Force</span></span>
<span data-ttu-id="93415-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="93415-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93415-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="93415-113">-Name</span></span>
<span data-ttu-id="93415-114">O nome do conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="93415-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93415-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93415-115">-ResourceGroupName</span></span>
<span data-ttu-id="93415-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93415-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93415-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93415-117">-Confirm</span></span>
<span data-ttu-id="93415-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93415-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93415-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93415-119">-WhatIf</span></span>
<span data-ttu-id="93415-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93415-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="93415-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93415-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93415-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93415-122">CommonParameters</span></span>
<span data-ttu-id="93415-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93415-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93415-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93415-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93415-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93415-125">INPUTS</span></span>

### <span data-ttu-id="93415-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="93415-126">None</span></span>
<span data-ttu-id="93415-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="93415-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93415-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93415-128">OUTPUTS</span></span>

## <span data-ttu-id="93415-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93415-129">NOTES</span></span>

## <span data-ttu-id="93415-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93415-130">RELATED LINKS</span></span>

[<span data-ttu-id="93415-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93415-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="93415-132">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93415-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


