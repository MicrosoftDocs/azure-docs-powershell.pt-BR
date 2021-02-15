---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115275"
---
# <span data-ttu-id="15a8b-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="15a8b-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="15a8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="15a8b-103">Obtém a definição atualizada para um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="15a8b-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="15a8b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15a8b-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15a8b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="15a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="15a8b-106">O cmdlet **Get-AzAppUpgradedDefinition obtém** a definição atualizada para a versão de esquema e o aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15a8b-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="15a8b-107">Este cmdlet retorna um objeto que representa a definição do aplicativo de lógica atualizada.</span><span class="sxs-lookup"><span data-stu-id="15a8b-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="15a8b-108">Especifique o nome do grupo de recursos, o nome do aplicativo lógico e a versão de esquema de destino.</span><span class="sxs-lookup"><span data-stu-id="15a8b-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="15a8b-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="15a8b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="15a8b-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="15a8b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="15a8b-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="15a8b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="15a8b-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="15a8b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="15a8b-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15a8b-113">EXAMPLES</span></span>

### <span data-ttu-id="15a8b-114">Exemplo 1: Obter uma definição atualizada do aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="15a8b-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="15a8b-115">O primeiro comando obtém a definição do aplicativo lógico atualizado para a versão de esquema de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="15a8b-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="15a8b-116">O comando armazena a definição na variável $UpgradedDefinition dados.</span><span class="sxs-lookup"><span data-stu-id="15a8b-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="15a8b-117">O segundo comando exibe o conteúdo de $UpgradedDefinition como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="15a8b-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="15a8b-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15a8b-118">PARAMETERS</span></span>

### <span data-ttu-id="15a8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a8b-119">-DefaultProfile</span></span>
<span data-ttu-id="15a8b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="15a8b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15a8b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a8b-121">-Name</span></span>
<span data-ttu-id="15a8b-122">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="15a8b-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="15a8b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a8b-123">-ResourceGroupName</span></span>
<span data-ttu-id="15a8b-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15a8b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15a8b-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="15a8b-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="15a8b-126">Especifica a versão de esquema de destino da definição.</span><span class="sxs-lookup"><span data-stu-id="15a8b-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="15a8b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a8b-127">CommonParameters</span></span>
<span data-ttu-id="15a8b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a8b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a8b-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a8b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a8b-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="15a8b-130">INPUTS</span></span>

### <span data-ttu-id="15a8b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="15a8b-131">System.String</span></span>

## <span data-ttu-id="15a8b-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="15a8b-132">OUTPUTS</span></span>

### <span data-ttu-id="15a8b-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="15a8b-133">System.Object</span></span>

## <span data-ttu-id="15a8b-134">Notas</span><span class="sxs-lookup"><span data-stu-id="15a8b-134">NOTES</span></span>

## <span data-ttu-id="15a8b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15a8b-135">RELATED LINKS</span></span>

[<span data-ttu-id="15a8b-136">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="15a8b-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


