---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117710"
---
# <span data-ttu-id="a4fd9-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a4fd9-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="a4fd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fd9-103">Obtém o histórico de execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="a4fd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4fd9-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4fd9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="a4fd9-106">O cmdlet **Get-AzLogicAppRunHistory** Obtém o histórico de execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="a4fd9-107">Esse cmdlet retorna uma coleção de objetos **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="a4fd9-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="a4fd9-108">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="a4fd9-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a4fd9-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a4fd9-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a4fd9-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a4fd9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4fd9-113">EXAMPLES</span></span>

### <span data-ttu-id="a4fd9-114">Exemplo 1: obter o histórico de execução de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a4fd9-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="a4fd9-115">Esse comando obtém o histórico de execução de um aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="a4fd9-116">Exemplo 2: obter uma execução de aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a4fd9-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="a4fd9-117">Esse comando obtém um aplicativo lógico específico executado para o aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="a4fd9-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a4fd9-118">Example 3</span></span>

<span data-ttu-id="a4fd9-119">Esse comando obtém o histórico de execução de um aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="a4fd9-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="a4fd9-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="a4fd9-121">OS</span><span class="sxs-lookup"><span data-stu-id="a4fd9-121">PARAMETERS</span></span>

### <span data-ttu-id="a4fd9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fd9-122">-DefaultProfile</span></span>
<span data-ttu-id="a4fd9-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a4fd9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4fd9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4fd9-124">-Name</span></span>
<span data-ttu-id="a4fd9-125">Especifica o nome do aplicativo lógico para o qual este cmdlet obtém o histórico de execução.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="a4fd9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fd9-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4fd9-127">Especifica o nome de um grupo de recursos que contém o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="a4fd9-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="a4fd9-128">-RunName</span></span>
<span data-ttu-id="a4fd9-129">Especifica o nome de execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="a4fd9-130">Esse cmdlet obtém a execução do fluxo de trabalho que este cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fd9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fd9-131">CommonParameters</span></span>
<span data-ttu-id="a4fd9-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fd9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fd9-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4fd9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fd9-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4fd9-134">INPUTS</span></span>

### <span data-ttu-id="a4fd9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fd9-135">System.String</span></span>

## <span data-ttu-id="a4fd9-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4fd9-136">OUTPUTS</span></span>

### <span data-ttu-id="a4fd9-137">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="a4fd9-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="a4fd9-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4fd9-138">NOTES</span></span>

## <span data-ttu-id="a4fd9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4fd9-139">RELATED LINKS</span></span>

[<span data-ttu-id="a4fd9-140">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="a4fd9-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="a4fd9-141">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a4fd9-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="a4fd9-142">Parar-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a4fd9-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


