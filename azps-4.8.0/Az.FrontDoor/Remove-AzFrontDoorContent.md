---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114521"
---
# <span data-ttu-id="bcaba-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="bcaba-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="bcaba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcaba-102">SYNOPSIS</span></span>
<span data-ttu-id="bcaba-103">Remover conteúdo na porta frontal</span><span class="sxs-lookup"><span data-stu-id="bcaba-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="bcaba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcaba-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcaba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcaba-105">DESCRIPTION</span></span>
<span data-ttu-id="bcaba-106">Remove-AzFrontDoorContent limpa o conteúdo em cache na porta frontal</span><span class="sxs-lookup"><span data-stu-id="bcaba-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="bcaba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcaba-107">EXAMPLES</span></span>

### <span data-ttu-id="bcaba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bcaba-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="bcaba-109">OS</span><span class="sxs-lookup"><span data-stu-id="bcaba-109">PARAMETERS</span></span>

### <span data-ttu-id="bcaba-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="bcaba-110">-ContentPath</span></span>
<span data-ttu-id="bcaba-111">Os caminhos para o conteúdo a ser limpo.</span><span class="sxs-lookup"><span data-stu-id="bcaba-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="bcaba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcaba-112">-DefaultProfile</span></span>
<span data-ttu-id="bcaba-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcaba-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcaba-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcaba-114">-Name</span></span>
<span data-ttu-id="bcaba-115">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="bcaba-115">Front Door name.</span></span>

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

### <span data-ttu-id="bcaba-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcaba-116">-PassThru</span></span>
<span data-ttu-id="bcaba-117">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="bcaba-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="bcaba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcaba-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcaba-119">O nome do grupo de recursos da porta frontal</span><span class="sxs-lookup"><span data-stu-id="bcaba-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="bcaba-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bcaba-120">-Confirm</span></span>
<span data-ttu-id="bcaba-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcaba-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcaba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcaba-122">-WhatIf</span></span>
<span data-ttu-id="bcaba-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcaba-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcaba-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcaba-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcaba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcaba-125">CommonParameters</span></span>
<span data-ttu-id="bcaba-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcaba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcaba-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcaba-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcaba-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcaba-128">INPUTS</span></span>

### <span data-ttu-id="bcaba-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bcaba-129">None</span></span>

## <span data-ttu-id="bcaba-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcaba-130">OUTPUTS</span></span>

### <span data-ttu-id="bcaba-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcaba-131">System.Boolean</span></span>

## <span data-ttu-id="bcaba-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcaba-132">NOTES</span></span>

## <span data-ttu-id="bcaba-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcaba-133">RELATED LINKS</span></span>
