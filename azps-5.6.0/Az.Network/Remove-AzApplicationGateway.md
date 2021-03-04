---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: 7095190570e649ab5262de0a8cebfc97d55fbf17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889423"
---
# <span data-ttu-id="ac820-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac820-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="ac820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac820-102">SYNOPSIS</span></span>
<span data-ttu-id="ac820-103">Remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac820-103">Removes an application gateway.</span></span>

## <span data-ttu-id="ac820-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac820-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac820-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ac820-105">DESCRIPTION</span></span>
<span data-ttu-id="ac820-106">O cmdlet **Remove-AzApplicationGateway** remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac820-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="ac820-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac820-107">EXAMPLES</span></span>

### <span data-ttu-id="ac820-108">Exemplo 1: Remover um gateway de aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="ac820-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ac820-109">Este comando remove o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ac820-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ac820-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac820-110">PARAMETERS</span></span>

### <span data-ttu-id="ac820-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac820-111">-DefaultProfile</span></span>
<span data-ttu-id="ac820-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ac820-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac820-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ac820-113">-Force</span></span>
<span data-ttu-id="ac820-114">Indica que o cmdlet força a exclusão do gateway de aplicativo, independentemente de os recursos a ele ser atribuídos.</span><span class="sxs-lookup"><span data-stu-id="ac820-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac820-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ac820-115">-Name</span></span>
<span data-ttu-id="ac820-116">Especifica o nome do gateway de aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ac820-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac820-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac820-117">-PassThru</span></span>
<span data-ttu-id="ac820-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ac820-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac820-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ac820-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac820-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac820-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac820-121">Especifica o nome do nome do grupo de recursos ao que o gateway de aplicativo pertence.</span><span class="sxs-lookup"><span data-stu-id="ac820-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac820-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac820-122">-Confirm</span></span>
<span data-ttu-id="ac820-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac820-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac820-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac820-124">-WhatIf</span></span>
<span data-ttu-id="ac820-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac820-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac820-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac820-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac820-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac820-127">CommonParameters</span></span>
<span data-ttu-id="ac820-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac820-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac820-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac820-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac820-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac820-130">INPUTS</span></span>

### <span data-ttu-id="ac820-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ac820-131">System.String</span></span>

### <span data-ttu-id="ac820-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac820-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac820-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac820-133">OUTPUTS</span></span>

### <span data-ttu-id="ac820-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac820-134">System.Boolean</span></span>

## <span data-ttu-id="ac820-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac820-135">NOTES</span></span>

## <span data-ttu-id="ac820-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac820-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac820-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac820-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


