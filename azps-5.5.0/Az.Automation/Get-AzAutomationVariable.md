---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117003"
---
# <span data-ttu-id="4c53f-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4c53f-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="4c53f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c53f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c53f-103">Obtém uma variável automação.</span><span class="sxs-lookup"><span data-stu-id="4c53f-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="4c53f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c53f-104">SYNTAX</span></span>

### <span data-ttu-id="4c53f-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c53f-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c53f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4c53f-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c53f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c53f-107">DESCRIPTION</span></span>
<span data-ttu-id="4c53f-108">O **cmdlet Get-AzAutomationVariable** obtém uma ou mais variáveis de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c53f-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="4c53f-109">Para obter uma variável específica, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="4c53f-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="4c53f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c53f-110">EXAMPLES</span></span>

### <span data-ttu-id="4c53f-111">Exemplo 1: Obter uma variável</span><span class="sxs-lookup"><span data-stu-id="4c53f-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="4c53f-112">O primeiro comando obtém uma variável automação chamada Variável06 na conta chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4c53f-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="4c53f-113">O comando armazena esse objeto na variável $Variable dados.</span><span class="sxs-lookup"><span data-stu-id="4c53f-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="4c53f-114">O segundo comando usa notação de ponto padrão para se referir à propriedade **de** valor de $Variable.</span><span class="sxs-lookup"><span data-stu-id="4c53f-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="4c53f-115">O comando armazena o valor na variável $value dados.</span><span class="sxs-lookup"><span data-stu-id="4c53f-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="4c53f-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c53f-116">PARAMETERS</span></span>

### <span data-ttu-id="4c53f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c53f-117">-AutomationAccountName</span></span>
<span data-ttu-id="4c53f-118">Especifica o nome da conta automação que contém as variáveis que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4c53f-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4c53f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c53f-119">-DefaultProfile</span></span>
<span data-ttu-id="4c53f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4c53f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c53f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c53f-121">-Name</span></span>
<span data-ttu-id="4c53f-122">Especifica o nome de uma variável que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4c53f-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4c53f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c53f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c53f-124">Especifica o grupo de recursos para o qual este cmdlet obtém variáveis.</span><span class="sxs-lookup"><span data-stu-id="4c53f-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="4c53f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c53f-125">CommonParameters</span></span>
<span data-ttu-id="4c53f-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c53f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c53f-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c53f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c53f-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c53f-128">INPUTS</span></span>

### <span data-ttu-id="4c53f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4c53f-129">System.String</span></span>

## <span data-ttu-id="4c53f-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c53f-130">OUTPUTS</span></span>

### <span data-ttu-id="4c53f-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="4c53f-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="4c53f-132">Notas</span><span class="sxs-lookup"><span data-stu-id="4c53f-132">NOTES</span></span>

## <span data-ttu-id="4c53f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c53f-133">RELATED LINKS</span></span>

[<span data-ttu-id="4c53f-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4c53f-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="4c53f-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4c53f-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="4c53f-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4c53f-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


