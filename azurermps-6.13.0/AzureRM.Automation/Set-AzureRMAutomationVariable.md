---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 462566749ce0c55d4f892cc19e362f62b6fd0fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426450"
---
# <span data-ttu-id="ed982-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ed982-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="ed982-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed982-102">SYNOPSIS</span></span>
<span data-ttu-id="ed982-103">Modifica uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="ed982-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed982-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed982-104">SYNTAX</span></span>

### <span data-ttu-id="ed982-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="ed982-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed982-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="ed982-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed982-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed982-107">DESCRIPTION</span></span>
<span data-ttu-id="ed982-108">O cmdlet **set-AzureRmAutomationVariable** modifica o valor ou a descrição de uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed982-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="ed982-109">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="ed982-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="ed982-110">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="ed982-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="ed982-111">A especificação *criptografada* para uma variável existente, não criptografada falha.</span><span class="sxs-lookup"><span data-stu-id="ed982-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="ed982-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed982-112">EXAMPLES</span></span>

### <span data-ttu-id="ed982-113">Exemplo 1: definir o valor de uma variável</span><span class="sxs-lookup"><span data-stu-id="ed982-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="ed982-114">Esse comando define um novo valor para a variável chamada StringVariable22 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ed982-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ed982-115">OS</span><span class="sxs-lookup"><span data-stu-id="ed982-115">PARAMETERS</span></span>

### <span data-ttu-id="ed982-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed982-116">-AutomationAccountName</span></span>
<span data-ttu-id="ed982-117">Especifica o nome da conta de automação na qual a variável está armazenada.</span><span class="sxs-lookup"><span data-stu-id="ed982-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="ed982-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed982-118">-DefaultProfile</span></span>
<span data-ttu-id="ed982-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ed982-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed982-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ed982-120">-Description</span></span>
<span data-ttu-id="ed982-121">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="ed982-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed982-122">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="ed982-122">-Encrypted</span></span>
<span data-ttu-id="ed982-123">Especifica se o cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ed982-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed982-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed982-124">-Name</span></span>
<span data-ttu-id="ed982-125">Especifica o nome da variável que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ed982-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed982-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed982-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed982-127">Especifica o grupo de recursos para o qual esse cmdlet modifica uma variável.</span><span class="sxs-lookup"><span data-stu-id="ed982-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="ed982-128">-Valor</span><span class="sxs-lookup"><span data-stu-id="ed982-128">-Value</span></span>
<span data-ttu-id="ed982-129">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="ed982-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed982-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed982-130">CommonParameters</span></span>
<span data-ttu-id="ed982-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed982-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed982-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed982-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed982-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed982-133">INPUTS</span></span>

### <span data-ttu-id="ed982-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed982-134">System.String</span></span>

### <span data-ttu-id="ed982-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed982-135">System.Boolean</span></span>

### <span data-ttu-id="ed982-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="ed982-136">System.Object</span></span>

## <span data-ttu-id="ed982-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed982-137">OUTPUTS</span></span>

### <span data-ttu-id="ed982-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="ed982-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="ed982-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed982-139">NOTES</span></span>

## <span data-ttu-id="ed982-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed982-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed982-141">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ed982-141">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="ed982-142">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ed982-142">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="ed982-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ed982-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


