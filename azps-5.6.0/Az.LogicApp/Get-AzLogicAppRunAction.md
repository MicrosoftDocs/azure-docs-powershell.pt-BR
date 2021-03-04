---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892773"
---
# <span data-ttu-id="156e7-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="156e7-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="156e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156e7-102">SYNOPSIS</span></span>

<span data-ttu-id="156e7-103">Obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="156e7-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="156e7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="156e7-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="156e7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="156e7-105">DESCRIPTION</span></span>

<span data-ttu-id="156e7-106">O cmdlet **Get-AzLogicAppRunAction** obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="156e7-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="156e7-107">Este cmdlet retorna um **objeto WorkflowRunAction.**</span><span class="sxs-lookup"><span data-stu-id="156e7-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="156e7-108">Especifique o aplicativo lógico, o grupo de recursos e execute.</span><span class="sxs-lookup"><span data-stu-id="156e7-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="156e7-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="156e7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="156e7-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="156e7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="156e7-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="156e7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="156e7-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="156e7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="156e7-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="156e7-113">EXAMPLES</span></span>

### <span data-ttu-id="156e7-114">Exemplo 1: Obter uma ação de um Aplicativo Lógico executado</span><span class="sxs-lookup"><span data-stu-id="156e7-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
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

<span data-ttu-id="156e7-115">Este comando obtém uma ação específica do Aplicativo Lógico do aplicativo lógico chamado LogicApp05 para a executar com o identificador 08585925184423369718380498702CU26.</span><span class="sxs-lookup"><span data-stu-id="156e7-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="156e7-116">Exemplo 2: Executar todas as ações de um Aplicativo Lógico</span><span class="sxs-lookup"><span data-stu-id="156e7-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="156e7-117">Este comando obtém todas as ações do Aplicativo Lógico de uma executar com o identificador 0858592518442369718380498702CU26 de um aplicativo lógico chamado LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="156e7-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="156e7-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="156e7-118">PARAMETERS</span></span>

### <span data-ttu-id="156e7-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="156e7-119">-ActionName</span></span>

<span data-ttu-id="156e7-120">Especifica o nome de uma ação em um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="156e7-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="156e7-121">Este cmdlet obtém a ação especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="156e7-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="156e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156e7-122">-DefaultProfile</span></span>

<span data-ttu-id="156e7-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="156e7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="156e7-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="156e7-124">-FollowNextPageLink</span></span>

<span data-ttu-id="156e7-125">Indica que o cmdlet deve seguir os links da próxima página.</span><span class="sxs-lookup"><span data-stu-id="156e7-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="156e7-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="156e7-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="156e7-127">Especifica quantas vezes seguir os links da próxima página se FollowNextPageLink for usado.</span><span class="sxs-lookup"><span data-stu-id="156e7-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="156e7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="156e7-128">-Name</span></span>

<span data-ttu-id="156e7-129">Especifica o nome de um aplicativo lógico para o qual este cmdlet obtém uma ação.</span><span class="sxs-lookup"><span data-stu-id="156e7-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="156e7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156e7-130">-ResourceGroupName</span></span>

<span data-ttu-id="156e7-131">Especifica o nome de um grupo de recursos no qual este cmdlet obtém uma ação.</span><span class="sxs-lookup"><span data-stu-id="156e7-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="156e7-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="156e7-132">-RunName</span></span>

<span data-ttu-id="156e7-133">Especifica o nome de uma executar um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="156e7-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="156e7-134">Este cmdlet obtém uma ação para a executar que este parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="156e7-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="156e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156e7-135">CommonParameters</span></span>

<span data-ttu-id="156e7-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156e7-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="156e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156e7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="156e7-138">INPUTS</span></span>

### <span data-ttu-id="156e7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="156e7-139">System.String</span></span>

## <span data-ttu-id="156e7-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="156e7-140">OUTPUTS</span></span>

### <span data-ttu-id="156e7-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="156e7-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="156e7-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="156e7-142">NOTES</span></span>

## <span data-ttu-id="156e7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="156e7-143">RELATED LINKS</span></span>

[<span data-ttu-id="156e7-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="156e7-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="156e7-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="156e7-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
