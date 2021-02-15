---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115263"
---
# <span data-ttu-id="f4629-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f4629-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="f4629-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4629-102">SYNOPSIS</span></span>
<span data-ttu-id="f4629-103">Executa um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4629-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="f4629-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4629-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4629-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4629-105">DESCRIPTION</span></span>
<span data-ttu-id="f4629-106">O **cmdlet Start-Az LogicApp** executa um aplicativo lógico usando o recurso Aplicativos Lógicos.</span><span class="sxs-lookup"><span data-stu-id="f4629-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="f4629-107">Especifique um nome, um grupo de recursos e um gatilho.</span><span class="sxs-lookup"><span data-stu-id="f4629-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="f4629-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f4629-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f4629-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="f4629-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f4629-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f4629-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f4629-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="f4629-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f4629-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4629-112">EXAMPLES</span></span>

### <span data-ttu-id="f4629-113">Exemplo 1: Executar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="f4629-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="f4629-114">Esse comando executa o aplicativo lógico no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4629-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f4629-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4629-115">PARAMETERS</span></span>

### <span data-ttu-id="f4629-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4629-116">-DefaultProfile</span></span>
<span data-ttu-id="f4629-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f4629-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4629-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4629-118">-Name</span></span>
<span data-ttu-id="f4629-119">Especifica o nome do aplicativo lógico que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="f4629-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f4629-120">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4629-120">-Parameters</span></span>
<span data-ttu-id="f4629-121">Especifica um objeto de conjunto de parâmetros do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="f4629-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="f4629-122">Especifique uma tabela hash, dicionário \<string\> ou \<string, WorkflowParameter\> dicionário.</span><span class="sxs-lookup"><span data-stu-id="f4629-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4629-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4629-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4629-124">Especifica o nome do grupo de recursos que contém o aplicativo lógico que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="f4629-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f4629-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="f4629-125">-TriggerName</span></span>
<span data-ttu-id="f4629-126">Especifica o nome do gatilho do aplicativo lógico que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="f4629-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f4629-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f4629-127">-Confirm</span></span>
<span data-ttu-id="f4629-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4629-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4629-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4629-129">-WhatIf</span></span>
<span data-ttu-id="f4629-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f4629-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4629-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4629-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4629-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4629-132">CommonParameters</span></span>
<span data-ttu-id="f4629-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4629-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4629-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4629-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4629-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="f4629-135">INPUTS</span></span>

### <span data-ttu-id="f4629-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f4629-136">System.String</span></span>

## <span data-ttu-id="f4629-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="f4629-137">OUTPUTS</span></span>

### <span data-ttu-id="f4629-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="f4629-138">System.Void</span></span>

## <span data-ttu-id="f4629-139">Notas</span><span class="sxs-lookup"><span data-stu-id="f4629-139">NOTES</span></span>

## <span data-ttu-id="f4629-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4629-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4629-141">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="f4629-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="f4629-142">Get-AzHistoryAppRun</span><span class="sxs-lookup"><span data-stu-id="f4629-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="f4629-143">Novo-AzApp</span><span class="sxs-lookup"><span data-stu-id="f4629-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="f4629-144">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="f4629-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="f4629-145">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="f4629-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="f4629-146">Stop-AzAppRun</span><span class="sxs-lookup"><span data-stu-id="f4629-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


