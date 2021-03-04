---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: 608c80322e46f3c6871bac0350fcc8ae5a5113bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901481"
---
# <span data-ttu-id="275ee-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="275ee-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="275ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275ee-102">SYNOPSIS</span></span>
<span data-ttu-id="275ee-103">Remover conteúdo na Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="275ee-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="275ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="275ee-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275ee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="275ee-105">DESCRIPTION</span></span>
<span data-ttu-id="275ee-106">Remove-AzFrontDoorContent limpa o conteúdo armazenado em cache em uma porta da frente</span><span class="sxs-lookup"><span data-stu-id="275ee-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="275ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="275ee-107">EXAMPLES</span></span>

### <span data-ttu-id="275ee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="275ee-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="275ee-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="275ee-109">PARAMETERS</span></span>

### <span data-ttu-id="275ee-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="275ee-110">-ContentPath</span></span>
<span data-ttu-id="275ee-111">Os caminhos para o conteúdo a ser limpo.</span><span class="sxs-lookup"><span data-stu-id="275ee-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275ee-112">-DefaultProfile</span></span>
<span data-ttu-id="275ee-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="275ee-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275ee-114">-Name</span><span class="sxs-lookup"><span data-stu-id="275ee-114">-Name</span></span>
<span data-ttu-id="275ee-115">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="275ee-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ee-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="275ee-116">-PassThru</span></span>
<span data-ttu-id="275ee-117">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="275ee-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="275ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="275ee-119">O nome do grupo de recursos da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="275ee-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ee-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="275ee-120">-Confirm</span></span>
<span data-ttu-id="275ee-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275ee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275ee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275ee-122">-WhatIf</span></span>
<span data-ttu-id="275ee-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="275ee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275ee-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="275ee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275ee-125">CommonParameters</span></span>
<span data-ttu-id="275ee-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275ee-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="275ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275ee-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="275ee-128">INPUTS</span></span>

### <span data-ttu-id="275ee-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="275ee-129">None</span></span>

## <span data-ttu-id="275ee-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="275ee-130">OUTPUTS</span></span>

### <span data-ttu-id="275ee-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="275ee-131">System.Boolean</span></span>

## <span data-ttu-id="275ee-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="275ee-132">NOTES</span></span>

## <span data-ttu-id="275ee-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="275ee-133">RELATED LINKS</span></span>
