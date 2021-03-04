---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: f9feca370a2672b14252691711810f5de241aa78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887116"
---
# <span data-ttu-id="550b2-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="550b2-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="550b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="550b2-102">SYNOPSIS</span></span>
<span data-ttu-id="550b2-103">Remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="550b2-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="550b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="550b2-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="550b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="550b2-105">DESCRIPTION</span></span>
<span data-ttu-id="550b2-106">O cmdlet **Remove-AzLogicApp** remove um aplicativo lógico de um grupo de recursos usando o recurso Aplicativos Lógicos.</span><span class="sxs-lookup"><span data-stu-id="550b2-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="550b2-107">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="550b2-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="550b2-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="550b2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="550b2-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="550b2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="550b2-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="550b2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="550b2-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="550b2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="550b2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="550b2-112">EXAMPLES</span></span>

### <span data-ttu-id="550b2-113">Exemplo 1: Remover um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="550b2-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="550b2-114">Este comando remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="550b2-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="550b2-115">O comando inclui o parâmetro *Force,* que impede que o comando solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="550b2-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="550b2-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="550b2-116">PARAMETERS</span></span>

### <span data-ttu-id="550b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550b2-117">-DefaultProfile</span></span>
<span data-ttu-id="550b2-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="550b2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="550b2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="550b2-119">-Force</span></span>
<span data-ttu-id="550b2-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="550b2-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="550b2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="550b2-121">-Name</span></span>
<span data-ttu-id="550b2-122">Especifica o nome do aplicativo lógico que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="550b2-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="550b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="550b2-124">Especifica o nome do grupo de recursos que contém o aplicativo lógico que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="550b2-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="550b2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="550b2-125">-Confirm</span></span>
<span data-ttu-id="550b2-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="550b2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="550b2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="550b2-127">-WhatIf</span></span>
<span data-ttu-id="550b2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="550b2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="550b2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="550b2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="550b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550b2-130">CommonParameters</span></span>
<span data-ttu-id="550b2-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="550b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550b2-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="550b2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550b2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="550b2-133">INPUTS</span></span>

### <span data-ttu-id="550b2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="550b2-134">System.String</span></span>

## <span data-ttu-id="550b2-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="550b2-135">OUTPUTS</span></span>

### <span data-ttu-id="550b2-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="550b2-136">System.Void</span></span>

## <span data-ttu-id="550b2-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="550b2-137">NOTES</span></span>

## <span data-ttu-id="550b2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="550b2-138">RELATED LINKS</span></span>

[<span data-ttu-id="550b2-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="550b2-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="550b2-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="550b2-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="550b2-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="550b2-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="550b2-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="550b2-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


