---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126094"
---
# <span data-ttu-id="b6ece-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="b6ece-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="b6ece-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6ece-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ece-103">Obtém a definição atualizada para um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="b6ece-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="b6ece-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6ece-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6ece-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6ece-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ece-106">O cmdlet **Get-AzLogicAppUpgradedDefinition** Obtém a definição atualizada da versão do esquema e do aplicativo lógico a partir de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6ece-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="b6ece-107">Esse cmdlet retorna um objeto que representa a definição do aplicativo lógico atualizado.</span><span class="sxs-lookup"><span data-stu-id="b6ece-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="b6ece-108">Especifique o nome do grupo de recursos, o nome do aplicativo lógico e a versão do esquema de destino.</span><span class="sxs-lookup"><span data-stu-id="b6ece-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="b6ece-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="b6ece-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b6ece-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="b6ece-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b6ece-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b6ece-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b6ece-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="b6ece-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b6ece-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6ece-113">EXAMPLES</span></span>

### <span data-ttu-id="b6ece-114">Exemplo 1: obter uma definição de aplicativo lógico atualizado</span><span class="sxs-lookup"><span data-stu-id="b6ece-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="b6ece-115">O primeiro comando obtém a definição do aplicativo lógico atualizado para a versão de esquema de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="b6ece-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="b6ece-116">O comando armazena a definição na variável $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="b6ece-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="b6ece-117">O segundo comando exibe o conteúdo de $UpgradedDefinition como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6ece-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="b6ece-118">OS</span><span class="sxs-lookup"><span data-stu-id="b6ece-118">PARAMETERS</span></span>

### <span data-ttu-id="b6ece-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ece-119">-DefaultProfile</span></span>
<span data-ttu-id="b6ece-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b6ece-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6ece-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6ece-121">-Name</span></span>
<span data-ttu-id="b6ece-122">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="b6ece-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="b6ece-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ece-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6ece-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6ece-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b6ece-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="b6ece-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="b6ece-126">Especifica a versão de esquema de destino da definição.</span><span class="sxs-lookup"><span data-stu-id="b6ece-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="b6ece-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ece-127">CommonParameters</span></span>
<span data-ttu-id="b6ece-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ece-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ece-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ece-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ece-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6ece-130">INPUTS</span></span>

### <span data-ttu-id="b6ece-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b6ece-131">System.String</span></span>

## <span data-ttu-id="b6ece-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6ece-132">OUTPUTS</span></span>

### <span data-ttu-id="b6ece-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="b6ece-133">System.Object</span></span>

## <span data-ttu-id="b6ece-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6ece-134">NOTES</span></span>

## <span data-ttu-id="b6ece-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6ece-135">RELATED LINKS</span></span>

[<span data-ttu-id="b6ece-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b6ece-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


