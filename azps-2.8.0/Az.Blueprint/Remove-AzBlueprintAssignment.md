---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597633"
---
# <span data-ttu-id="72157-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="72157-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="72157-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72157-102">SYNOPSIS</span></span>
<span data-ttu-id="72157-103">Remover uma atribuição Blueprint de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="72157-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="72157-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72157-104">SYNTAX</span></span>

### <span data-ttu-id="72157-105">DeleteBlueprintAssignmentByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="72157-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72157-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="72157-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72157-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72157-107">DESCRIPTION</span></span>
<span data-ttu-id="72157-108">Remover um plano gráfico atribuído a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="72157-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="72157-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72157-109">EXAMPLES</span></span>

### <span data-ttu-id="72157-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72157-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="72157-111">Remover a atribuição Blueprint especificada pelo nome da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="72157-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="72157-112">O cmdlet pedirá confirmação antes de executar o comando.</span><span class="sxs-lookup"><span data-stu-id="72157-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="72157-113">OS</span><span class="sxs-lookup"><span data-stu-id="72157-113">PARAMETERS</span></span>

### <span data-ttu-id="72157-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72157-114">-DefaultProfile</span></span>
<span data-ttu-id="72157-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72157-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72157-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72157-116">-InputObject</span></span>
<span data-ttu-id="72157-117">Objeto de atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="72157-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72157-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="72157-118">-Name</span></span>
<span data-ttu-id="72157-119">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="72157-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72157-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72157-120">-PassThru</span></span>
<span data-ttu-id="72157-121">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="72157-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="72157-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72157-122">-SubscriptionId</span></span>
<span data-ttu-id="72157-123">ID da assinatura na qual a atribuição Blueprint é implantada.</span><span class="sxs-lookup"><span data-stu-id="72157-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72157-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72157-124">-Confirm</span></span>
<span data-ttu-id="72157-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72157-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72157-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72157-126">-WhatIf</span></span>
<span data-ttu-id="72157-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72157-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72157-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72157-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72157-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72157-129">CommonParameters</span></span>
<span data-ttu-id="72157-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72157-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72157-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72157-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72157-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72157-132">INPUTS</span></span>

### <span data-ttu-id="72157-133">System. String</span><span class="sxs-lookup"><span data-stu-id="72157-133">System.String</span></span>

### <span data-ttu-id="72157-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="72157-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="72157-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72157-135">OUTPUTS</span></span>

### <span data-ttu-id="72157-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="72157-136">System.Object</span></span>
## <span data-ttu-id="72157-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72157-137">NOTES</span></span>

## <span data-ttu-id="72157-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72157-138">RELATED LINKS</span></span>
