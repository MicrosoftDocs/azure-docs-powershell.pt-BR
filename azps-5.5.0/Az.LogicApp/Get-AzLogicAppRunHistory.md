---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 855cab84e4ab9de2cd7afae2a25dbc867a192e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113622"
---
# <span data-ttu-id="e0ade-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e0ade-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="e0ade-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0ade-102">SYNOPSIS</span></span>

<span data-ttu-id="e0ade-103">Obtém o histórico de executar de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e0ade-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="e0ade-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0ade-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0ade-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0ade-105">DESCRIPTION</span></span>

<span data-ttu-id="e0ade-106">O cmdlet **Get-AzAppRunHistory** obtém o histórico de executar de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e0ade-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="e0ade-107">Este cmdlet retorna um conjunto de objetos **WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="e0ade-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="e0ade-108">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0ade-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="e0ade-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="e0ade-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e0ade-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="e0ade-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e0ade-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e0ade-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e0ade-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="e0ade-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e0ade-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0ade-113">EXAMPLES</span></span>

### <span data-ttu-id="e0ade-114">Exemplo 1: Obter o histórico de executar de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="e0ade-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="e0ade-115">Esse comando obtém o histórico de executar de um aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="e0ade-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="e0ade-116">Exemplo 2: Executar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="e0ade-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="e0ade-117">Esse comando obtém um aplicativo lógico específico executado para o aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="e0ade-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="e0ade-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e0ade-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="e0ade-119">Esse comando obtém todo o histórico de executar de um aplicativo lógico chamado LogicApp03 seguindo o NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="e0ade-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="e0ade-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e0ade-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="e0ade-121">Esse comando obtém as duas primeiras páginas do histórico de executar de um aplicativo lógico chamado LogicApp03 seguindo o NextPageLink e limitando o tamanho do resultado a duas páginas.</span><span class="sxs-lookup"><span data-stu-id="e0ade-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="e0ade-122">Cada página contém 30 resultados.</span><span class="sxs-lookup"><span data-stu-id="e0ade-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="e0ade-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0ade-123">PARAMETERS</span></span>

### <span data-ttu-id="e0ade-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ade-124">-DefaultProfile</span></span>

<span data-ttu-id="e0ade-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e0ade-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0ade-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="e0ade-126">-FollowNextPageLink</span></span>

<span data-ttu-id="e0ade-127">Indica que o cmdlet deve seguir os próximos links de página.</span><span class="sxs-lookup"><span data-stu-id="e0ade-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="e0ade-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="e0ade-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="e0ade-129">Especifica quantas vezes seguir os próximos links de página se o FollowNextPageLink for usado.</span><span class="sxs-lookup"><span data-stu-id="e0ade-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="e0ade-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0ade-130">-Name</span></span>

<span data-ttu-id="e0ade-131">Especifica o nome do aplicativo lógico para o qual este cmdlet recebe histórico de executar.</span><span class="sxs-lookup"><span data-stu-id="e0ade-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="e0ade-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ade-132">-ResourceGroupName</span></span>

<span data-ttu-id="e0ade-133">Especifica o nome de um grupo de recursos que contém o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e0ade-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="e0ade-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="e0ade-134">-RunName</span></span>

<span data-ttu-id="e0ade-135">Especifica o nome de executar de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e0ade-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="e0ade-136">Esse cmdlet obtém o fluxo de trabalho que este cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="e0ade-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="e0ade-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ade-137">CommonParameters</span></span>

<span data-ttu-id="e0ade-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ade-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ade-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ade-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ade-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0ade-140">INPUTS</span></span>

### <span data-ttu-id="e0ade-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ade-141">System.String</span></span>

## <span data-ttu-id="e0ade-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0ade-142">OUTPUTS</span></span>

### <span data-ttu-id="e0ade-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="e0ade-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="e0ade-144">Notas</span><span class="sxs-lookup"><span data-stu-id="e0ade-144">NOTES</span></span>

## <span data-ttu-id="e0ade-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0ade-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0ade-146">Get-AzAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e0ade-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="e0ade-147">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="e0ade-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="e0ade-148">Stop-AzAppRun</span><span class="sxs-lookup"><span data-stu-id="e0ade-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
