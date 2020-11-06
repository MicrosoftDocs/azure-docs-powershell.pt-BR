---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 891f7fcd50281f5dab9b8d4eaf9f1bd842fbc85e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427887"
---
# <span data-ttu-id="82dc2-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="82dc2-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="82dc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="82dc2-103">Obtém um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="82dc2-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82dc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82dc2-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82dc2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="82dc2-106">O cmdlet **Get-AzureRmLogicApp** Obtém um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="82dc2-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="82dc2-107">Esse cmdlet retorna um objeto de **fluxo de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="82dc2-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="82dc2-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="82dc2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="82dc2-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="82dc2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="82dc2-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="82dc2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="82dc2-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="82dc2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="82dc2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82dc2-112">EXAMPLES</span></span>

### <span data-ttu-id="82dc2-113">Exemplo 1: obter um aplicativo lógico de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="82dc2-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="82dc2-114">Esse comando obtém um aplicativo lógico do grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="82dc2-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="82dc2-115">OS</span><span class="sxs-lookup"><span data-stu-id="82dc2-115">PARAMETERS</span></span>

### <span data-ttu-id="82dc2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="82dc2-116">-Name</span></span>
<span data-ttu-id="82dc2-117">Especifica o nome do aplicativo lógico que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="82dc2-117">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="82dc2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82dc2-118">-ResourceGroupName</span></span>
<span data-ttu-id="82dc2-119">Especifica o nome de um grupo de recursos em que esse cmdlet obtém um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="82dc2-119">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="82dc2-120">-Versão</span><span class="sxs-lookup"><span data-stu-id="82dc2-120">-Version</span></span>
<span data-ttu-id="82dc2-121">Especifica a versão de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="82dc2-121">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="82dc2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82dc2-122">-DefaultProfile</span></span>
<span data-ttu-id="82dc2-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82dc2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82dc2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82dc2-124">CommonParameters</span></span>
<span data-ttu-id="82dc2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82dc2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82dc2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82dc2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82dc2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82dc2-127">INPUTS</span></span>

## <span data-ttu-id="82dc2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82dc2-128">OUTPUTS</span></span>

### <span data-ttu-id="82dc2-129">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="82dc2-129">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="82dc2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82dc2-130">NOTES</span></span>

## <span data-ttu-id="82dc2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82dc2-131">RELATED LINKS</span></span>

[<span data-ttu-id="82dc2-132">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="82dc2-132">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="82dc2-133">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="82dc2-133">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="82dc2-134">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="82dc2-134">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="82dc2-135">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="82dc2-135">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


