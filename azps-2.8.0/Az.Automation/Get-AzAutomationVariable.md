---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a430b8a57abf19e036a75039b6bdddb8a7ea0d16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597819"
---
# <span data-ttu-id="32e61-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="32e61-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="32e61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32e61-102">SYNOPSIS</span></span>
<span data-ttu-id="32e61-103">Obtém uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="32e61-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="32e61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32e61-104">SYNTAX</span></span>

### <span data-ttu-id="32e61-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="32e61-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32e61-106">ByName</span><span class="sxs-lookup"><span data-stu-id="32e61-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32e61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32e61-107">DESCRIPTION</span></span>
<span data-ttu-id="32e61-108">O cmdlet **Get-AzAutomationVariable** Obtém uma ou mais variáveis de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="32e61-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="32e61-109">Para obter uma variável específica, especifique o nome dela.</span><span class="sxs-lookup"><span data-stu-id="32e61-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="32e61-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32e61-110">EXAMPLES</span></span>

### <span data-ttu-id="32e61-111">Exemplo 1: obter uma variável</span><span class="sxs-lookup"><span data-stu-id="32e61-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="32e61-112">O primeiro comando obtém uma variável de automação chamada Variable06 na conta chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="32e61-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="32e61-113">O comando armazena esse objeto na variável $Variable.</span><span class="sxs-lookup"><span data-stu-id="32e61-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="32e61-114">O segundo comando usa a notação de ponto padrão para fazer referência à propriedade **Value** de $Variable.</span><span class="sxs-lookup"><span data-stu-id="32e61-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="32e61-115">O comando armazena o valor na variável $value.</span><span class="sxs-lookup"><span data-stu-id="32e61-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="32e61-116">OS</span><span class="sxs-lookup"><span data-stu-id="32e61-116">PARAMETERS</span></span>

### <span data-ttu-id="32e61-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32e61-117">-AutomationAccountName</span></span>
<span data-ttu-id="32e61-118">Especifica o nome da conta de automação que contém as variáveis obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e61-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e61-119">-DefaultProfile</span></span>
<span data-ttu-id="32e61-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="32e61-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32e61-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="32e61-121">-Name</span></span>
<span data-ttu-id="32e61-122">Especifica o nome de uma variável obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e61-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e61-123">-ResourceGroupName</span></span>
<span data-ttu-id="32e61-124">Especifica o grupo de recursos para o qual esse cmdlet obtém variáveis.</span><span class="sxs-lookup"><span data-stu-id="32e61-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e61-125">CommonParameters</span></span>
<span data-ttu-id="32e61-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e61-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e61-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e61-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32e61-128">INPUTS</span></span>

### <span data-ttu-id="32e61-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32e61-129">System.String</span></span>

## <span data-ttu-id="32e61-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32e61-130">OUTPUTS</span></span>

### <span data-ttu-id="32e61-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="32e61-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="32e61-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32e61-132">NOTES</span></span>

## <span data-ttu-id="32e61-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32e61-133">RELATED LINKS</span></span>

[<span data-ttu-id="32e61-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="32e61-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="32e61-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="32e61-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="32e61-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="32e61-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


