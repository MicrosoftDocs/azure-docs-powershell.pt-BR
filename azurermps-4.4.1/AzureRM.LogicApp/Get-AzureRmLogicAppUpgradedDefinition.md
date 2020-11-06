---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: fda0c69f1df7df0939af3b788354111ddbaf8471
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610766"
---
# <span data-ttu-id="61920-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="61920-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="61920-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61920-102">SYNOPSIS</span></span>
<span data-ttu-id="61920-103">Obtém a definição atualizada para um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="61920-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61920-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61920-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61920-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61920-105">DESCRIPTION</span></span>
<span data-ttu-id="61920-106">O cmdlet **Get-AzureRmLogicAppUpgradedDefinition** Obtém a definição atualizada da versão do esquema e do aplicativo lógico a partir de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61920-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="61920-107">Esse cmdlet retorna um objeto que representa a definição do aplicativo lógico atualizado.</span><span class="sxs-lookup"><span data-stu-id="61920-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="61920-108">Especifique o nome do grupo de recursos, o nome do aplicativo lógico e a versão do esquema de destino.</span><span class="sxs-lookup"><span data-stu-id="61920-108">Specify the resource group name, logic app name, and target schema version.</span></span>

<span data-ttu-id="61920-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="61920-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61920-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="61920-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61920-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="61920-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61920-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="61920-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61920-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61920-113">EXAMPLES</span></span>

### <span data-ttu-id="61920-114">Exemplo 1: obter uma definição de aplicativo lógico atualizado</span><span class="sxs-lookup"><span data-stu-id="61920-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="61920-115">O primeiro comando obtém a definição do aplicativo lógico atualizado para a versão de esquema de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="61920-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="61920-116">O comando armazena a definição na variável $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="61920-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>

<span data-ttu-id="61920-117">O segundo comando exibe o conteúdo de $UpgradedDefinition como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="61920-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="61920-118">OS</span><span class="sxs-lookup"><span data-stu-id="61920-118">PARAMETERS</span></span>

### <span data-ttu-id="61920-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="61920-119">-Name</span></span>
<span data-ttu-id="61920-120">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="61920-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="61920-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61920-121">-ResourceGroupName</span></span>
<span data-ttu-id="61920-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61920-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61920-123">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="61920-123">-TargetSchemaVersion</span></span>
<span data-ttu-id="61920-124">Especifica a versão de esquema de destino da definição.</span><span class="sxs-lookup"><span data-stu-id="61920-124">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="61920-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61920-125">-DefaultProfile</span></span>
<span data-ttu-id="61920-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61920-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61920-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61920-127">CommonParameters</span></span>
<span data-ttu-id="61920-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61920-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61920-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61920-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61920-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61920-130">INPUTS</span></span>

## <span data-ttu-id="61920-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61920-131">OUTPUTS</span></span>

### <span data-ttu-id="61920-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="61920-132">System.Object</span></span>

## <span data-ttu-id="61920-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61920-133">NOTES</span></span>

## <span data-ttu-id="61920-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61920-134">RELATED LINKS</span></span>

[<span data-ttu-id="61920-135">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="61920-135">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)


