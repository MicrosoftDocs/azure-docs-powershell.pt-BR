---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111806"
---
# <span data-ttu-id="277c7-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="277c7-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="277c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="277c7-102">SYNOPSIS</span></span>
<span data-ttu-id="277c7-103">Remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="277c7-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="277c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="277c7-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277c7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="277c7-105">DESCRIPTION</span></span>
<span data-ttu-id="277c7-106">O cmdlet **Remove-Az LogicApp** remove um aplicativo lógico de um grupo de recursos usando o recurso Aplicativos Lógicos.</span><span class="sxs-lookup"><span data-stu-id="277c7-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="277c7-107">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="277c7-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="277c7-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="277c7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="277c7-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="277c7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="277c7-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="277c7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="277c7-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="277c7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="277c7-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="277c7-112">EXAMPLES</span></span>

### <span data-ttu-id="277c7-113">Exemplo 1: Remover um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="277c7-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="277c7-114">Esse comando remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="277c7-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="277c7-115">O comando inclui o parâmetro *Forçar,* o que impede que o comando solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="277c7-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="277c7-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="277c7-116">PARAMETERS</span></span>

### <span data-ttu-id="277c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277c7-117">-DefaultProfile</span></span>
<span data-ttu-id="277c7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="277c7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="277c7-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="277c7-119">-Force</span></span>
<span data-ttu-id="277c7-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="277c7-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="277c7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="277c7-121">-Name</span></span>
<span data-ttu-id="277c7-122">Especifica o nome do aplicativo lógico que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="277c7-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="277c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="277c7-124">Especifica o nome do grupo de recursos que contém o aplicativo lógico que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="277c7-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="277c7-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="277c7-125">-Confirm</span></span>
<span data-ttu-id="277c7-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="277c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277c7-127">-WhatIf</span></span>
<span data-ttu-id="277c7-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="277c7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277c7-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="277c7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277c7-130">CommonParameters</span></span>
<span data-ttu-id="277c7-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="277c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277c7-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="277c7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277c7-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="277c7-133">INPUTS</span></span>

### <span data-ttu-id="277c7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="277c7-134">System.String</span></span>

## <span data-ttu-id="277c7-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="277c7-135">OUTPUTS</span></span>

### <span data-ttu-id="277c7-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="277c7-136">System.Void</span></span>

## <span data-ttu-id="277c7-137">Notas</span><span class="sxs-lookup"><span data-stu-id="277c7-137">NOTES</span></span>

## <span data-ttu-id="277c7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="277c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="277c7-139">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="277c7-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="277c7-140">Novo-AzApp</span><span class="sxs-lookup"><span data-stu-id="277c7-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="277c7-141">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="277c7-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="277c7-142">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="277c7-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


