---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114667"
---
# <span data-ttu-id="8de66-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8de66-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="8de66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8de66-102">SYNOPSIS</span></span>
<span data-ttu-id="8de66-103">Remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8de66-103">Removes an application gateway.</span></span>

## <span data-ttu-id="8de66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8de66-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de66-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8de66-105">DESCRIPTION</span></span>
<span data-ttu-id="8de66-106">O **cmdlet Remove-AzApplicationGateway** remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8de66-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="8de66-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8de66-107">EXAMPLES</span></span>

### <span data-ttu-id="8de66-108">Exemplo 1: Remover um gateway de aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="8de66-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8de66-109">Esse comando remove o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8de66-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8de66-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8de66-110">PARAMETERS</span></span>

### <span data-ttu-id="8de66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de66-111">-DefaultProfile</span></span>
<span data-ttu-id="8de66-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8de66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8de66-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8de66-113">-Force</span></span>
<span data-ttu-id="8de66-114">Indica que o cmdlet força a exclusão do gateway de aplicativo independentemente de os recursos a ele estar atribuídos.</span><span class="sxs-lookup"><span data-stu-id="8de66-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="8de66-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8de66-115">-Name</span></span>
<span data-ttu-id="8de66-116">Especifica o nome do gateway de aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8de66-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="8de66-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de66-117">-PassThru</span></span>
<span data-ttu-id="8de66-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8de66-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8de66-119">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="8de66-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8de66-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de66-120">-ResourceGroupName</span></span>
<span data-ttu-id="8de66-121">Especifica o nome do nome do grupo de recursos ao que o gateway de aplicativo pertence.</span><span class="sxs-lookup"><span data-stu-id="8de66-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="8de66-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8de66-122">-Confirm</span></span>
<span data-ttu-id="8de66-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8de66-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de66-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de66-124">-WhatIf</span></span>
<span data-ttu-id="8de66-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8de66-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de66-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8de66-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de66-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de66-127">CommonParameters</span></span>
<span data-ttu-id="8de66-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de66-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de66-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de66-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de66-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="8de66-130">INPUTS</span></span>

### <span data-ttu-id="8de66-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8de66-131">System.String</span></span>

### <span data-ttu-id="8de66-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8de66-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8de66-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="8de66-133">OUTPUTS</span></span>

### <span data-ttu-id="8de66-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8de66-134">System.Boolean</span></span>

## <span data-ttu-id="8de66-135">Notas</span><span class="sxs-lookup"><span data-stu-id="8de66-135">NOTES</span></span>

## <span data-ttu-id="8de66-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8de66-136">RELATED LINKS</span></span>

[<span data-ttu-id="8de66-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8de66-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


