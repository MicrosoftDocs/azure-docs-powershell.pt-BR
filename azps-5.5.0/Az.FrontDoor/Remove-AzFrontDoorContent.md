---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117647"
---
# <span data-ttu-id="185b8-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="185b8-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="185b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="185b8-102">SYNOPSIS</span></span>
<span data-ttu-id="185b8-103">Remover conteúdo na Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="185b8-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="185b8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="185b8-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="185b8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="185b8-105">DESCRIPTION</span></span>
<span data-ttu-id="185b8-106">Remove-AzFrontDoorContent limpa o conteúdo armazenado em cache em uma Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="185b8-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="185b8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="185b8-107">EXAMPLES</span></span>

### <span data-ttu-id="185b8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="185b8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="185b8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="185b8-109">PARAMETERS</span></span>

### <span data-ttu-id="185b8-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="185b8-110">-ContentPath</span></span>
<span data-ttu-id="185b8-111">Os caminhos para o conteúdo a ser limpo.</span><span class="sxs-lookup"><span data-stu-id="185b8-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="185b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185b8-112">-DefaultProfile</span></span>
<span data-ttu-id="185b8-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="185b8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="185b8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="185b8-114">-Name</span></span>
<span data-ttu-id="185b8-115">Nome da porta da frente.</span><span class="sxs-lookup"><span data-stu-id="185b8-115">Front Door name.</span></span>

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

### <span data-ttu-id="185b8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="185b8-116">-PassThru</span></span>
<span data-ttu-id="185b8-117">Objeto return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="185b8-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="185b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="185b8-119">O nome do grupo de recursos da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="185b8-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="185b8-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="185b8-120">-Confirm</span></span>
<span data-ttu-id="185b8-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="185b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="185b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185b8-122">-WhatIf</span></span>
<span data-ttu-id="185b8-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="185b8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="185b8-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="185b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="185b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185b8-125">CommonParameters</span></span>
<span data-ttu-id="185b8-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="185b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185b8-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="185b8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185b8-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="185b8-128">INPUTS</span></span>

### <span data-ttu-id="185b8-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="185b8-129">None</span></span>

## <span data-ttu-id="185b8-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="185b8-130">OUTPUTS</span></span>

### <span data-ttu-id="185b8-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="185b8-131">System.Boolean</span></span>

## <span data-ttu-id="185b8-132">Notas</span><span class="sxs-lookup"><span data-stu-id="185b8-132">NOTES</span></span>

## <span data-ttu-id="185b8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="185b8-133">RELATED LINKS</span></span>
