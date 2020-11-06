---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430526"
---
# <span data-ttu-id="2aa7a-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2aa7a-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="2aa7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2aa7a-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa7a-103">Remove uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aa7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2aa7a-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2aa7a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2aa7a-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa7a-106">O cmdlet **Remove-AzureRmAutomationVariable** remove uma variável da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="2aa7a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aa7a-107">EXAMPLES</span></span>

### <span data-ttu-id="2aa7a-108">Exemplo 1: remover uma variável</span><span class="sxs-lookup"><span data-stu-id="2aa7a-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2aa7a-109">Esse comando Remove uma variável chamada StringVariable22 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="2aa7a-110">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="2aa7a-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2aa7a-111">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2aa7a-112">OS</span><span class="sxs-lookup"><span data-stu-id="2aa7a-112">PARAMETERS</span></span>

### <span data-ttu-id="2aa7a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2aa7a-113">-AutomationAccountName</span></span>
<span data-ttu-id="2aa7a-114">Especifica o nome da conta de automação que contém a variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="2aa7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa7a-115">-DefaultProfile</span></span>
<span data-ttu-id="2aa7a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2aa7a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aa7a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2aa7a-117">-Name</span></span>
<span data-ttu-id="2aa7a-118">Especifica o nome da variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa7a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa7a-119">-ResourceGroupName</span></span>
<span data-ttu-id="2aa7a-120">Especifica o grupo de recursos para o qual esse cmdlet exclui uma variável.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="2aa7a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2aa7a-121">-Confirm</span></span>
<span data-ttu-id="2aa7a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa7a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa7a-123">-WhatIf</span></span>
<span data-ttu-id="2aa7a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa7a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa7a-126">CommonParameters</span></span>
<span data-ttu-id="2aa7a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa7a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa7a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa7a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2aa7a-129">INPUTS</span></span>

### <span data-ttu-id="2aa7a-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2aa7a-130">None</span></span>
<span data-ttu-id="2aa7a-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2aa7a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2aa7a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2aa7a-132">OUTPUTS</span></span>

### <span data-ttu-id="2aa7a-133">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="2aa7a-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="2aa7a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2aa7a-134">NOTES</span></span>

## <span data-ttu-id="2aa7a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aa7a-135">RELATED LINKS</span></span>

[<span data-ttu-id="2aa7a-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2aa7a-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="2aa7a-137">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2aa7a-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="2aa7a-138">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2aa7a-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


