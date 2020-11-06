---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: 8866c805f0cbb42d72c8940d31652bc8e5444cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431812"
---
# <span data-ttu-id="e1096-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e1096-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="e1096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1096-102">SYNOPSIS</span></span>
<span data-ttu-id="e1096-103">Remove uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="e1096-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1096-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1096-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1096-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1096-105">DESCRIPTION</span></span>
<span data-ttu-id="e1096-106">O cmdlet **Remove-AzureRmAutomationVariable** remove uma variável da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e1096-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="e1096-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1096-107">EXAMPLES</span></span>

### <span data-ttu-id="e1096-108">Exemplo 1: remover uma variável</span><span class="sxs-lookup"><span data-stu-id="e1096-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e1096-109">Esse comando Remove uma variável chamada StringVariable22 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e1096-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e1096-110">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="e1096-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e1096-111">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="e1096-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e1096-112">OS</span><span class="sxs-lookup"><span data-stu-id="e1096-112">PARAMETERS</span></span>

### <span data-ttu-id="e1096-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1096-113">-AutomationAccountName</span></span>
<span data-ttu-id="e1096-114">Especifica o nome da conta de automação que contém a variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="e1096-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e1096-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1096-115">-Name</span></span>
<span data-ttu-id="e1096-116">Especifica o nome da variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="e1096-116">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e1096-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1096-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1096-118">Especifica o grupo de recursos para o qual esse cmdlet exclui uma variável.</span><span class="sxs-lookup"><span data-stu-id="e1096-118">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="e1096-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1096-119">-Confirm</span></span>
<span data-ttu-id="e1096-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1096-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1096-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1096-121">-WhatIf</span></span>
<span data-ttu-id="e1096-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1096-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1096-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1096-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1096-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1096-124">-DefaultProfile</span></span>
<span data-ttu-id="e1096-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1096-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1096-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1096-126">CommonParameters</span></span>
<span data-ttu-id="e1096-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1096-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1096-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1096-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1096-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1096-129">INPUTS</span></span>

## <span data-ttu-id="e1096-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1096-130">OUTPUTS</span></span>

### <span data-ttu-id="e1096-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="e1096-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="e1096-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1096-132">NOTES</span></span>

## <span data-ttu-id="e1096-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1096-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1096-134">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e1096-134">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="e1096-135">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e1096-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="e1096-136">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e1096-136">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


