---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786151"
---
# <span data-ttu-id="36ac7-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="36ac7-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="36ac7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="36ac7-103">Remove um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="36ac7-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36ac7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36ac7-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ac7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="36ac7-106">O cmdlet **Remove-AzureRmAvailabilitySet** remove um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="36ac7-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="36ac7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="36ac7-108">Exemplo 1: remover um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="36ac7-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="36ac7-109">Esse comando Remove um conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="36ac7-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="36ac7-110">OS</span><span class="sxs-lookup"><span data-stu-id="36ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="36ac7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36ac7-111">-AsJob</span></span>
<span data-ttu-id="36ac7-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="36ac7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36ac7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ac7-113">-DefaultProfile</span></span>
<span data-ttu-id="36ac7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36ac7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ac7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="36ac7-115">-Force</span></span>
<span data-ttu-id="36ac7-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="36ac7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36ac7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="36ac7-117">-Name</span></span>
<span data-ttu-id="36ac7-118">O nome do conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="36ac7-118">The availability set name.</span></span>

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

### <span data-ttu-id="36ac7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ac7-119">-ResourceGroupName</span></span>
<span data-ttu-id="36ac7-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36ac7-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="36ac7-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36ac7-121">-Confirm</span></span>
<span data-ttu-id="36ac7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ac7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ac7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ac7-123">-WhatIf</span></span>
<span data-ttu-id="36ac7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36ac7-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="36ac7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36ac7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ac7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ac7-126">CommonParameters</span></span>
<span data-ttu-id="36ac7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ac7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ac7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ac7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ac7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36ac7-129">INPUTS</span></span>

### <span data-ttu-id="36ac7-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="36ac7-130">None</span></span>
<span data-ttu-id="36ac7-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="36ac7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36ac7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36ac7-132">OUTPUTS</span></span>

### <span data-ttu-id="36ac7-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="36ac7-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="36ac7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36ac7-134">NOTES</span></span>

## <span data-ttu-id="36ac7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36ac7-135">RELATED LINKS</span></span>

[<span data-ttu-id="36ac7-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="36ac7-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="36ac7-137">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="36ac7-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


