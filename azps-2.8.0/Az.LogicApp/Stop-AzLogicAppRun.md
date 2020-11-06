---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: eedfc6f0ab4bc150c2f1516a937fc47320b712be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595994"
---
# <span data-ttu-id="89d62-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="89d62-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="89d62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89d62-102">SYNOPSIS</span></span>
<span data-ttu-id="89d62-103">Cancela uma execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="89d62-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="89d62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89d62-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89d62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89d62-105">DESCRIPTION</span></span>
<span data-ttu-id="89d62-106">O cmdlet **Stop-AzLogicAppRun** cancela uma execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="89d62-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="89d62-107">Especifique o aplicativo lógico, o grupo de recursos e execute.</span><span class="sxs-lookup"><span data-stu-id="89d62-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="89d62-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="89d62-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="89d62-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="89d62-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="89d62-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="89d62-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="89d62-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="89d62-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="89d62-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89d62-112">EXAMPLES</span></span>

### <span data-ttu-id="89d62-113">Exemplo 1: cancelar uma execução de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="89d62-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="89d62-114">Esse comando cancela uma execução do aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="89d62-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="89d62-115">OS</span><span class="sxs-lookup"><span data-stu-id="89d62-115">PARAMETERS</span></span>

### <span data-ttu-id="89d62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d62-116">-DefaultProfile</span></span>
<span data-ttu-id="89d62-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="89d62-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89d62-118">-Force</span><span class="sxs-lookup"><span data-stu-id="89d62-118">-Force</span></span>
<span data-ttu-id="89d62-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="89d62-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89d62-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="89d62-120">-Name</span></span>
<span data-ttu-id="89d62-121">Especifica o nome de um aplicativo lógico para o qual esse cmdlet cancela uma execução.</span><span class="sxs-lookup"><span data-stu-id="89d62-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="89d62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d62-122">-ResourceGroupName</span></span>
<span data-ttu-id="89d62-123">Especifica o nome de um grupo de recursos em que esse cmdlet cancela uma execução.</span><span class="sxs-lookup"><span data-stu-id="89d62-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="89d62-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="89d62-124">-RunName</span></span>
<span data-ttu-id="89d62-125">Especifica o nome de um aplicativo lógico executado que esse cmdlet cancela.</span><span class="sxs-lookup"><span data-stu-id="89d62-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="89d62-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89d62-126">-Confirm</span></span>
<span data-ttu-id="89d62-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89d62-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d62-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d62-128">-WhatIf</span></span>
<span data-ttu-id="89d62-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89d62-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d62-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89d62-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d62-131">CommonParameters</span></span>
<span data-ttu-id="89d62-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d62-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d62-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d62-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89d62-134">INPUTS</span></span>

### <span data-ttu-id="89d62-135">System. String</span><span class="sxs-lookup"><span data-stu-id="89d62-135">System.String</span></span>

## <span data-ttu-id="89d62-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89d62-136">OUTPUTS</span></span>

### <span data-ttu-id="89d62-137">System. void</span><span class="sxs-lookup"><span data-stu-id="89d62-137">System.Void</span></span>

## <span data-ttu-id="89d62-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89d62-138">NOTES</span></span>

## <span data-ttu-id="89d62-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89d62-139">RELATED LINKS</span></span>

[<span data-ttu-id="89d62-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="89d62-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


