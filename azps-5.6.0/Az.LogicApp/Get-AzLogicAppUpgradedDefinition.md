---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 1be662b88b487fbf79092c30f8bd7277adc9e3cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892761"
---
# <span data-ttu-id="02164-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="02164-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="02164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02164-102">SYNOPSIS</span></span>
<span data-ttu-id="02164-103">Obtém a definição atualizada para um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="02164-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="02164-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02164-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02164-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02164-105">DESCRIPTION</span></span>
<span data-ttu-id="02164-106">O cmdlet **Get-AzLogicAppUpgradedDefinition** obtém a definição atualizada para a versão do esquema e o aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02164-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="02164-107">Este cmdlet retorna um objeto que representa a definição do aplicativo lógico atualizado.</span><span class="sxs-lookup"><span data-stu-id="02164-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="02164-108">Especifique o nome do grupo de recursos, o nome do aplicativo lógico e a versão do esquema de destino.</span><span class="sxs-lookup"><span data-stu-id="02164-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="02164-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="02164-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="02164-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="02164-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="02164-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="02164-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="02164-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="02164-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="02164-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02164-113">EXAMPLES</span></span>

### <span data-ttu-id="02164-114">Exemplo 1: obter uma definição atualizada de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="02164-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="02164-115">O primeiro comando obtém a definição do aplicativo lógico atualizado para a versão de esquema de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="02164-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="02164-116">O comando armazena a definição na $UpgradedDefinition variável.</span><span class="sxs-lookup"><span data-stu-id="02164-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="02164-117">O segundo comando exibe o conteúdo do $UpgradedDefinition como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="02164-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="02164-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02164-118">PARAMETERS</span></span>

### <span data-ttu-id="02164-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02164-119">-DefaultProfile</span></span>
<span data-ttu-id="02164-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="02164-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02164-121">-Name</span><span class="sxs-lookup"><span data-stu-id="02164-121">-Name</span></span>
<span data-ttu-id="02164-122">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="02164-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="02164-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02164-123">-ResourceGroupName</span></span>
<span data-ttu-id="02164-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02164-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="02164-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="02164-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="02164-126">Especifica a versão de esquema de destino da definição.</span><span class="sxs-lookup"><span data-stu-id="02164-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02164-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02164-127">CommonParameters</span></span>
<span data-ttu-id="02164-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02164-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02164-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02164-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02164-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02164-130">INPUTS</span></span>

### <span data-ttu-id="02164-131">System.String</span><span class="sxs-lookup"><span data-stu-id="02164-131">System.String</span></span>

## <span data-ttu-id="02164-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02164-132">OUTPUTS</span></span>

### <span data-ttu-id="02164-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="02164-133">System.Object</span></span>

## <span data-ttu-id="02164-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="02164-134">NOTES</span></span>

## <span data-ttu-id="02164-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02164-135">RELATED LINKS</span></span>

[<span data-ttu-id="02164-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="02164-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


