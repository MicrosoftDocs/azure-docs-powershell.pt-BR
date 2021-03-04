---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: bcbfaefcc94415acdd1100025e1eefc2977f107a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885742"
---
# <span data-ttu-id="29eda-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="29eda-101">Remove-AzImage</span></span>

## <span data-ttu-id="29eda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29eda-102">SYNOPSIS</span></span>
<span data-ttu-id="29eda-103">Remove uma imagem.</span><span class="sxs-lookup"><span data-stu-id="29eda-103">Removes an image.</span></span>

## <span data-ttu-id="29eda-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29eda-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29eda-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29eda-105">DESCRIPTION</span></span>
<span data-ttu-id="29eda-106">O cmdlet **Remove-AzImage** remove uma imagem..</span><span class="sxs-lookup"><span data-stu-id="29eda-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="29eda-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29eda-107">EXAMPLES</span></span>

### <span data-ttu-id="29eda-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29eda-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="29eda-109">Este comando remove a imagem chamada 'Image01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="29eda-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="29eda-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29eda-110">PARAMETERS</span></span>

### <span data-ttu-id="29eda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29eda-111">-AsJob</span></span>
<span data-ttu-id="29eda-112">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="29eda-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="29eda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29eda-113">-DefaultProfile</span></span>
<span data-ttu-id="29eda-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="29eda-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29eda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="29eda-115">-Force</span></span>
<span data-ttu-id="29eda-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="29eda-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29eda-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="29eda-117">-ImageName</span></span>
<span data-ttu-id="29eda-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="29eda-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29eda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29eda-119">-ResourceGroupName</span></span>
<span data-ttu-id="29eda-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29eda-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29eda-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29eda-121">-Confirm</span></span>
<span data-ttu-id="29eda-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29eda-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29eda-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29eda-123">-WhatIf</span></span>
<span data-ttu-id="29eda-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29eda-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29eda-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29eda-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29eda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29eda-126">CommonParameters</span></span>
<span data-ttu-id="29eda-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29eda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29eda-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29eda-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29eda-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29eda-129">INPUTS</span></span>

### <span data-ttu-id="29eda-130">System.String</span><span class="sxs-lookup"><span data-stu-id="29eda-130">System.String</span></span>

## <span data-ttu-id="29eda-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29eda-131">OUTPUTS</span></span>

### <span data-ttu-id="29eda-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="29eda-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="29eda-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="29eda-133">NOTES</span></span>

## <span data-ttu-id="29eda-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29eda-134">RELATED LINKS</span></span>
