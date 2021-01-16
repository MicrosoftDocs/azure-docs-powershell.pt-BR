---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262073"
---
# <span data-ttu-id="e4486-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e4486-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="e4486-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4486-102">SYNOPSIS</span></span>
<span data-ttu-id="e4486-103">Obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="e4486-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="e4486-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4486-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4486-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4486-105">DESCRIPTION</span></span>
<span data-ttu-id="e4486-106">O cmdlet **Get-AzLogicAppRunAction** Obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="e4486-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="e4486-107">Esse cmdlet retorna objetos **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="e4486-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="e4486-108">Especifique o aplicativo lógico, o grupo de recursos e execute.</span><span class="sxs-lookup"><span data-stu-id="e4486-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="e4486-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="e4486-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e4486-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="e4486-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e4486-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4486-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e4486-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="e4486-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e4486-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4486-113">EXAMPLES</span></span>

### <span data-ttu-id="e4486-114">Exemplo 1: obter uma ação de um aplicativo lógico executado</span><span class="sxs-lookup"><span data-stu-id="e4486-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e4486-115">Esse comando obtém uma ação específica do aplicativo lógico do aplicativo lógico chamado LogicApp05 para a execução nomeada LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="e4486-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="e4486-116">Exemplo 2: obter todas as ações de uma execução de aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="e4486-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e4486-117">Esse comando obtém todas as ações da aplicação lógica de uma execução nomeada LogicAppRun56 de um aplicativo lógico chamado LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="e4486-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="e4486-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e4486-118">Example 3</span></span>

<span data-ttu-id="e4486-119">Esse comando obtém todas as ações da aplicação lógica de uma execução nomeada LogicAppRun56 de um aplicativo lógico chamado LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="e4486-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="e4486-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e4486-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="e4486-121">OS</span><span class="sxs-lookup"><span data-stu-id="e4486-121">PARAMETERS</span></span>

### <span data-ttu-id="e4486-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="e4486-122">-ActionName</span></span>
<span data-ttu-id="e4486-123">Especifica o nome de uma ação em um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="e4486-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="e4486-124">Esse cmdlet obtém a ação que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e4486-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4486-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4486-125">-DefaultProfile</span></span>
<span data-ttu-id="e4486-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e4486-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4486-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4486-127">-Name</span></span>
<span data-ttu-id="e4486-128">Especifica o nome de um aplicativo lógico para o qual esse cmdlet recebe uma ação.</span><span class="sxs-lookup"><span data-stu-id="e4486-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e4486-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4486-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4486-130">Especifica o nome de um grupo de recursos em que esse cmdlet recebe uma ação.</span><span class="sxs-lookup"><span data-stu-id="e4486-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e4486-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="e4486-131">-RunName</span></span>
<span data-ttu-id="e4486-132">Especifica o nome de uma execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e4486-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="e4486-133">Esse cmdlet obtém uma ação para a execução que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e4486-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4486-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4486-134">CommonParameters</span></span>
<span data-ttu-id="e4486-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4486-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4486-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4486-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4486-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4486-137">INPUTS</span></span>

### <span data-ttu-id="e4486-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e4486-138">System.String</span></span>

## <span data-ttu-id="e4486-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4486-139">OUTPUTS</span></span>

### <span data-ttu-id="e4486-140">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="e4486-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="e4486-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4486-141">NOTES</span></span>

## <span data-ttu-id="e4486-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4486-142">RELATED LINKS</span></span>

[<span data-ttu-id="e4486-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e4486-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="e4486-144">Parar-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="e4486-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


