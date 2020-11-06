---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 7c7dcac142beb809b95c573d89ef0a912fd1d0b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428201"
---
# <span data-ttu-id="836c4-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="836c4-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="836c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="836c4-102">SYNOPSIS</span></span>
<span data-ttu-id="836c4-103">Obtém uma URL de retorno de chamada de gatilho do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="836c4-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="836c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="836c4-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="836c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="836c4-105">DESCRIPTION</span></span>
<span data-ttu-id="836c4-106">O cmdlet **Get-AzureRmLogicAppTriggerCallbackUrl** Obtém uma URL de retorno de chamada de gatilho do aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="836c4-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="836c4-107">Esse cmdlet retorna um objeto **WorkflowTriggerCallbackUrl** que representa a URL de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="836c4-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="836c4-108">Especifique o nome do grupo de recursos, o nome do aplicativo lógico e o nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="836c4-108">Specify the resource group name, logic app name, and trigger name.</span></span>

<span data-ttu-id="836c4-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="836c4-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="836c4-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="836c4-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="836c4-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="836c4-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="836c4-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="836c4-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="836c4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="836c4-113">EXAMPLES</span></span>

### <span data-ttu-id="836c4-114">Exemplo 1: obter uma URL de retorno de chamada de gatilho do aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="836c4-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="836c4-115">Esse comando obtém uma URL de retorno de chamada de gatilho do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="836c4-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="836c4-116">OS</span><span class="sxs-lookup"><span data-stu-id="836c4-116">PARAMETERS</span></span>

### <span data-ttu-id="836c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836c4-117">-DefaultProfile</span></span>
<span data-ttu-id="836c4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="836c4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836c4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="836c4-119">-Name</span></span>
<span data-ttu-id="836c4-120">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="836c4-120">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="836c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="836c4-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="836c4-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="836c4-123">-Triggername</span><span class="sxs-lookup"><span data-stu-id="836c4-123">-TriggerName</span></span>
<span data-ttu-id="836c4-124">Especifica o nome de um gatilho.</span><span class="sxs-lookup"><span data-stu-id="836c4-124">Specifies the name of a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="836c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836c4-125">CommonParameters</span></span>
<span data-ttu-id="836c4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836c4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836c4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836c4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="836c4-128">INPUTS</span></span>

### <span data-ttu-id="836c4-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="836c4-129">None</span></span>
<span data-ttu-id="836c4-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="836c4-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="836c4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="836c4-131">OUTPUTS</span></span>

### <span data-ttu-id="836c4-132">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="836c4-132">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="836c4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="836c4-133">NOTES</span></span>

## <span data-ttu-id="836c4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="836c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="836c4-135">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="836c4-135">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

