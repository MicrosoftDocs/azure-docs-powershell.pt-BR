---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: f8e6204be07b9094b1fb4f2cb4c5cafa2a609f0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440782"
---
# <span data-ttu-id="a0523-101">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a0523-101">Get-AzureRmLogicAppRunHistory</span></span>

## <span data-ttu-id="a0523-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0523-102">SYNOPSIS</span></span>
<span data-ttu-id="a0523-103">Obtém o histórico de execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0523-103">Gets the run history of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0523-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0523-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0523-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0523-105">DESCRIPTION</span></span>
<span data-ttu-id="a0523-106">O cmdlet **Get-AzureRmLogicAppRunHistory** Obtém o histórico de execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0523-106">The **Get-AzureRmLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="a0523-107">Esse cmdlet retorna uma coleção de objetos **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="a0523-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="a0523-108">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0523-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="a0523-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="a0523-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a0523-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="a0523-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a0523-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a0523-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a0523-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="a0523-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a0523-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0523-113">EXAMPLES</span></span>

### <span data-ttu-id="a0523-114">Exemplo 1: obter o histórico de execução de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a0523-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="a0523-115">Esse comando obtém o histórico de execução de um aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a0523-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="a0523-116">Exemplo 2: obter uma execução de aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a0523-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="a0523-117">Esse comando obtém um aplicativo lógico específico executado para o aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a0523-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="a0523-118">OS</span><span class="sxs-lookup"><span data-stu-id="a0523-118">PARAMETERS</span></span>

### <span data-ttu-id="a0523-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0523-119">-DefaultProfile</span></span>
<span data-ttu-id="a0523-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a0523-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0523-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0523-121">-Name</span></span>
<span data-ttu-id="a0523-122">Especifica o nome do aplicativo lógico para o qual este cmdlet obtém o histórico de execução.</span><span class="sxs-lookup"><span data-stu-id="a0523-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="a0523-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0523-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0523-124">Especifica o nome de um grupo de recursos que contém o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0523-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="a0523-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="a0523-125">-RunName</span></span>
<span data-ttu-id="a0523-126">Especifica o nome de execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0523-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="a0523-127">Esse cmdlet obtém a execução do fluxo de trabalho que este cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="a0523-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="a0523-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0523-128">CommonParameters</span></span>
<span data-ttu-id="a0523-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0523-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0523-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0523-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0523-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0523-131">INPUTS</span></span>

### <span data-ttu-id="a0523-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0523-132">System.String</span></span>

## <span data-ttu-id="a0523-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0523-133">OUTPUTS</span></span>

### <span data-ttu-id="a0523-134">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="a0523-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="a0523-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0523-135">NOTES</span></span>

## <span data-ttu-id="a0523-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0523-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0523-137">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="a0523-137">Get-AzureRmLogicAppRunAction</span></span>](./Get-AzureRmLogicAppRunAction.md)

[<span data-ttu-id="a0523-138">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0523-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

[<span data-ttu-id="a0523-139">Parar-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a0523-139">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


