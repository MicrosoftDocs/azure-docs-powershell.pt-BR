---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 7c0d34ad56021e2fb4f74aef1bed41ca38c918c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892762"
---
# <span data-ttu-id="a597a-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="a597a-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="a597a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a597a-102">SYNOPSIS</span></span>

<span data-ttu-id="a597a-103">Obtém o histórico de gatilhos em um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="a597a-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="a597a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a597a-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a597a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a597a-105">DESCRIPTION</span></span>

<span data-ttu-id="a597a-106">O cmdlet **Get-AzLogicAppTriggerHistory** obtém o histórico de gatilhos em um aplicativo lógico no recurso Aplicativos Lógicos.</span><span class="sxs-lookup"><span data-stu-id="a597a-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="a597a-107">Este cmdlet retorna um **objeto WorkflowTriggerHistory.**</span><span class="sxs-lookup"><span data-stu-id="a597a-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="a597a-108">Especifique o aplicativo lógico, o grupo de recursos e o gatilho.</span><span class="sxs-lookup"><span data-stu-id="a597a-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="a597a-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="a597a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a597a-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="a597a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a597a-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a597a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a597a-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="a597a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a597a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a597a-113">EXAMPLES</span></span>

### <span data-ttu-id="a597a-114">Exemplo 1: obter um histórico de gatilho de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a597a-114">Example 1: Get a trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="a597a-115">Este comando obtém um histórico de disparo de aplicativo lógico específico para um gatilho no aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a597a-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="a597a-116">Exemplo 2: Obter históricos de gatilho de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a597a-116">Example 2: Get trigger histories of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="a597a-117">Este comando obtém os históricos de gatilho de fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="a597a-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="a597a-118">Exemplo 3: obter todo o histórico de gatilho de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="a597a-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="a597a-119">Esse comando obtém todo o histórico de gatilho de fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp08 seguindo o NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="a597a-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="a597a-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a597a-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="a597a-121">Este comando obtém as duas primeiras páginas do histórico de gatilhos de fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp09 seguindo o NextPageLink e limitando o tamanho do resultado a duas páginas.</span><span class="sxs-lookup"><span data-stu-id="a597a-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="a597a-122">Cada página contém trinta resultados.</span><span class="sxs-lookup"><span data-stu-id="a597a-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="a597a-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a597a-123">PARAMETERS</span></span>

### <span data-ttu-id="a597a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a597a-124">-DefaultProfile</span></span>

<span data-ttu-id="a597a-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a597a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a597a-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="a597a-126">-FollowNextPageLink</span></span>

<span data-ttu-id="a597a-127">Indica que o cmdlet deve seguir os links da próxima página.</span><span class="sxs-lookup"><span data-stu-id="a597a-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="a597a-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="a597a-128">-HistoryName</span></span>

<span data-ttu-id="a597a-129">Especifica o nome do histórico que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a597a-129">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a597a-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="a597a-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="a597a-131">Especifica quantas vezes seguir os links da próxima página se FollowNextPageLink for usado.</span><span class="sxs-lookup"><span data-stu-id="a597a-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="a597a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a597a-132">-Name</span></span>

<span data-ttu-id="a597a-133">Especifica o nome do aplicativo lógico para o qual esse cmdlet obtém o histórico do gatilho.</span><span class="sxs-lookup"><span data-stu-id="a597a-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="a597a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a597a-134">-ResourceGroupName</span></span>

<span data-ttu-id="a597a-135">Especifica o nome do grupo de recursos no qual este cmdlet obtém histórico.</span><span class="sxs-lookup"><span data-stu-id="a597a-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="a597a-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a597a-136">-TriggerName</span></span>

<span data-ttu-id="a597a-137">Especifica o nome do gatilho para o qual este cmdlet obtém histórico.</span><span class="sxs-lookup"><span data-stu-id="a597a-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="a597a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a597a-138">CommonParameters</span></span>

<span data-ttu-id="a597a-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a597a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a597a-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a597a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a597a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a597a-141">INPUTS</span></span>

### <span data-ttu-id="a597a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a597a-142">System.String</span></span>

## <span data-ttu-id="a597a-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a597a-143">OUTPUTS</span></span>

### <span data-ttu-id="a597a-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="a597a-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="a597a-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="a597a-145">NOTES</span></span>

## <span data-ttu-id="a597a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a597a-146">RELATED LINKS</span></span>

[<span data-ttu-id="a597a-147">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a597a-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="a597a-148">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="a597a-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="a597a-149">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a597a-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
