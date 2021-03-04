---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 98232807cc5f7624242cd44c7d27579ef0f92d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886223"
---
# <span data-ttu-id="c42d6-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c42d6-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="c42d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c42d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c42d6-103">Obtém um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c42d6-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="c42d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c42d6-104">SYNTAX</span></span>

### <span data-ttu-id="c42d6-105">ListWorkflows (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c42d6-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c42d6-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="c42d6-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c42d6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c42d6-107">DESCRIPTION</span></span>
<span data-ttu-id="c42d6-108">O cmdlet **Get-AzLogicApp** obtém um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c42d6-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="c42d6-109">Este cmdlet retorna um **objeto Workflow.**</span><span class="sxs-lookup"><span data-stu-id="c42d6-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="c42d6-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c42d6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c42d6-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="c42d6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c42d6-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c42d6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c42d6-113">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="c42d6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c42d6-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c42d6-114">EXAMPLES</span></span>

### <span data-ttu-id="c42d6-115">Exemplo 1: Obter um aplicativo lógico de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c42d6-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="c42d6-116">Este comando obtém um aplicativo lógico do grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c42d6-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="c42d6-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c42d6-117">PARAMETERS</span></span>

### <span data-ttu-id="c42d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42d6-118">-DefaultProfile</span></span>
<span data-ttu-id="c42d6-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c42d6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c42d6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c42d6-120">-Name</span></span>
<span data-ttu-id="c42d6-121">Especifica o nome do aplicativo lógico que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c42d6-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="c42d6-123">Especifica o nome de um grupo de recursos no qual esse cmdlet obtém um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c42d6-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42d6-124">-Version</span><span class="sxs-lookup"><span data-stu-id="c42d6-124">-Version</span></span>
<span data-ttu-id="c42d6-125">Especifica a versão de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c42d6-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42d6-126">CommonParameters</span></span>
<span data-ttu-id="c42d6-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42d6-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c42d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42d6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c42d6-129">INPUTS</span></span>

### <span data-ttu-id="c42d6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c42d6-130">System.String</span></span>

## <span data-ttu-id="c42d6-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c42d6-131">OUTPUTS</span></span>

### <span data-ttu-id="c42d6-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="c42d6-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="c42d6-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="c42d6-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="c42d6-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="c42d6-134">NOTES</span></span>

## <span data-ttu-id="c42d6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c42d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="c42d6-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c42d6-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="c42d6-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c42d6-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="c42d6-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c42d6-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="c42d6-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c42d6-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


