---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426343"
---
# <span data-ttu-id="af26c-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="af26c-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="af26c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af26c-102">SYNOPSIS</span></span>
<span data-ttu-id="af26c-103">Remover conteúdo na porta frontal</span><span class="sxs-lookup"><span data-stu-id="af26c-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af26c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af26c-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af26c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af26c-105">DESCRIPTION</span></span>
<span data-ttu-id="af26c-106">Remove-AzureRmFrontDoorContent limpa o conteúdo em cache na porta frontal</span><span class="sxs-lookup"><span data-stu-id="af26c-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="af26c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af26c-107">EXAMPLES</span></span>

### <span data-ttu-id="af26c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af26c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="af26c-109">OS</span><span class="sxs-lookup"><span data-stu-id="af26c-109">PARAMETERS</span></span>

### <span data-ttu-id="af26c-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="af26c-110">-ContentPath</span></span>
<span data-ttu-id="af26c-111">Os caminhos para o conteúdo a ser limpo.</span><span class="sxs-lookup"><span data-stu-id="af26c-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="af26c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af26c-112">-DefaultProfile</span></span>
<span data-ttu-id="af26c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af26c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af26c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="af26c-114">-Name</span></span>
<span data-ttu-id="af26c-115">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="af26c-115">Front Door name.</span></span>

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

### <span data-ttu-id="af26c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af26c-116">-PassThru</span></span>
<span data-ttu-id="af26c-117">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="af26c-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="af26c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af26c-118">-ResourceGroupName</span></span>
<span data-ttu-id="af26c-119">O nome do grupo de recursos da porta frontal</span><span class="sxs-lookup"><span data-stu-id="af26c-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="af26c-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af26c-120">-Confirm</span></span>
<span data-ttu-id="af26c-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af26c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af26c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af26c-122">-WhatIf</span></span>
<span data-ttu-id="af26c-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af26c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af26c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af26c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af26c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af26c-125">CommonParameters</span></span>
<span data-ttu-id="af26c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af26c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af26c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af26c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af26c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af26c-128">INPUTS</span></span>

### <span data-ttu-id="af26c-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af26c-129">None</span></span>

## <span data-ttu-id="af26c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af26c-130">OUTPUTS</span></span>

### <span data-ttu-id="af26c-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af26c-131">System.Boolean</span></span>

## <span data-ttu-id="af26c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af26c-132">NOTES</span></span>

## <span data-ttu-id="af26c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af26c-133">RELATED LINKS</span></span>
