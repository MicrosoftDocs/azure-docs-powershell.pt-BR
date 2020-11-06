---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 9c27fd1e46d17722f843a09babab31338e88e2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610312"
---
# <span data-ttu-id="c5297-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c5297-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="c5297-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5297-102">SYNOPSIS</span></span>
<span data-ttu-id="c5297-103">Obtém o histórico de gatilhos em um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5297-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5297-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5297-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5297-105">DESCRIPTION</span></span>
<span data-ttu-id="c5297-106">O cmdlet **Get-AzureRmLogicAppTriggerHistory** Obtém o histórico de gatilhos em um aplicativo lógico no recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="c5297-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="c5297-107">Esse cmdlet retorna um objeto **WorkflowTriggerHistory** .</span><span class="sxs-lookup"><span data-stu-id="c5297-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="c5297-108">Especifique o aplicativo lógico, o grupo de recursos e o gatilho.</span><span class="sxs-lookup"><span data-stu-id="c5297-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="c5297-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c5297-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c5297-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="c5297-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c5297-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c5297-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c5297-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="c5297-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c5297-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5297-113">EXAMPLES</span></span>

### <span data-ttu-id="c5297-114">Exemplo 1: obter um histórico de gatilho de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="c5297-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="c5297-115">Esse comando obtém um histórico de gatilho do aplicativo lógico específico para um gatilho no aplicativo lógico chamado LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="c5297-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="c5297-116">Exemplo 2: obter históricos de gatilho de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="c5297-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="c5297-117">Esse comando obtém os históricos de gatilho do fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="c5297-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="c5297-118">OS</span><span class="sxs-lookup"><span data-stu-id="c5297-118">PARAMETERS</span></span>

### <span data-ttu-id="c5297-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5297-119">-DefaultProfile</span></span>
<span data-ttu-id="c5297-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c5297-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5297-121">-Historyname</span><span class="sxs-lookup"><span data-stu-id="c5297-121">-HistoryName</span></span>
<span data-ttu-id="c5297-122">Especifica o nome do histórico que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c5297-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c5297-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5297-123">-Name</span></span>
<span data-ttu-id="c5297-124">Especifica o nome do aplicativo lógico para o qual este cmdlet tem o histórico de gatilhos.</span><span class="sxs-lookup"><span data-stu-id="c5297-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="c5297-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5297-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5297-126">Especifica o nome do grupo de recursos no qual esse cmdlet obtém o histórico.</span><span class="sxs-lookup"><span data-stu-id="c5297-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="c5297-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="c5297-127">-TriggerName</span></span>
<span data-ttu-id="c5297-128">Especifica o nome do gatilho para o qual esse cmdlet obtém o histórico.</span><span class="sxs-lookup"><span data-stu-id="c5297-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="c5297-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5297-129">CommonParameters</span></span>
<span data-ttu-id="c5297-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5297-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5297-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5297-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5297-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5297-132">INPUTS</span></span>

### <span data-ttu-id="c5297-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c5297-133">System.String</span></span>

## <span data-ttu-id="c5297-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5297-134">OUTPUTS</span></span>

### <span data-ttu-id="c5297-135">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c5297-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="c5297-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5297-136">NOTES</span></span>

## <span data-ttu-id="c5297-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5297-137">RELATED LINKS</span></span>

[<span data-ttu-id="c5297-138">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c5297-138">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="c5297-139">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="c5297-139">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="c5297-140">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c5297-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


