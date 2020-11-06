---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 5d496d4d79c13208c3c48a9d01bfe010ef64c244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601286"
---
# <span data-ttu-id="f6847-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="f6847-101">Remove-AzImage</span></span>

## <span data-ttu-id="f6847-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6847-102">SYNOPSIS</span></span>
<span data-ttu-id="f6847-103">Remove uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f6847-103">Removes an image.</span></span>

## <span data-ttu-id="f6847-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6847-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6847-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6847-105">DESCRIPTION</span></span>
<span data-ttu-id="f6847-106">O cmdlet **Remove-AzImage** remove uma imagem..</span><span class="sxs-lookup"><span data-stu-id="f6847-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="f6847-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6847-107">EXAMPLES</span></span>

### <span data-ttu-id="f6847-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6847-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="f6847-109">Este comando Remove a imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f6847-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f6847-110">OS</span><span class="sxs-lookup"><span data-stu-id="f6847-110">PARAMETERS</span></span>

### <span data-ttu-id="f6847-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6847-111">-AsJob</span></span>
<span data-ttu-id="f6847-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="f6847-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f6847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6847-113">-DefaultProfile</span></span>
<span data-ttu-id="f6847-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6847-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6847-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f6847-115">-Force</span></span>
<span data-ttu-id="f6847-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6847-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6847-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f6847-117">-ImageName</span></span>
<span data-ttu-id="f6847-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f6847-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f6847-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6847-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6847-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6847-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f6847-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6847-121">-Confirm</span></span>
<span data-ttu-id="f6847-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6847-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6847-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6847-123">-WhatIf</span></span>
<span data-ttu-id="f6847-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6847-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6847-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6847-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6847-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6847-126">CommonParameters</span></span>
<span data-ttu-id="f6847-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6847-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6847-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6847-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6847-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6847-129">INPUTS</span></span>

### <span data-ttu-id="f6847-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f6847-130">System.String</span></span>

## <span data-ttu-id="f6847-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6847-131">OUTPUTS</span></span>

### <span data-ttu-id="f6847-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f6847-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f6847-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6847-133">NOTES</span></span>

## <span data-ttu-id="f6847-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6847-134">RELATED LINKS</span></span>
