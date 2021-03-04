---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 01bba193f763eff784bdd5f3f67118d84c6235a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892770"
---
# <span data-ttu-id="87074-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="87074-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="87074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87074-102">SYNOPSIS</span></span>

<span data-ttu-id="87074-103">Obtém o histórico de executar um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="87074-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="87074-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87074-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87074-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87074-105">DESCRIPTION</span></span>

<span data-ttu-id="87074-106">O cmdlet **Get-AzLogicAppRunHistory** obtém o histórico de executar de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="87074-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="87074-107">Este cmdlet retorna uma coleção de **objetos WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="87074-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="87074-108">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87074-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="87074-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="87074-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="87074-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="87074-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="87074-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87074-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="87074-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="87074-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="87074-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87074-113">EXAMPLES</span></span>

### <span data-ttu-id="87074-114">Exemplo 1: Obter o histórico de executar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="87074-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="87074-115">Este comando obtém o histórico de executar um aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="87074-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="87074-116">Exemplo 2: Executar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="87074-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="87074-117">Esse comando obtém um aplicativo lógico específico executado para o aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="87074-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="87074-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="87074-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="87074-119">Este comando obtém todo o histórico de executar um aplicativo lógico chamado LogicApp03 seguindo o NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="87074-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="87074-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="87074-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="87074-121">Este comando obtém as duas primeiras páginas do histórico de executar um aplicativo lógico chamado LogicApp03 seguindo o NextPageLink e limitando o tamanho do resultado a duas páginas.</span><span class="sxs-lookup"><span data-stu-id="87074-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="87074-122">Cada página contém trinta resultados.</span><span class="sxs-lookup"><span data-stu-id="87074-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="87074-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87074-123">PARAMETERS</span></span>

### <span data-ttu-id="87074-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87074-124">-DefaultProfile</span></span>

<span data-ttu-id="87074-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="87074-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87074-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="87074-126">-FollowNextPageLink</span></span>

<span data-ttu-id="87074-127">Indica que o cmdlet deve seguir os links da próxima página.</span><span class="sxs-lookup"><span data-stu-id="87074-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87074-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="87074-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="87074-129">Especifica quantas vezes seguir os links da próxima página se FollowNextPageLink for usado.</span><span class="sxs-lookup"><span data-stu-id="87074-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87074-130">-Name</span><span class="sxs-lookup"><span data-stu-id="87074-130">-Name</span></span>

<span data-ttu-id="87074-131">Especifica o nome do aplicativo lógico para o qual esse cmdlet obtém histórico de executar.</span><span class="sxs-lookup"><span data-stu-id="87074-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="87074-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87074-132">-ResourceGroupName</span></span>

<span data-ttu-id="87074-133">Especifica o nome de um grupo de recursos que contém o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="87074-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="87074-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="87074-134">-RunName</span></span>

<span data-ttu-id="87074-135">Especifica o nome de executar de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="87074-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="87074-136">Este cmdlet obtém o fluxo de trabalho executado que este cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="87074-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="87074-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87074-137">CommonParameters</span></span>

<span data-ttu-id="87074-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87074-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87074-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87074-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87074-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87074-140">INPUTS</span></span>

### <span data-ttu-id="87074-141">System.String</span><span class="sxs-lookup"><span data-stu-id="87074-141">System.String</span></span>

## <span data-ttu-id="87074-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87074-142">OUTPUTS</span></span>

### <span data-ttu-id="87074-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="87074-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="87074-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="87074-144">NOTES</span></span>

## <span data-ttu-id="87074-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87074-145">RELATED LINKS</span></span>

[<span data-ttu-id="87074-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="87074-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="87074-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="87074-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="87074-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="87074-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
