---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 96e7be91319713ca17f6ad443596316513d2bfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428304"
---
# <span data-ttu-id="5fc91-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5fc91-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="5fc91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fc91-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc91-103">Modifica uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="5fc91-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fc91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fc91-104">SYNTAX</span></span>

### <span data-ttu-id="5fc91-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="5fc91-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc91-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="5fc91-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fc91-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fc91-107">DESCRIPTION</span></span>
<span data-ttu-id="5fc91-108">O cmdlet **set-AzureRmAutomationVariable** modifica o valor ou a descrição de uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5fc91-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="5fc91-109">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="5fc91-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="5fc91-110">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="5fc91-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="5fc91-111">A especificação *criptografada* para uma variável existente, não criptografada falha.</span><span class="sxs-lookup"><span data-stu-id="5fc91-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="5fc91-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fc91-112">EXAMPLES</span></span>

### <span data-ttu-id="5fc91-113">Exemplo 1: definir o valor de uma variável</span><span class="sxs-lookup"><span data-stu-id="5fc91-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="5fc91-114">Esse comando define um novo valor para a variável chamada StringVariable22 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5fc91-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5fc91-115">OS</span><span class="sxs-lookup"><span data-stu-id="5fc91-115">PARAMETERS</span></span>

### <span data-ttu-id="5fc91-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5fc91-116">-AutomationAccountName</span></span>
<span data-ttu-id="5fc91-117">Especifica o nome da conta de automação na qual a variável está armazenada.</span><span class="sxs-lookup"><span data-stu-id="5fc91-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="5fc91-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5fc91-118">-Description</span></span>
<span data-ttu-id="5fc91-119">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="5fc91-119">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="5fc91-120">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="5fc91-120">-Encrypted</span></span>
<span data-ttu-id="5fc91-121">Especifica se o cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5fc91-121">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="5fc91-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fc91-122">-Name</span></span>
<span data-ttu-id="5fc91-123">Especifica o nome da variável que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5fc91-123">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5fc91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc91-124">-ResourceGroupName</span></span>
<span data-ttu-id="5fc91-125">Especifica o grupo de recursos para o qual esse cmdlet modifica uma variável.</span><span class="sxs-lookup"><span data-stu-id="5fc91-125">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="5fc91-126">-Valor</span><span class="sxs-lookup"><span data-stu-id="5fc91-126">-Value</span></span>
<span data-ttu-id="5fc91-127">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="5fc91-127">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="5fc91-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc91-128">-DefaultProfile</span></span>
<span data-ttu-id="5fc91-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fc91-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc91-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc91-130">CommonParameters</span></span>
<span data-ttu-id="5fc91-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc91-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc91-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc91-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc91-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fc91-133">INPUTS</span></span>

## <span data-ttu-id="5fc91-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fc91-134">OUTPUTS</span></span>

### <span data-ttu-id="5fc91-135">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="5fc91-135">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="5fc91-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fc91-136">NOTES</span></span>

## <span data-ttu-id="5fc91-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fc91-137">RELATED LINKS</span></span>

[<span data-ttu-id="5fc91-138">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5fc91-138">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="5fc91-139">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5fc91-139">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="5fc91-140">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5fc91-140">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


