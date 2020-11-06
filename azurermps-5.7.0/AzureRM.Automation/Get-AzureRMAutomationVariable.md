---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441505"
---
# <span data-ttu-id="8b819-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8b819-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="8b819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b819-102">SYNOPSIS</span></span>
<span data-ttu-id="8b819-103">Obtém uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="8b819-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b819-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b819-104">SYNTAX</span></span>

### <span data-ttu-id="8b819-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b819-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b819-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8b819-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b819-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b819-107">DESCRIPTION</span></span>
<span data-ttu-id="8b819-108">O cmdlet **Get-AzureRmAutomationVariable** Obtém uma ou mais variáveis de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b819-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="8b819-109">Para obter uma variável específica, especifique o nome dela.</span><span class="sxs-lookup"><span data-stu-id="8b819-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="8b819-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b819-110">EXAMPLES</span></span>

### <span data-ttu-id="8b819-111">Exemplo 1: obter uma variável</span><span class="sxs-lookup"><span data-stu-id="8b819-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="8b819-112">O primeiro comando obtém uma variável de automação chamada Variable06 na conta chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8b819-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="8b819-113">O comando armazena esse objeto na variável $Variable.</span><span class="sxs-lookup"><span data-stu-id="8b819-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="8b819-114">O segundo comando usa a notação de ponto padrão para fazer referência à propriedade **Value** de $Variable.</span><span class="sxs-lookup"><span data-stu-id="8b819-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="8b819-115">O comando armazena o valor na variável $value.</span><span class="sxs-lookup"><span data-stu-id="8b819-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="8b819-116">OS</span><span class="sxs-lookup"><span data-stu-id="8b819-116">PARAMETERS</span></span>

### <span data-ttu-id="8b819-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b819-117">-AutomationAccountName</span></span>
<span data-ttu-id="8b819-118">Especifica o nome da conta de automação que contém as variáveis obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b819-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b819-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b819-119">-DefaultProfile</span></span>
<span data-ttu-id="8b819-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8b819-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b819-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b819-121">-Name</span></span>
<span data-ttu-id="8b819-122">Especifica o nome de uma variável obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b819-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b819-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b819-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b819-124">Especifica o grupo de recursos para o qual esse cmdlet obtém variáveis.</span><span class="sxs-lookup"><span data-stu-id="8b819-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b819-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b819-125">CommonParameters</span></span>
<span data-ttu-id="8b819-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b819-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b819-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b819-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b819-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b819-128">INPUTS</span></span>

### <span data-ttu-id="8b819-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8b819-129">None</span></span>
<span data-ttu-id="8b819-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8b819-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b819-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b819-131">OUTPUTS</span></span>

### <span data-ttu-id="8b819-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="8b819-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="8b819-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b819-133">NOTES</span></span>

## <span data-ttu-id="8b819-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b819-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b819-135">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8b819-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="8b819-136">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8b819-136">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="8b819-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8b819-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


