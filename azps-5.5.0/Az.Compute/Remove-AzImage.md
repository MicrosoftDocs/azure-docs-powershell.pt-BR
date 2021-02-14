---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116523"
---
# <span data-ttu-id="b4e42-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="b4e42-101">Remove-AzImage</span></span>

## <span data-ttu-id="b4e42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4e42-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e42-103">Remove uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b4e42-103">Removes an image.</span></span>

## <span data-ttu-id="b4e42-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4e42-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e42-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4e42-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e42-106">O cmdlet **Remove-AzImage** remove uma imagem..</span><span class="sxs-lookup"><span data-stu-id="b4e42-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="b4e42-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4e42-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e42-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4e42-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="b4e42-109">Esse comando remove a imagem chamada 'Imagem01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="b4e42-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b4e42-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4e42-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e42-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4e42-111">-AsJob</span></span>
<span data-ttu-id="b4e42-112">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="b4e42-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b4e42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e42-113">-DefaultProfile</span></span>
<span data-ttu-id="b4e42-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b4e42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4e42-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b4e42-115">-Force</span></span>
<span data-ttu-id="b4e42-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b4e42-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4e42-117">-NomedaImagem</span><span class="sxs-lookup"><span data-stu-id="b4e42-117">-ImageName</span></span>
<span data-ttu-id="b4e42-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b4e42-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b4e42-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e42-119">-ResourceGroupName</span></span>
<span data-ttu-id="b4e42-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4e42-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4e42-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4e42-121">-Confirm</span></span>
<span data-ttu-id="b4e42-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4e42-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e42-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e42-123">-WhatIf</span></span>
<span data-ttu-id="b4e42-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4e42-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e42-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4e42-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e42-126">CommonParameters</span></span>
<span data-ttu-id="b4e42-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e42-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4e42-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e42-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4e42-129">INPUTS</span></span>

### <span data-ttu-id="b4e42-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b4e42-130">System.String</span></span>

## <span data-ttu-id="b4e42-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4e42-131">OUTPUTS</span></span>

### <span data-ttu-id="b4e42-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b4e42-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b4e42-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b4e42-133">NOTES</span></span>

## <span data-ttu-id="b4e42-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4e42-134">RELATED LINKS</span></span>
