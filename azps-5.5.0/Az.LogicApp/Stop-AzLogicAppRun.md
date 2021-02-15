---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115262"
---
# <span data-ttu-id="8602f-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="8602f-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="8602f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8602f-102">SYNOPSIS</span></span>
<span data-ttu-id="8602f-103">Cancela uma executar um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="8602f-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="8602f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8602f-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8602f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8602f-105">DESCRIPTION</span></span>
<span data-ttu-id="8602f-106">O cmdlet **Stop-AzAppRun** cancela uma executar um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="8602f-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="8602f-107">Especifique o aplicativo lógico, o grupo de recursos e execute.</span><span class="sxs-lookup"><span data-stu-id="8602f-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="8602f-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="8602f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8602f-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="8602f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8602f-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8602f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8602f-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="8602f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8602f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8602f-112">EXAMPLES</span></span>

### <span data-ttu-id="8602f-113">Exemplo 1: Cancelar uma executar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="8602f-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="8602f-114">Esse comando cancela uma executar o aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="8602f-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="8602f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8602f-115">PARAMETERS</span></span>

### <span data-ttu-id="8602f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8602f-116">-DefaultProfile</span></span>
<span data-ttu-id="8602f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8602f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8602f-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8602f-118">-Force</span></span>
<span data-ttu-id="8602f-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8602f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8602f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8602f-120">-Name</span></span>
<span data-ttu-id="8602f-121">Especifica o nome de um aplicativo lógico para o qual este cmdlet cancela uma executar.</span><span class="sxs-lookup"><span data-stu-id="8602f-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="8602f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8602f-122">-ResourceGroupName</span></span>
<span data-ttu-id="8602f-123">Especifica o nome de um grupo de recursos no qual este cmdlet cancela uma executar.</span><span class="sxs-lookup"><span data-stu-id="8602f-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="8602f-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="8602f-124">-RunName</span></span>
<span data-ttu-id="8602f-125">Especifica o nome de um aplicativo lógico executado que este cmdlet cancela.</span><span class="sxs-lookup"><span data-stu-id="8602f-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="8602f-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8602f-126">-Confirm</span></span>
<span data-ttu-id="8602f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8602f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8602f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8602f-128">-WhatIf</span></span>
<span data-ttu-id="8602f-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8602f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8602f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8602f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8602f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8602f-131">CommonParameters</span></span>
<span data-ttu-id="8602f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8602f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8602f-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8602f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8602f-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="8602f-134">INPUTS</span></span>

### <span data-ttu-id="8602f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8602f-135">System.String</span></span>

## <span data-ttu-id="8602f-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="8602f-136">OUTPUTS</span></span>

### <span data-ttu-id="8602f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="8602f-137">System.Void</span></span>

## <span data-ttu-id="8602f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="8602f-138">NOTES</span></span>

## <span data-ttu-id="8602f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8602f-139">RELATED LINKS</span></span>

[<span data-ttu-id="8602f-140">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="8602f-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


