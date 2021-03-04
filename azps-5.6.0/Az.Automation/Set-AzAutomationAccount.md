---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: bc810da3cd43a18506160d03e6c172eb272bd797
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892881"
---
# <span data-ttu-id="32467-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="32467-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="32467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32467-102">SYNOPSIS</span></span>
<span data-ttu-id="32467-103">Modifica uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="32467-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="32467-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32467-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32467-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32467-105">DESCRIPTION</span></span>
<span data-ttu-id="32467-106">O cmdlet **Set-AzAutomationAccount** modifica uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="32467-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="32467-107">Para obter mais informações sobre contas de automação, consulte New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32467-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="32467-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32467-108">EXAMPLES</span></span>

### <span data-ttu-id="32467-109">Exemplo 1: definir as marcas de uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="32467-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="32467-110">O primeiro comando atribui dois pares de chave/valor à $Tags variável.</span><span class="sxs-lookup"><span data-stu-id="32467-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="32467-111">O segundo comando define marcas em $Tags para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="32467-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="32467-112">Exemplo 2: Alterar o plano de uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="32467-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="32467-113">Este comando altera o plano para Basic para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="32467-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="32467-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32467-114">PARAMETERS</span></span>

### <span data-ttu-id="32467-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32467-115">-DefaultProfile</span></span>
<span data-ttu-id="32467-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="32467-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32467-117">-Name</span><span class="sxs-lookup"><span data-stu-id="32467-117">-Name</span></span>
<span data-ttu-id="32467-118">Especifica o nome da conta de automação que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="32467-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32467-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="32467-119">-Plan</span></span>
<span data-ttu-id="32467-120">Especifica o plano para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="32467-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="32467-121">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="32467-121">Valid values are:</span></span>
- <span data-ttu-id="32467-122">Básico</span><span class="sxs-lookup"><span data-stu-id="32467-122">Basic</span></span>
- <span data-ttu-id="32467-123">Gratuito</span><span class="sxs-lookup"><span data-stu-id="32467-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32467-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32467-124">-ResourceGroupName</span></span>
<span data-ttu-id="32467-125">Especifica o nome de um grupo de recursos que contém a conta de automação que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="32467-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="32467-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="32467-126">-Tags</span></span>
<span data-ttu-id="32467-127">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="32467-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="32467-128">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="32467-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32467-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32467-129">CommonParameters</span></span>
<span data-ttu-id="32467-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32467-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32467-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32467-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32467-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32467-132">INPUTS</span></span>

### <span data-ttu-id="32467-133">System.String</span><span class="sxs-lookup"><span data-stu-id="32467-133">System.String</span></span>

### <span data-ttu-id="32467-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="32467-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="32467-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32467-135">OUTPUTS</span></span>

### <span data-ttu-id="32467-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="32467-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="32467-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="32467-137">NOTES</span></span>

## <span data-ttu-id="32467-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32467-138">RELATED LINKS</span></span>

[<span data-ttu-id="32467-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="32467-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="32467-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="32467-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="32467-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="32467-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
